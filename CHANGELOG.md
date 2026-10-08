# Changelog

**English** | [Italiano](CHANGELOG.it.md)

Every release of acrk-tray, newest first. Versions follow `MAJOR.MINOR.PATCH`; the setup of
each one is on the [Releases](https://github.com/agastal/acrkchallenge-Release/releases) page.

## [0.13.1] - 2026-10-08

A double click on the icon no longer stops the recording it has just started.

### Fixed

- A double click on the tray icon used to start the recording and stop it at once, so the stages
  driven afterwards were not recorded. A second click within a second of the first is now ignored:
  one click starts the recording, the next one (later) stops it.
- When you send diagnostics, they now say what stopped each recording (the icon, the menu, a
  shortcut, the driver panel, the game closing, the end of an attempt), so the organiser finds the
  cause sooner.

## [0.13.0] - 2026-10-05

A time the game does not save is no longer lost: it reaches the site and waits for the organiser.

### New

- Now and then the game finishes a stage without saving the time. The app now sends it anyway, with the
  time on its clock and the pictures of the road: you get "Run waiting for validation", the overlay says
  "sent · waiting for validation", and the organiser checks stage, car, weather and penalty before it
  counts. A challenge attempt waits for it instead of being lost, and the recording started for the
  attempt stops by itself as after any other finish.
- With every time the app also sends the stage and car names the game shows, so the site recognises them
  when a time arrives that the game did not save.

### Changed

- The pictures of the road at the start and after the finish are sharper (the same size as the session
  screen), so rain and snow on the road are easier to judge.
- On a very wide screen or three monitors the pictures keep only the middle part, the screen in front of you.
## [0.12.0] - 2026-10-03

Two small pictures of the road with every time, the mouse pointer out of the way, and the recording that
stops with the game.

### New

- With every time the app now sends two small pictures of the game window: the road at the start line,
  taken before the start once the engine is running, and the road a few seconds after the finish, while
  you slow down after the line. The organiser sees how much snow or water is on the road, and whether it
  changed during the stage.
- *Move the mouse pointer to a corner when a run starts* in Settings (off by default): when the clock
  starts, the pointer goes to the bottom right corner of the game's screen instead of staying in the
  middle of the road.

### Changed

- When the game's session screen was not seen, the picture sent in its place is now the one after the
  finish, whole: it shows the road, the weather, the time of day and your time. The one at the start line
  could catch the game's loading screen.
- Closing the game now stops *Start recording times* too when you started it by hand. A time that has
  just finished is still waited for; with a challenge attempt armed, the recording stays on for when you
  open the game again.

### Fixed

- "Run not saved by the game" could appear right at the finish of a run the game did save.
- After closing the game, "Game found" could come back a few times in a row.

## [0.11.1] - 2026-10-02

Times driven many times in a row on the same stage reach the site again.

### Fixed

- After several runs on a stage without going back to the menu, the times were refused by the site
  ("game_stage is missing") and counted nowhere, not even in a challenge's attempt. The app now reads
  the stage of every run, however many there are.

## [0.11.0] - 2026-10-02

Updates install from the app: one click, or by themselves with the game closed.

### New

- *Install update X.Y.Z* in the menu (it was *Download update*): the app downloads the new version,
  checks its signature, installs it and starts again in a few seconds, with settings and connection
  as they were. It waits if the game is open, times are being recorded, an attempt is on or a time
  is still to be sent, and says so.
- *Install them by themselves, with the game closed* in Settings, under the daily check (off by
  default): the app updates itself once nothing is going on.
- After an update a notice says which version you have now; a click on it opens what changed.
- Every setup is signed: the app installs only a setup made by the organiser, never a damaged or
  altered one.

### Changed

- This is the last update you install by hand: from 0.11.0 on, the app does it.

## [0.10.0] - 2026-10-02

An overlay on the game with the gap to your record, and night stages told apart by their weather.

### New

- *Game overlay* in the menu: a small see-through box over the game with what its HUD lacks. A dot
  says whether times are being recorded (yellow off, green ready, red during a run); beside it the
  challenge attempt or the condition it wants, the gap to your record with its trend, your record
  and the finish time if the gap holds, and what became of your last run (sent with its place on
  the board, waiting to be sent, not sent, attempt valid or retired). It shows only with a stage
  loaded and the game on screen, lets clicks through to the game, and stays out of screenshots and
  recordings.
- *Place the overlay* (menu, or Ctrl+Shift+F8, which you can change in Settings): drag it where you
  want it, then double-click or press the shortcut again to fix it. While you place it, its dot
  starts and stops recording times.
- The overlay warns you when the stage you loaded is not the challenge's.
- *Run not saved by the game*: a notice when the game keeps no result of a finished run, so you know
  that time did not reach the site.

### Changed

- Night now goes with the weather: *night, dry*, *night, wet* and *night, snow / ice* are separate
  conditions, in the driver panel and the Challenges window as on the site.

### Fixed

- A new best time the game wrote only among its best times, without a result of its own, was not
  sent: it now reaches the site.

## [0.9.0] - 2026-10-01

A driver panel for a second monitor, with the gap to your record while you drive, and a picture
with every time even when the app does not see the session screen.

### New

- *Driver panel...* in the menu: a wide, short window for a second monitor. One button starts and
  stops recording times, or arms the attempt of the challenge you pick in its list; beside it the
  stage clock, speed and gear, the throttle and brake bars, and the condition the challenge wants.
  It remembers where you put it, and it can stay above other windows (Settings).
- The panel shows how far ahead (green) or behind (red) you are against your own best time on the
  same stage, car and condition, metre by metre, and holds the final gap at the finish. The first
  run you finish with the panel open becomes the reference; every faster one replaces it. These
  traces stay on your PC.
- When you drive a stage of a challenge without starting the attempt, a notice tells you the time
  counted only for the time attack.

### Changed

- *Start/Stop session* is now *Start/Stop recording times*, so it is not mistaken for the game's own
  START SESSION.
- When the app does not see the session screen before the stage (another game mode, the app opened
  in the stage), it takes one picture of the game window at the start line instead, before you set
  off, and tells the organiser why the session screen was missing.
- The session screen is recognised on more screen shapes (16:10, ultrawide) and when the game is
  behind another window that does not cover it, such as the driver panel.
- *Open sessions folder* left the menu: the wiki says where the folder is, and *Send diagnostics to
  the organiser...* sends what is needed.

### Fixed

- Long shortcut names no longer get cut in Settings.

## [0.8.1] - 2026-09-30

A fix for times that reached the site without their stage.

### Fixed

- Some times reached the site with a wrong stage name, so the site could not place them: they
  waited for the organiser, and an attempt they closed stayed *Running* in *Challenges...*
  in the meantime. The stage is now read right.

## [0.8.0] - 2026-09-29

When a time or an attempt does not reach the site, the app can send the organiser what it needs
to find out why.

### New

- *Send diagnostics to the organiser...* in the menu: after a confirmation, the app sends the log
  of your latest sessions, its settings, the times still waiting to be sent, the game's save file
  and a report on the app and Windows. Only the organiser sees it, and it is deleted after 30 days;
  the connection key is never sent. A notification gives you a code to tell the organiser; if
  sending fails, the file is left on your Desktop for you to send.

## [0.7.0] - 2026-09-28

The app can record by itself while the game is open, and no attempt is lost to a recording
started at the wrong moment.

### New

- *Record by itself while the game is open*, in Settings (off by default): the recording starts
  when you open the game and stops when you close it. Stopped by hand with the game open, it waits
  until you close the game.
- A left click on the app's icon starts or stops the recording; the menu is on the right click.
  While an attempt is armed or running, the left click opens the menu, so that a click does not
  retire it.

### Fixed

- Starting the recording while the game still showed the result of the previous run spent an
  attempt of a challenge: the app took that frozen time for a start, and the restart that followed
  retired the attempt.
- Runs driven after stopping and starting the recording without leaving the stage reached the
  site without the picture of the session screen. The app now watches for that screen while it is
  open, also when it is not recording; the picture stays in its memory until a run is sent.

## [0.6.2] - 2026-09-27

The recorded sessions no longer fill the disk.

### Changed

- The recorded sessions (about 85 MB per hour of driving) are cleaned up by the app: at the start
  of each session it deletes the ones older than 30 days, then the oldest until the rest fits in
  500 MB.

## [0.6.1] - 2026-09-27

A restart no longer loses the next attempt of a challenge with more than one.

### Fixed

- On a challenge with more than one attempt, restarting the stage retired the attempt and
  stopped the recording, so the run you drove next was never seen. Now the app arms the next
  attempt at once and keeps recording: the run that starts after the restart is that attempt,
  and a notification says so (*restarted. Attempt 2 of 3 is armed*).

### Changed

- The Challenges window is narrower and taller.

## [0.6.0] - 2026-09-27

Sounds and warnings for what happens while you drive, and more control over how the app starts.

### New

- A warning with a sound **before the start** when the game is loading a different stage from
  the challenge's: go back to the menu, or the attempt is retired.
- Sounds for the outcome of each run (time received, attempt closed, retirement, warning,
  error), since Windows holds notifications back while the game is full screen.
- Intermediate times are read from the game and sent with each run.
- **Settings**: "Start acrk-tray when I sign in to Windows" and "Check for new versions once a
  day", both can be switched off.

### Changed

- Closing the game during a stage now retires the attempt (reason "closed"), and the session
  waits for the game to start again.
- The icon in the notification area is the app's stopwatch in grey while idle.
- The mark shortcut is gone: only start and stop remain.
- The Challenges window explains that for a time attack you start a session from the menu, and
  every run you drive then counts.
- Start with Windows now uses the same setting as the app, so the setup and Settings agree and
  the app never starts twice.

## [0.5.0] - 2026-09-26

First public release.

### New

- Installer: per-user setup, no administrator rights, Start menu entry, optional start with
  Windows; the page on your data is shown before installing. Uninstalling offers to delete
  settings and recorded sessions.
- Update check: once a day the app asks GitHub for the latest release and, when there is a
  newer one, says so with a notification and a **Download update** menu item. Updating stays
  manual.
- New **Challenges** window in the site's look: one card per stage with conditions, cars,
  closing date, attempts and a coloured status; light or dark following Windows.
  Double-click a ready stage to start the attempt.
- The app's version is shown in its menu and in the file properties.

### Already in the app

- Records stages from shared memory and save file, and sends each finished stage to ACR
  Challenge once the PC is connected to the site; results wait in an outbox when offline.
- Challenges with limited attempts: arming, start, restart and quitting a stage reported to
  the site; the recording started by an attempt stops when the attempt ends.
- Screenshot of the game's session screen sent with the runs, to check weather and setup.
- Global shortcuts with sounds, interface in five languages.
