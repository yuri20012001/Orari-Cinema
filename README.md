# Turni Cinema — web app installabile su iPhone

Questa è una Progressive Web App (PWA). Non richiede Mac, account o abbonamenti.
Per installarla sulla schermata Home deve essere pubblicata su un indirizzo HTTPS.

## Pubblicazione gratuita con GitHub Pages
1. Crea gratuitamente un account GitHub e un nuovo repository pubblico, ad esempio `turni-cinema`.
2. Carica tutti i file contenuti in questa cartella nella radice del repository.
3. In Settings → Pages seleziona `Deploy from a branch`, branch `main`, cartella `/root`, quindi Save.
4. Attendi la pubblicazione e apri l'indirizzo HTTPS indicato da GitHub Pages su Safari dell'iPhone.
5. Premi Condividi → Aggiungi alla schermata Home.

## Utilizzo
1. Apri Turni Cinema dalla schermata Home.
2. Lascia o modifica il nominativo `Marchiani Yuri`.
3. Seleziona il PDF.
4. Controlla date e orari riconosciuti e deseleziona eventuali turni errati.
5. Premi `Crea file per Calendario Apple`, apri il file `.ics` e importa gli eventi nel Calendario.

## Limite importante
Una PWA su iOS non può scrivere direttamente nel database del Calendario Apple. Per sicurezza iOS richiede il passaggio di importazione del file `.ics`. La lettura PDF usa PDF.js da CDN, quindi per la prima lettura del PDF serve una connessione Internet. I dati del PDF vengono elaborati nel browser e non inviati a un server.

## Nota sul parser
I PDF tabellari possono cambiare struttura a seconda del software che li genera. Il parser tenta di associare gli orari alle colonne dei giorni usando la posizione degli elementi PDF. Verifica sempre l'anteprima prima di importare; se il PDF specifico non viene riconosciuto correttamente, si può adattare il parser al modello esatto.
