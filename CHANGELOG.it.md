# Changelog

[English](CHANGELOG.md) | **Italiano**

Tutte le versioni di acrk-tray, dalla più recente. Le versioni seguono `MAJOR.MINOR.PATCH`;
il setup di ognuna è nella pagina [Releases](https://github.com/agastal/acrkchallenge-Release/releases).

## [0.6.2] - 2026-09-27

Le sessioni registrate non riempiono più il disco.

### Modifiche

- Le sessioni registrate (circa 85 MB per ora di guida) le pulisce l'app: all'inizio di ogni
  sessione cancella quelle più vecchie di 30 giorni, poi le più vecchie finché il resto sta in
  500 MB.

## [0.6.1] - 2026-09-27

Un riavvio non fa più perdere il tentativo successivo di una sfida che ne ha più di uno.

### Correzioni

- In una sfida con più tentativi, riavviare la prova ritirava il tentativo e fermava la
  registrazione, così la prova guidata subito dopo non veniva vista. Ora l'app arma subito il
  tentativo successivo e continua a registrare: la prova che parte dopo il riavvio è quel
  tentativo, e una notifica lo dice (*riavvio. Il tentativo 2 di 3 è armato*).

### Modifiche

- La finestra Sfide è più stretta e più alta.

## [0.6.0] - 2026-09-27

Suoni e avvisi per quello che succede mentre guidi, e più controllo su come parte l'app.

### Novità

- Un avviso con suono **prima della partenza** quando il gioco sta caricando una prova diversa
  da quella della sfida: torna al menu, o il tentativo è ritirato.
- Suoni per l'esito di ogni prova (tempo ricevuto, tentativo chiuso, ritiro, avviso, errore),
  perché Windows trattiene le notifiche mentre il gioco è a schermo intero.
- I tempi intermedi vengono letti dal gioco e inviati con ogni prova.
- **Impostazioni**: "Avvia acrk-tray all'accesso a Windows" e "Controlla una volta al giorno se
  ci sono nuove versioni", entrambe disattivabili.

### Modifiche

- Chiudere il gioco durante una prova ora ritira il tentativo (motivo "closed") e la sessione
  aspetta che il gioco riparta.
- A riposo, l'icona nell'area di notifica è il cronometro dell'app in grigio.
- La scorciatoia del segnaposto non c'è più: restano avvio e stop.
- La finestra Sfide spiega che per il time attack si avvia una sessione dal menu, e da lì ogni
  prova che guidi conta.
- L'avvio con Windows ora usa la stessa impostazione dell'app: setup e Impostazioni sono
  d'accordo e l'app non parte mai due volte.

## [0.5.0] - 2026-09-26

Prima versione pubblica.

### Novità

- Installer: setup per utente, senza diritti di amministratore, voce nel menu Start, avvio con
  Windows facoltativo; prima dell'installazione mostra la pagina sui tuoi dati. La
  disinstallazione propone di cancellare impostazioni e sessioni registrate.
- Controllo aggiornamenti: una volta al giorno l'app chiede a GitHub l'ultima versione e, se
  ce n'è una più recente, lo segnala con una notifica e la voce di menu **Scarica
  l'aggiornamento**. L'aggiornamento resta manuale.
- Nuova finestra **Sfide** con l'aspetto del sito: una scheda per prova con condizioni, auto,
  data di chiusura, tentativi e stato colorato; chiara o scura come Windows. Doppio clic su una
  prova pronta per avviare il tentativo.
- La versione dell'app è indicata nel menu e nelle proprietà del file.

### Già presente

- Registra le prove da memoria condivisa e salvataggio, e manda ogni prova conclusa ad ACR
  Challenge una volta collegato il PC al sito; senza rete i risultati aspettano in una coda.
- Sfide con tentativi limitati: armamento, partenza, riavvio e uscita dalla prova comunicati al
  sito; la registrazione avviata da un tentativo si ferma quando il tentativo finisce.
- Screenshot della schermata della sessione inviato con le prove, per verificare meteo e
  configurazione.
- Scorciatoie globali con suoni, interfaccia in cinque lingue.
