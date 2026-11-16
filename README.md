# SoundLimit

A volume limiter for Windows that lives in your system tray and keeps the sound coming out of your speakers under the limit you set — no matter how loud whatever you're watching or playing gets.

If a movie scene suddenly explodes or a video starts clipping, SoundLimit turns the master volume down just enough to stay at your limit, then brings it back up slowly when things go quiet. The volume is never lowered when the audio is already below the limit, and it never goes below what you actually need.

## Features

- **System tray icon** — blue when active, grey when off. Left click or right click opens the menu.
- **Adjustable limit** — vertical slider from 5% to 100%, with a live loudness bar next to it showing exactly what your speakers are outputting (green below your limit, red at the limit, grey for what was trimmed).
- **Recovery speed** — how fast the volume comes back up after a loud passage: Fast, Normal, or Slow.
- **Respects your volume** — anything you set by hand becomes the new ceiling; the limiter will never push volume above what you chose.
- **Smart on/off** — when you re-enable it, it restores the volume it had lowered (unless you changed it yourself while it was off).
- **Menu in Spanish or English** — Settings → Language, defaults to your Windows language.
- **Start with Windows** — optional, toggled from the menu.

## Requirements

- **Windows 10 or 11, 64-bit.**
- **.NET Desktop Runtime 10.x** — free from Microsoft. The installer checks for it first and, if it's missing, shows a page explaining exactly what to download so you can retry without closing the installer.
- Nothing else to install. The only third-party library bundled in the app is [NAudio](https://github.com/naudio/NAudio) (MIT license), used to read and set the Windows master volume.

## Getting started

1. Download the latest `SoundLimit-x.y.z-setup.exe` from the [Releases](../../releases) page and run it.
2. The installer asks for no admin rights, installs only for your user, and leaves a Start Menu shortcut (desktop shortcut is optional). Tick "Run SoundLimit" at the end, or launch it later from the Start Menu.
3. A blue icon appears in the system tray (check the hidden-icons area if you don't see it).

## How to use it

Click the tray icon to open the menu and drag the slider to the limit you want. That's it — leave it running in the background.

To stop limiting temporarily, open the menu and turn the limiter off (icon turns grey). To quit, choose Exit.

Want it always running? Enable **Start with Windows** in the menu (Settings).

## Updating and uninstalling

- Running a newer setup upgrades your existing install in place and keeps your settings.
- Uninstall from Windows (Settings → Apps); your saved settings in `%APPDATA%\SoundLimit` survive, in case you reinstall later.

## Good to know

- It works on the default output device, whatever app is playing sound.
- It limits the master output volume; it does not process or compress the audio itself.
- Everything runs locally: no internet connection, no accounts, no telemetry.
