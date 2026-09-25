# Documentazione tecnica

## Com'è fatto

Tutto il gioco sta in **un solo file**, `index.html`: HTML, CSS e JavaScript insieme, senza build e senza server. Dall'esterno carica solo:

| Risorsa | Da dove | Se manca |
|---|---|---|
| Skulpt 1.2.0 (interprete Python) | `cdn.jsdelivr.net` | Il codice non si può eseguire |
| Caratteri Lilita One, Nunito, JetBrains Mono | Google Fonts | Si usano i caratteri del sistema |

Suoni, grafica (Pyto, pianeti, razzo) e animazioni sono generati dal codice: non ci sono immagini o file audio.

## Parti principali dello script

| Sezione (commento nel codice) | Cosa contiene |
|---|---|
| `CONTENUTI` | L'array `LEVELS`: pianeti e problemi |
| `SNIPPETS` | Gli esempi del Laboratorio |
| `STATO` | Il salvataggio dei progressi |
| Editor | Una `textarea` trasparente sopra un `pre` con i colori della sintassi, i numeri di riga, `Tab`/`Maiusc+Tab` e `Ctrl+Invio` |
| `runPython` | L'esecuzione con Skulpt, l'input simulato e i test nascosti |
| `submit` / `answerQuiz` / `complete` | La verifica, le stelle, gli XP e la finestra di premio |
| Suoni (`sfx`) | Sintesi con la Web Audio API: `click`, `warp`, `run`, `ok`, `bad`, `star`, `hint`, `planet`, `levelup`, `fireworks`, `launch` |
| `REGISTRO DELLA CLASSE` | Il registro condiviso (solo su Claude) |

## Come si aggiunge o si modifica un problema

Ogni pianeta in `LEVELS` ha questa forma:

```js
{ id:"p1", planet:"Printia", topic:"print e testo",
  c:["#7FB2FF","#2C4FB8"],   // colore chiaro e scuro del pianeta
  ring:false,                // anello attorno al pianeta
  boss:true,                 // (facoltativo) pianeta finale, più grande
  part:"l'antenna",          // pezzo del razzo che si recupera
  intro:"…",                 // frase di Pyto
  problems:[ … ] }
```

### Esercizio di codice

```js
{ id:"s-ciao", type:"code", xp:100, title:"Ciao, mondo!",
  story:"…",                           // nuvoletta di Pyto
  concept:"<p>…</p>",                  // spiegazione (HTML)
  example:`print("Buongiorno!")`,      // esempio
  task:"Fai stampare … <kbd>…</kbd>",  // la missione
  starter:`# codice iniziale\n`,
  runs:[{inputs:["7"], out:"Il doppio è 14"}, …],   // prove: input e output atteso
  require:[["regex", "messaggio se manca"]],        // (facoltativo) costrutti obbligatori
  forbid:[["testo", "messaggio se presente"]],      // (facoltativo) costrutti vietati
  tests:`assert x == 12, "messaggio"`,              // (facoltativo) controlli sulle variabili
  hint:"…",
  solution:`…` }
```

- L'output viene confrontato **dopo aver tolto gli spazi alla fine delle righe**.
- `tests` viene eseguito solo nella prima prova, dopo il codice dello studente.
- Ogni esecuzione si ferma dopo **4 secondi**, così un ciclo infinito non blocca la pagina.

### Quiz

```js
{ id:"s-q-prec", type:"quiz", xp:50, title:"Quiz: chi va prima?",
  story:"…", question:"Cosa stampa questo programma?",
  code:`print(2 + 3 * 4)`,
  options:["20", "14", "2 + 3 * 4", "24"],
  answer:1,        // indice della risposta giusta, partendo da 0
  explain:"…" }
```

> Gli `id` dei problemi devono essere **unici** e **non vanno cambiati** dopo che gli studenti hanno iniziato: i progressi sono salvati usando l'`id`.

Dopo ogni modifica prova il problema in modalità docente: prima con la soluzione, che deve passare, poi con un errore, che deve essere segnalato.

## Salvataggio (localStorage)

| Chiave | Contenuto |
|---|---|
| `missione-python-v3` | Nome, classe, problemi risolti (stelle e XP), pianeti liberati, codice scritto, tentativi, modalità docente |
| `missione-python-v3-lab` | Il codice del Laboratorio |
| `missione-python-v3-sound` | Suoni attivi (`on`) o spenti (`off`) |

Le versioni a 10 pianeti usavano la chiave `missione-python-v2`: i progressi fatti con quelle versioni non passano a quella attuale.

Se si cambia molto la struttura dei livelli, conviene cambiare la chiave (`v4`) per non mescolare dati vecchi e nuovi.

## Registro della classe

Il registro usa le funzioni che Claude mette a disposizione delle pagine pubblicate (`window.claude.use("db")` e `window.claude.use("user")`). Fuori da Claude queste funzioni non esistono: dopo circa 6 secondi il gioco mostra un avviso e continua a funzionare senza registro.

- **Dati:** la raccolta `registro` contiene un documento per ogni utente, identificato dall'ID dell'utente. Ogni documento ha i campi `nome`, `classe`, `xp`, `stelle`, `pianeti`, `problemi`, `progresso` (i problemi risolti per ogni pianeta) e `aggiornato`.
- **Permessi:** chi può vedere la pagina legge il registro. Ognuno può scrivere solo il proprio documento, se ha il permesso "Può interagire". Solo la proprietaria può cancellare le righe degli altri.
- La riga si aggiorna circa 1 secondo dopo ogni cambiamento, e solo se i dati sono cambiati davvero.

Per avere un registro condiviso anche su GitHub Pages servirebbe un servizio esterno (per esempio Firebase o Supabase), con account e configurazione propri.

## Accessibilità

- Si può usare tutto con la tastiera. Il focus è evidenziato in giallo.
- Le etichette ARIA sono sui pulsanti e sulle aree che si aggiornano da sole.
- Con l'impostazione di sistema "riduci movimento" le animazioni si spengono.
- Il layout si adatta al telefono: sotto i 900 px diventa una colonna sola.
