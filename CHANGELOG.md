# Changelog

**English** | [Italiano](CHANGELOG.it.md)

Every release of acrk-tray, newest first. Versions follow `MAJOR.MINOR.PATCH`; the setup of
each one is on the [Releases](https://github.com/agastal/acrkchallenge-Release/releases) page.

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
