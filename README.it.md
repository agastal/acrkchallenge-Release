# acrk-tray

[English](README.md) | **Italiano**

acrk-tray è una piccola app per Windows di **ACRK Challenge**, le classifiche e le sfide della
community di **Assetto Corsa Rally** su <https://ch.acrkhotlap.workers.dev>. Sta nell'area di
notifica, legge ogni prova che concludi direttamente dal gioco e manda il tempo al sito:
niente da scrivere, niente screenshot da caricare.

> **Nessun dato personale.** acrk-tray non chiede e-mail, account o password, non legge niente
> del tuo PC (nome del computer, utente Windows, hardware) e non traccia niente. Al sito arrivano
> solo il nome pilota che scegli e i dati delle tue prove: vedi [Privacy e dati](#privacy-e-dati).

> Repository ufficiale di distribuzione: installer, changelog e documentazione. Il codice
> sorgente non è pubblicato qui.

## Download

Scarica il setup dalla pagina [Releases](https://github.com/agastal/acrkchallenge-Release/releases):

- `acrk-tray-<versione>-setup.exe`: l'installer;
- `SHA256SUMS.txt`: impronta SHA-256 dell'installer.

GitHub Releases è l'unico canale di distribuzione ufficiale. Non scaricare l'app da mirror o
da link condivisi altrove.

## Cosa fa

- registra le tue prove mentre guidi, leggendo la memoria condivisa e il salvataggio del gioco;
- manda ogni prova conclusa al sito, dove entra nelle classifiche del time attack e nelle
  sfide aperte;
- finestra **Sfide**: le weekly e gli eventi a più prove aperti in questo momento, con le
  regole di ciascuno; un clic arma il tuo tentativo su una prova prima di guidarla;
- **[Pannello pilota](https://github.com/agastal/acrkchallenge-Release/wiki/Pannello-pilota)** (spento
  di serie): una finestra per il secondo monitor per avviare o fermare una sfida con un pulsante e
  vedere cronometro, distacco dal tuo record, velocità, marcia e le barre acceleratore/freno mentre
  guidi;
- **[Overlay sul gioco](https://github.com/agastal/acrkchallenge-Release/wiki/Pannello-pilota#loverlay-sul-gioco)**
  (spento di serie): un piccolo riquadro trasparente sopra il gioco con lo stato della registrazione,
  il distacco dal tuo record e che fine ha fatto la tua ultima prova;
- un avviso con suono **prima della partenza** quando la prova che si sta caricando non è quella
  della sfida;
- suoni per quello che conta mentre guidi (tempo ricevuto, tentativo chiuso o ritirato), perché
  Windows trattiene le notifiche quando un gioco è a schermo intero;
- scorciatoie globali (avvia, ferma, posiziona l'overlay) che funzionano con il gioco in primo piano;
- avvio all'accesso a Windows, se lo vuoi;
- interfaccia in italiano, inglese, francese, tedesco e spagnolo;
- installa le nuove versioni con un clic, o da sola a gioco chiuso.

## Requisiti

- Windows 10 o 11 a 64 bit;
- Assetto Corsa Rally sullo stesso PC, meglio in modalità finestra senza bordi ("schermo
  intero in finestra"): il perché è in [Privacy e dati](https://github.com/agastal/acrkchallenge-Release/wiki/Privacy-e-dati).

Il setup installa solo per il tuo utente Windows e non chiede i diritti di amministratore;
nient'altro da installare (niente .NET, niente runtime di Visual C++). L'app usa circa 20 MB di
memoria e quasi niente CPU. Spazio su disco, rete e come disinstallarla senza lasciare niente:
[Requisiti e risorse](https://github.com/agastal/acrkchallenge-Release/wiki/Requisiti-e-risorse).

## Per iniziare

1. Esegui il setup e leggi la pagina sui tuoi dati (la stessa qui sotto).
2. Avvia acrk-tray: nell'area di notifica compare il suo cronometro, grigio (può essere
   nascosto sotto `^`).
   La prima volta **Impostazioni** chiede il tuo nome pilota, quello che compare nelle
   classifiche.
3. Dal suo menu scegli **Collega al sito...**. Un avviso mostra un codice:
   l'organizzatore lo approva, e il menu diventa *Collegato come &lt;nome&gt;*.
4. Guida. Ogni prova conclusa arriva al sito da sola.
5. Per una sfida con tentativi limitati apri **Sfide...**, scegli la prova e premi **Avvia il
   mio tentativo** *prima* di guidarla.

La guida completa è nella [wiki](https://github.com/agastal/acrkchallenge-Release/wiki).

## Privacy e dati

**acrk-tray non raccoglie dati personali.** Niente e-mail, account o password, niente sul tuo
PC (nome del computer, utente Windows, hardware), nessun tracciamento d'uso.

Cosa arriva al sito, e solo dopo che hai collegato l'app:

| Cosa | Perché |
| --- | --- |
| il nome pilota che scegli (va bene un soprannome) | è il nome nelle classifiche |
| per ogni prova conclusa: tempo, tempi intermedi, penalità, prova, auto, meteo, ora del giorno, data, versione dell'app | le classifiche |
| una prova conclusa che il gioco non ha salvato: il tempo del cronometro dell'app, prova e auto come le mostra il gioco | l'organizzatore, che la controlla prima che conti |
| **uno screenshot della schermata della sessione del gioco** | verificare la configurazione della prova |

**Screenshot automatici.** Quando avvii una prova dalla schermata della sessione del gioco
("Prove libere", con prova, auto e meteo), acrk-tray cattura un'immagine di quella schermata e
la invia con le prove di quella speciale. Il gioco non salva sempre il meteo di una prova, e
l'immagine permette all'organizzatore di verificare prova, auto, meteo e ora del giorno.
Cattura **solo la finestra di Assetto Corsa Rally, e solo mentre il gioco è in primo piano**,
mai il desktop o altri programmi. Mostra quello che mostra il gioco in quel momento, compreso
il nome del tuo profilo di gioco se visibile. La vede solo l'organizzatore, nella console del
sito; non compare nelle pagine pubbliche. L'app osserva quella schermata anche quando non
registra, e tiene l'immagine solo in memoria finché non invia una prova di quella speciale.
Cattura anche due piccole immagini della finestra di gioco, una sulla linea di partenza prima del
via e una qualche secondo dopo l'arrivo, e le invia con quella prova accanto alla schermata:
mostrano quanta neve o acqua c'è sulla strada, e se è cambiata. Se non ha visto la schermata della
sessione prima del caricamento, l'immagine dopo l'arrivo la sostituisce, intera, con una breve nota
tecnica sul perché mancava.

**Dati per l'assistenza.** Solo se lo scegli dal menu (*Invia dati per l'assistenza...*),
l'app manda all'organizzatore uno zip con il registro e la telemetria delle ultime sessioni, le
sue impostazioni, i tempi da inviare, il salvataggio del gioco e un rapporto su app e Windows.
Mai la chiave di collegamento; lo vede solo l'organizzatore ed è cancellato dopo 30 giorni.

Il sito non registra indirizzi IP. Una volta al giorno l'app chiede a GitHub se esiste una
versione più recente, e ne scarica il setup da GitHub quando la installi; non viene inviato niente
che ti riguardi, e il controllo si può spegnere nelle Impostazioni.

Sul tuo PC:

| Dati | Dove |
| --- | --- |
| impostazioni, chiave di collegamento (protetta con Windows DPAPI) | `%LOCALAPPDATA%\acrk-tray` |
| sessioni registrate: telemetria, copie del salvataggio, screenshot | `%TEMP%\acr-sessions` |

La disinstallazione propone di cancellare entrambe le cartelle. Altro in
[Privacy e dati](https://github.com/agastal/acrkchallenge-Release/wiki/Privacy-e-dati).

## Aggiornamenti

Quando esce una versione più recente, acrk-tray mostra una notifica e aggiunge **Installa
l'aggiornamento X.Y.Z** in cima al menu: un clic scarica il nuovo setup, ne controlla la firma, lo
installa e riavvia l'app, mantenendo impostazioni e collegamento. Nelle Impostazioni puoi lasciare
che lo faccia da sola, a gioco chiuso. Dalla 0.11.0; prima, esegui a mano il nuovo setup. Dettagli
in [Aggiornamenti](https://github.com/agastal/acrkchallenge-Release/wiki/Aggiornamenti); le novità
in [CHANGELOG.it.md](CHANGELOG.it.md).

## Installer non firmato

Il setup non ha una firma digitale, quindi **Edge e Chrome possono bloccarne il download**:
aprili con Ctrl+J e scegli di tenere il file (Edge: **…** > **Mantieni** > **Mostra altro** >
**Mantieni comunque**; Chrome: **Mantieni** o **Scarica comunque**). I passaggi con più
dettagli sono nel [wiki](https://github.com/agastal/acrkchallenge-Release/wiki/Installazione#se-il-browser-blocca-il-download).

Per lo stesso motivo Windows SmartScreen può avvisare la prima volta:
scegli **Ulteriori informazioni**, poi **Esegui comunque**. Nel dubbio confronta il file con
`SHA256SUMS.txt`:

```powershell
Get-FileHash .\acrk-tray-0.5.0-setup.exe -Algorithm SHA256
```

## Avvertenza

Progetto non ufficiale della community. acrk-tray e ACRK Challenge non sono affiliati,
approvati o associati ad Assetto Corsa Rally o ai suoi sviluppatori (Supernova Games Studios,
Kunos Simulazioni) o al suo editore (505 Games). È un'iniziativa di appassionati, portata
avanti dalla community. Tutti i marchi appartengono ai rispettivi proprietari.
