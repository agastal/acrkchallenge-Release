# Changelog

**English** | [Italiano](CHANGELOG.it.md)

Every release of acrk-tray, newest first. Versions follow `MAJOR.MINOR.PATCH`; the setup of
each one is on the [Releases](https://github.com/agastal/acrkchallenge-Release/releases) page.

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
