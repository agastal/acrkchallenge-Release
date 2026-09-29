# acrk-tray

**English** | [Italiano](README.it.md)

acrk-tray is a small Windows app for **ACRK Challenge**, the community leaderboards and
challenges for **Assetto Corsa Rally** at <https://ch.acrkhotlap.workers.dev>. It sits in the
notification area, reads each stage you finish straight from the game and sends the time to
the site: no typing, no screenshots to upload.

> **No personal data.** acrk-tray asks for no e-mail, account or password, reads nothing about
> your PC (computer name, Windows user, hardware) and tracks nothing. Only the driver name you
> choose and the data of your runs reach the site: see [Privacy and data](#privacy-and-data).

> Official binary-distribution repository: installer, changelog and documentation. The
> source code is not published here.

## Download

Get the setup from the [Releases](https://github.com/agastal/acrkchallenge-Release/releases)
page:

- `acrk-tray-<version>-setup.exe`: the installer;
- `SHA256SUMS.txt`: SHA-256 fingerprint of the installer.

GitHub Releases is the only official distribution channel. Do not download the app from
mirrors or links shared elsewhere.

## What it does

- records your stages while you drive, reading the game's shared memory and save file;
- sends each finished stage to the site, where it enters the time attack boards and the
  open challenges;
- **Challenges** window: the weeklies and multi-stage events open right now, with the rules
  of each; one click arms your attempt on a stage before you drive it;
- a warning with a sound **before the start** when the stage loading is not the challenge's;
- sounds for what matters while you drive (time received, attempt closed or retired), since
  Windows holds notifications back while a game is full screen;
- two global shortcuts (start, stop) that work with the game in front;
- optional start when you sign in to Windows;
- English, Italian, French, German and Spanish interface;
- tells you when a new version is out.

## Requirements

- Windows 10 or 11, 64-bit;
- Assetto Corsa Rally on the same PC, best in borderless window mode ("full screen
  windowed"): see [Privacy and data](https://github.com/agastal/acrkchallenge-Release/wiki/Privacy-and-data) for why.

The setup installs for your Windows user only and does not ask for administrator rights; nothing
else to install (no .NET, no Visual C++ runtime). The app uses about 20 MB of memory and next to
no CPU. Disk space, network and how to uninstall without leaving anything behind:
[Requirements and resources](https://github.com/agastal/acrkchallenge-Release/wiki/Requirements-and-resources).

## Getting started

1. Run the setup and read the page on your data (the same as below).
2. Start acrk-tray: its stopwatch appears, grey, in the notification area (it may be hidden
   under `^`).
   The first time, **Settings** asks for your driver name, the one shown on the
   leaderboards.
3. From its menu choose **Connect to the site...**. A balloon shows a code: the
   organiser approves it, and the menu then reads *Connected as &lt;name&gt;*.
4. Drive. Each finished stage reaches the site by itself.
5. For a challenge with limited attempts, open **Challenges...**, pick the stage and press
   **Start my attempt** *before* driving it.

The full guide is in the [wiki](https://github.com/agastal/acrkchallenge-Release/wiki).

## Privacy and data

**acrk-tray does not collect personal data.** No e-mail, account or password, nothing
about your PC (computer name, Windows user, hardware), no usage tracking.

What goes to the site, and only after you connect the app:

| What | Why |
| --- | --- |
| the driver name you choose (a nickname is fine) | it is the name on the leaderboards |
| for each finished stage: time, intermediate times, penalty, stage, car, weather, time of day, date, app version | the leaderboards |
| **a screenshot of the game's session screen** | checking the setup of the run |

**Automatic screenshots.** When you start a stage from the game's session screen (the one
showing stage, car and weather before the stage loads), acrk-tray takes a picture of that
screen and sends it with the runs of that stage. The game does not always save the weather
of a run, and the picture lets the organiser check stage, car, weather and time of day.
It captures **only the Assetto Corsa Rally window, only while the game is in front**, never
the desktop or other programs. It shows what the game shows at that moment, including
your in-game profile name if visible. Only the organiser sees it, in the site's console;
it is not shown on public pages. The app watches for that screen also when it is not
recording, keeping the picture in memory only until a run of that stage is sent.

**Diagnostics.** Only if you choose it from the menu (*Send diagnostics to the organiser...*),
the app sends the organiser a zip with the log and telemetry of your latest sessions, its
settings, the times waiting to be sent, the game's save file and a report on the app and
Windows. Never the connection key; only the organiser sees it, and it is deleted after 30 days.

The site does not record IP addresses. Once a day the app asks GitHub whether a newer
version exists; nothing about you is sent, and Settings can turn the check off.

On your PC:

| Data | Where |
| --- | --- |
| settings, connection key (protected with Windows DPAPI) | `%LOCALAPPDATA%\acrk-tray` |
| recorded sessions: telemetry, copies of the save file, screenshots | `%TEMP%\acr-sessions` |

Uninstalling offers to delete both folders. More in
[Privacy and data](https://github.com/agastal/acrkchallenge-Release/wiki/Privacy-and-data).

## Updates

When a newer version is out, acrk-tray shows a notification and adds **Download update
X.Y.Z...** at the top of its menu. The app never updates itself: download the new setup
from the release page and run it. It closes the running app, replaces it and keeps your
settings and connection. See [CHANGELOG.md](CHANGELOG.md) for what changed.

## Unsigned installer

The setup is not code-signed, so **Edge and Chrome may block the download**: open the
downloads with Ctrl+J and choose to keep the file (Edge: **…** > **Keep** > **Show more** >
**Keep anyway**; Chrome: **Keep** or **Download anyway**). The steps in more detail are in the
[wiki](https://github.com/agastal/acrkchallenge-Release/wiki/Installation#if-the-browser-blocks-the-download).

For the same reason Windows SmartScreen may warn the first time: choose
**More info**, then **Run anyway**. Check the file against `SHA256SUMS.txt` if in doubt:

```powershell
Get-FileHash .\acrk-tray-0.5.0-setup.exe -Algorithm SHA256
```

## Disclaimer

Unofficial community project. acrk-tray and ACRK Challenge are not affiliated with, endorsed
by, or associated with Assetto Corsa Rally or its developers (Supernova Games Studios,
Kunos Simulazioni) or its publisher (505 Games). This is a fan-run, community effort. All
trademarks are the property of their respective owners.
