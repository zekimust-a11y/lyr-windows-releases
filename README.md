# Lyr for Windows — installer downloads

This repository is the **public mirror** for the Windows installer of [Lyr](https://github.com/zekimust-a11y/lyriqapp) (a music streaming client for LMS, Qobuz, Tidal, etc.). The application source lives in a separate private repository; this repo only exists so testers and end users can download the installer without needing GitHub access.

## Download the latest installer

Grab the most recent Windows 10/11 (x64) build from the nightly release:

**[Lyr Windows installer — latest release](https://github.com/zekimust-a11y/lyr-windows-releases/releases/tag/windows-nightly)**

Direct download (overwritten on every successful build):

```
https://github.com/zekimust-a11y/lyr-windows-releases/releases/download/windows-nightly/Lyr-Setup-1.0.0-x64.exe
```

The installer is a standard NSIS setup. Run it, accept the SmartScreen prompt (the binary isn't code-signed yet), and Lyr will install to `%LOCALAPPDATA%\Programs\Lyr`.

## How this repo gets updated

Each push to `main` on the private `lyriqapp` repo can trigger the `Build Windows Installer` GitHub Actions workflow. On success, the workflow uploads the freshly-built `.exe` (and its `builder-debug.yml`) to the `windows-nightly` release here, overwriting the previous build.

## System requirements

- Windows 10 (64-bit) or newer
- ~500 MB free disk space
- Network access to a Lyr Core server / LMS server on the same LAN (or a public Lyr API)

## Issues / feedback

Issue tracking happens on the private source repo. If you're a tester, send feedback to the same channel you received the link from.
