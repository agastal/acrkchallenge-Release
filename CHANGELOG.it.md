# Changelog

[English](CHANGELOG.md) | **Italiano**

Tutte le versioni di acrk-tray, dalla più recente. Le versioni seguono `MAJOR.MINOR.PATCH`;
il setup di ognuna è nella pagina [Releases](https://github.com/agastal/acrkchallenge-Release/releases).

## [0.11.1] - 2026-10-02

I tempi fatti più volte di fila sulla stessa prova speciale tornano ad arrivare al sito.

### Correzioni

- Dopo diverse prove sulla stessa speciale senza tornare al menu, i tempi venivano rifiutati dal sito
  ("game_stage is missing") e non contavano da nessuna parte, nemmeno per il tentativo di una sfida.
  Ora l'app legge la speciale di ogni prova, per quante siano.

## [0.11.0] - 2026-10-02

Gli aggiornamenti si installano dall'app: con un clic, o da soli a gioco chiuso.

### Novità

- *Installa l'aggiornamento X.Y.Z* nel menu (era *Scarica l'aggiornamento*): l'app scarica la nuova
  versione, ne controlla la firma, la installa e si riavvia in pochi secondi, con impostazioni e
  collegamento come prima. Aspetta se il gioco è aperto, se stai registrando i tempi, se c'è un
  tentativo in corso o un tempo ancora da inviare, e lo dice.
- *Installale da sola, a gioco chiuso* nelle Impostazioni, sotto il controllo giornaliero (spenta di
  serie): l'app si aggiorna da sola appena non c'è niente in corso.
- Dopo un aggiornamento un avviso dice quale versione hai ora; un clic apre le novità.
- Ogni setup è firmato: l'app installa solo un setup fatto dall'organizzatore, mai uno rovinato o
  alterato.

### Modifiche

- Questo è l'ultimo aggiornamento da installare a mano: dalla 0.11.0 lo fa l'app.

## [0.10.0] - 2026-10-02

Un overlay sul gioco con il distacco dal tuo record, e le prove notturne distinte per meteo.

### Novità

- *Overlay sul gioco* nel menu: un piccolo riquadro trasparente sopra il gioco con quello che il suo
  HUD non mostra. Un pallino dice se i tempi vengono registrati (giallo spento, verde pronto, rosso
  durante una prova); accanto il tentativo della sfida o la condizione che chiede, il distacco dal
  tuo record con la sua tendenza, il tuo record e il tempo d'arrivo se il distacco resta quello, e
  che fine ha fatto la tua ultima prova (inviata con la posizione in classifica, in attesa di invio,
  non inviata, tentativo valido o ritirato). Compare solo con una prova caricata e il gioco sullo
  schermo, lascia passare i clic al gioco e non finisce negli screenshot né nelle registrazioni.
- *Posiziona l'overlay* (menu, oppure Ctrl+Maiusc+F8, modificabile nelle Impostazioni): trascinalo
  dove vuoi, poi doppio clic o di nuovo la scorciatoia per fissarlo. Mentre lo posizioni, il suo
  pallino avvia e ferma la registrazione tempi.
- L'overlay ti avvisa quando la prova caricata non è quella della sfida.
- *Prova non salvata dal gioco*: un avviso quando il gioco non conserva il risultato di una prova
  conclusa, così sai che quel tempo non è arrivato al sito.

### Modifiche

- La notte ora va con il meteo: *notte, asciutto*, *notte, bagnato* e *notte, neve / ghiaccio* sono
  condizioni distinte, nel pannello pilota e nella finestra Sfide come sul sito.

### Correzioni

- Un nuovo record che il gioco scriveva solo tra i suoi migliori tempi, senza un risultato a sé, non
  veniva inviato: ora arriva al sito.

## [0.9.0] - 2026-10-01

Un pannello pilota per il secondo monitor, con il distacco dal tuo record mentre guidi, e
un'immagine con ogni tempo anche quando l'app non vede la schermata della sessione.

### Novità

- *Pannello pilota...* nel menu: una finestra larga e bassa per il secondo monitor. Un pulsante
  avvia e ferma la registrazione dei tempi, o arma il tentativo della sfida che scegli nel suo
  elenco; accanto, il cronometro della prova, velocità e marcia, le barre di acceleratore e freno e
  la condizione richiesta dalla sfida. Ricorda dove lo metti e può restare sopra le altre finestre
  (Impostazioni).
- Il pannello mostra quanto sei avanti (verde) o indietro (rosso) rispetto al tuo miglior tempo
  sulla stessa prova speciale, auto e condizione, metro per metro, e all'arrivo resta sul distacco
  finale. La prima prova che finisci con il pannello aperto diventa il riferimento; ogni prova più
  veloce lo sostituisce. Queste tracce restano sul tuo PC.
- Quando guidi una prova di una sfida senza avviare il tentativo, un avviso ti dice che il tempo è
  valso solo per il time attack.

### Modifiche

- *Avvia/Ferma sessione* ora si chiama *Avvia/Ferma registrazione tempi*, per non confonderlo con
  AVVIA SESSIONE del gioco.
- Quando l'app non vede la schermata della sessione prima della prova (un'altra modalità di gioco,
  l'app aperta dentro la prova), cattura invece un'immagine della finestra di gioco sulla linea di
  partenza, prima del via, e dice all'organizzatore perché mancava.
- La schermata della sessione viene riconosciuta su più formati di schermo (16:10, ultrawide) e
  quando il gioco è dietro un'altra finestra che non lo copre, come il pannello pilota.
- *Apri la cartella delle sessioni* è uscito dal menu: il wiki dice dov'è la cartella, e *Invia dati per
  l'assistenza...* manda quello che serve.

### Correzioni

- I nomi lunghi delle scorciatoie non vengono più tagliati nelle Impostazioni.

## [0.8.1] - 2026-09-30

Una correzione per i tempi arrivati al sito senza la loro speciale.

### Correzioni

- Alcuni tempi arrivavano al sito con il nome della speciale sbagliato, e il sito non sapeva dove
  metterli: restavano in attesa dell'organizzatore e, nel frattempo, il tentativo che chiudevano
  restava *In corso* in *Sfide...*. Ora la speciale viene letta correttamente.

## [0.8.0] - 2026-09-29

Quando un tempo o un tentativo non arriva al sito, l'app può mandare all'organizzatore quello che
gli serve per capire perché.

### Novità

- *Invia dati per l'assistenza...* nel menu: dopo una conferma, l'app invia il registro delle tue
  ultime sessioni, le sue impostazioni, i tempi ancora da inviare, il salvataggio del gioco e un
  rapporto su app e Windows. Lo vede solo l'organizzatore e viene cancellato dopo 30 giorni; la
  chiave di collegamento non viene mai inviata. Una notifica ti dà un codice da comunicare
  all'organizzatore; se l'invio non riesce, il file resta sul Desktop e lo mandi tu.

## [0.7.0] - 2026-09-28

L'app può registrare da sola mentre il gioco è aperto, e nessun tentativo va perso per una
registrazione avviata nel momento sbagliato.

### Novità

- *Registra da solo quando il gioco è aperto*, nelle Impostazioni (spenta di serie): la
  registrazione parte quando apri il gioco e si ferma quando lo chiudi. Se la fermi a mano con il
  gioco aperto, aspetta che tu lo chiuda.
- Un clic sinistro sull'icona dell'app avvia o ferma la registrazione; il menu è sul clic destro.
  Con un tentativo armato o in corso il clic sinistro apre il menu, così un clic non lo ritira.

### Correzioni

- Avviare la registrazione mentre il gioco mostrava ancora il risultato della prova precedente
  consumava un tentativo di una sfida: l'app prendeva quel tempo fermo per una partenza, e la
  ripartenza che seguiva ritirava il tentativo.
- Le prove guidate dopo aver fermato e riavviato la registrazione senza uscire dalla speciale
  arrivavano al sito senza l'immagine della schermata della sessione. Ora l'app osserva quella
  schermata finché è aperta, anche quando non registra; l'immagine resta nella sua memoria finché
  non invia una prova.

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
