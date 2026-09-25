# Guida per il docente

## In breve

- **Destinatari:** scuola secondaria di primo grado, principianti assoluti di programmazione.
- **Durata:** 6 pianeti con 3 problemi ciascuno. Indicativamente un pianeta ogni 20-30 minuti, quindi 2-3 lezioni per tutto il percorso. Chi finisce prima può usare il Laboratorio.
- **Serve:** un PC con un browser recente (Chrome, Edge, Firefox o Safari) e la connessione a internet, perché l'interprete Python e i caratteri si caricano dalla rete.
- **Non serve:** installare programmi o creare account (tranne per il registro, vedi sotto).

## Quale link dare agli studenti

| Situazione | Link da usare |
|---|---|
| Vuoi vedere i progressi di tutta la classe nel registro | **Link di Claude**: https://claude.ai/artifact/2ChwKNxjWtaZ6CAjYNU6Ui |
| Gli studenti non hanno un account Claude della scuola, o vuoi un link semplice | **GitHub Pages**: https://annadm81.github.io/SWIM/ |

### Link di Claude (con registro)

- Gli studenti devono entrare con l'**account Claude della scuola**. Il gioco non si può aprire con un link pubblico.
- Dal menu **Condividi** dai agli studenti il permesso **"Può interagire"**. Con "Può visualizzare" vedono il registro, ma non ci compaiono.
- Prima della lezione fai una prova con un account studente: risolvi un problema e controlla che la sua riga compaia nel registro.

### GitHub Pages (senza registro)

- Basta aprire il link, senza account.
- I progressi restano **nel browser di quel PC**. Se lo studente cambia PC o browser, riparte da zero.
- La scheda "Registro della classe" mostra un avviso e non funziona.

## Prima lezione: cosa dire agli studenti

1. Scrivete **nome e cognome** nel campo "Pilota", in alto.
2. Se usate il link di Claude, andate su **Registro della classe** e scrivete anche la **classe** (per esempio `3B`).
3. Partite dal pianeta 1 e leggete sempre la nuvoletta di Pyto, la spiegazione e l'esempio.
4. Usate **Esegui** per provare quante volte volete: non costa niente. Premete **Consegna** solo quando siete convinti.
5. Se usate le cuffie, controllate i suoni. Se lavorate senza cuffie, spegneteli con il pulsante dell'altoparlante in alto a destra.

## Come si guadagnano stelle e punti

### Esercizi di codice

| Situazione | Stelle | Punti (XP) |
|---|---|---|
| Giusto alla prima consegna, senza suggerimento | ★★★ | 100% |
| Usato il suggerimento, oppure 1-2 consegne sbagliate | ★★ | 80% |
| 3 o più consegne sbagliate | ★ | 50% |
| Guardata la soluzione | ★ | 50% |

*Esegui* non conta come tentativo: contano solo le consegne sbagliate.

### Quiz

| Situazione | Stelle |
|---|---|
| Giusto al primo colpo | ★★★ |
| 1 risposta sbagliata | ★★ |
| 2 o più risposte sbagliate | ★ |

### Punti e gradi

- Ogni esercizio di codice vale **100 XP**, ogni quiz **50 XP** e la sfida finale **150 XP**.
- Ogni pianeta liberato dà **100 XP di bonus**.
- In tutto si possono fare **2150 XP** e **54 stelle**.
- Chi rifà un problema e fa meglio aggiorna le stelle e i punti. Se fa peggio, non perde niente.

| Grado | Punti necessari |
|---|---|
| Cadetto | 0 |
| Pilota | 258 |
| Navigatore | 753 |
| Comandante | 1290 |
| Ammiraglio Python | 1828 |

## Suggerimenti e soluzioni

- Il **suggerimento** si può aprire sempre, ma costa una stella.
- La **soluzione** si sblocca dopo **3 consegne sbagliate**. Guardarla vale al massimo 1 stella.
- Dopo aver visto la soluzione, lo studente può copiarla nell'editor con un pulsante. Pyto consiglia di riscriverla con parole proprie.

## Modalità docente

La casella **"Modalità docente"**, in fondo alla pagina, sblocca tutti i pianeti, tutti i problemi e tutte le soluzioni. Serve per:

- preparare la lezione e provare i problemi;
- proiettare un problema alla lavagna e risolverlo insieme alla classe.

> ⚠️ **Attenzione:** la casella **non ha una password**. Anche gli studenti possono attivarla e vedere le soluzioni. Se è un problema, dillo agli studenti fin dall'inizio oppure chiedi di aggiungere una protezione.

## Registro della classe (solo link di Claude)

- Ogni studente compare con nome, classe, pianeti liberati (pallini colorati: pieno = liberato, chiaro = iniziato), stelle, punti e ultima attività.
- In alto ci sono tre numeri: quanti piloti ci sono, quanti pianeti liberano in media e quante missioni sono state completate.
- Puoi **filtrare per classe** e **ordinare** per punti, stelle, nome o ultima attività.
- L'elenco si aggiorna da solo quando qualcuno risolve un problema.
- **Chi può fare cosa:**
  - ogni studente modifica solo la propria riga;
  - tu, come proprietaria del gioco, puoi **rimuovere** qualsiasi riga (per esempio quelle di prova). La rimozione chiede una conferma.

## Azzerare i progressi

Il pulsante **"Azzera progressi"**, in fondo alla pagina, va premuto **due volte** (la seconda volta chiede conferma). Cancella stelle, punti e codice scritto, ma **tiene il nome e la classe**. Con il link di Claude aggiorna anche la riga nel registro.

## PC del laboratorio condivisi

I progressi sono salvati **nel browser**. Questo significa che:

- se due studenti usano lo stesso PC e lo stesso browser, **condividono i progressi**. Usate un PC a testa, oppure profili diversi del browser;
- se lo studente cambia PC la lezione dopo, **riparte da zero**. Con il link di Claude il registro mostra comunque i risultati raggiunti, ma il gioco sul nuovo PC riparte dall'inizio;
- la navigazione in incognito cancella tutto quando si chiude la finestra.

## Problemi comuni

| Problema | Cosa fare |
|---|---|
| In fondo resta scritto "Caricamento dell'interprete Python…" | La rete blocca `cdn.jsdelivr.net`. Chiedi al tecnico di sbloccarlo, oppure ricarica la pagina |
| I caratteri sembrano diversi | La rete blocca Google Fonts. Il gioco funziona lo stesso |
| Non si sente niente | Controlla il pulsante dell'altoparlante e il volume del PC. I suoni partono dopo il primo clic sulla pagina |
| Il registro dice che "funziona solo dal link di Claude" | Stai usando GitHub Pages: usa il link di Claude |
| Lo studente vede il registro ma non ci compare | Nel menu Condividi dagli il permesso "Può interagire" |
| Il programma sembra bloccato | Probabilmente c'è un ciclo infinito: dopo qualche secondo Python si ferma da solo |
| Uno studente ha perso i progressi | Ha cambiato PC o browser, oppure ha cancellato i dati del browser |
