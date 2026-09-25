# Missione Python

Un **gioco interattivo** per imparare le basi di Python, pensato per la scuola secondaria di primo grado.

Il robot **Pyto** si è schiantato con il suo razzo e i pezzi sono sparsi su **6 pianeti**. Su ogni pianeta ci sono **3 problemi**, cioè 2 esercizi di codice e 1 quiz. Chi li risolve tutti libera il pianeta e recupera un pezzo del razzo. Quando tutti i pezzi sono recuperati, il razzo riparte e lo studente riceve un diploma.

**Gioca:** https://annadm81.github.io/SWIM/ (funziona dopo aver attivato GitHub Pages, vedi sotto)

## Cosa c'è nel gioco

| Sezione | A cosa serve |
|---|---|
| **Mappa stellare** | I 6 pianeti in ordine: ognuno si sblocca quando si finisce il precedente |
| **Problemi** | Un editor Python con i colori del codice, il pulsante *Esegui* per provare e *Consegna* per la verifica automatica |
| **Quiz** | Domande a scelta multipla del tipo "cosa stampa questo programma?", da risolvere senza eseguire il codice |
| **Laboratorio** | Un editor libero, senza punti, con 4 esempi pronti |
| **Registro della classe** | L'elenco condiviso dei progressi di tutti gli studenti. Funziona solo dal link di Claude |
| **Modalità docente** | Sblocca tutti i pianeti e tutte le soluzioni |
| **Suoni** | Effetti per le risposte giuste e sbagliate, le stelle, i pianeti liberati e il decollo, con un pulsante per spegnerli |

Il codice Python viene eseguito **nel browser** con [Skulpt](https://skulpt.org). Non serve installare niente e non serve un server.

## Documentazione

- [Guida per il docente](docs/GUIDA-DOCENTE.md): come usarlo in classe, la modalità docente, il registro e i problemi più comuni
- [Guida per lo studente](docs/GUIDA-STUDENTE.md): come si gioca e come si guadagnano le stelle
- [Contenuti didattici](docs/CONTENUTI.md): i 6 pianeti e i 18 problemi, con obiettivi e soluzioni
- [Documentazione tecnica](docs/TECNICA.md): come è fatto il codice e come si aggiunge o si modifica un problema
- [Storia delle versioni](docs/VERSIONI.md): le versioni in `versioni/` e le differenze tra una e l'altra
- [Traguardi, obiettivi e valutazione](docs/DIDATTICA.md): il collegamento con le Indicazioni nazionali, una griglia di valutazione e una prova finale

## Struttura del repository

```
index.html        il gioco (versione attuale, 6 pianeti)
README.md         questo file
LICENSE.md        la licenza (CC BY-SA 4.0)
docs/             la documentazione
versioni/         tutte le versioni precedenti, così come sono state scaricate dalla chat
```

## Due link diversi

| | Link di Claude | GitHub Pages |
|---|---|---|
| Indirizzo | https://claude.ai/artifact/2ChwKNxjWtaZ6CAjYNU6Ui | https://annadm81.github.io/SWIM/ |
| Serve un account | Sì, un account Claude della scuola | No, basta il link |
| Registro della classe | ✅ Condiviso tra tutti | ❌ Mostra solo un avviso |
| Progressi | Nel registro e nel browser | Solo nel browser di quel PC |
| Suoni, gioco, laboratorio | ✅ | ✅ |

## Mettere online il gioco (GitHub Pages)

1. Apri **Settings → Pages** del repository.
2. In **Source** scegli **Deploy from a branch**.
3. In **Branch** scegli **`main`** e la cartella **`/ (root)`**, poi premi **Save**.
4. Dopo 1-2 minuti il gioco è su https://annadm81.github.io/SWIM/.

## Aggiornare il gioco

Dal sito di GitHub: **Add file → Upload files**, carica il nuovo `index.html` (con esattamente questo nome) e premi **Commit changes**. GitHub Pages si aggiorna da solo in un paio di minuti.

## Crediti

- **Anno scolastico:** 2026/2027
- **Autrici:** Lidia M. e Anna
- **Tipo di risorsa:** gioco interattivo
- **Realizzazione:** con l'aiuto di Claude (Anthropic)
- **Interprete Python:** [Skulpt](https://skulpt.org)

## Licenza

[CC BY-SA 4.0](LICENSE.md): puoi riusare e modificare il gioco citando le autrici (Lidia M. e Anna) e condividendo le modifiche con la stessa licenza.
