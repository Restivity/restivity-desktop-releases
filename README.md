# Restivity desktop — releases

This repository holds **only the installers** of the Restivity desktop app (macOS `.dmg` / `.zip`,
Windows `.exe`) and the `latest*.yml` feed files that `electron-updater` reads to find a new
version. It is public because an installed app must be able to check for updates without a token.

The source code, its history, tests and issues live in a **private** repository and are not
published here. Nothing in an installer is a secret: the app talks only to https://restivity.ai
with the signed-in person's own session.

## Install

Download the latest release from the Releases tab:

- **macOS (Apple Silicon)**: `Restivity-<version>-mac-arm64.dmg`
- **macOS (Intel)**: `Restivity-<version>-mac-x64.dmg`
- **Windows (x64)**: `Restivity-<version>-win-x64.exe`

Until the app is signed with an Apple Developer ID, macOS Gatekeeper shows «Restivity cannot be
opened»: open System Settings → Privacy & Security and choose **Open Anyway** at the bottom.
Windows SmartScreen may warn on the first run of an unsigned installer: choose «More info» → «Run
anyway».

## Updates

The app checks this repository's Releases ten seconds after launch and every six hours, downloads
a newer version in the background and installs it when the app quits. On macOS an update is
applied only when the app is signed with a Developer ID; until then, download the new `.dmg`
from here.
