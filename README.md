[English](README.md) | [日本語](README.ja.md)

# SendBlocker

A macOS menu-bar utility that **swaps Return and Shift+Return** — only in the apps you choose.

It keeps chat apps from sending a message when you meant to start a new line. Return inserts a line break, and Shift+Return sends.

**➡️ [Download the latest release](https://github.com/EVAtiter/SendBlocker-release/releases/latest)**

---

## How keys are converted

| You press | The target app receives |
| --- | --- |
| Return | Shift+Return (new line) |
| Shift+Return | Return (send) |
| Command / Option / Control + Return | Unchanged (not converted) |

Keys are converted only while a target app is in front. In every other app, Return works as usual.

---

## Installation

### Homebrew

```bash
brew install --cask EVAtiter/tap/sendblocker
```

If Homebrew 7 or later reports an "untrusted tap", trust sendblocker first with the command below, then install again.

```bash
brew trust --cask evatiter/tap/sendblocker
```

### Manual

1. Download `SendBlocker-x.x.x.zip` from [Releases](https://github.com/EVAtiter/SendBlocker-release/releases/latest)
2. Unzip it and move `SendBlocker.app` to your Applications folder
3. Launch it — a ↩ icon appears in the menu bar (the app does not appear in the Dock)

---

## Usage

1. From the ↩ icon in the menu bar, open **Target Apps → Add from Running Apps…** and **double-click** the app you want to add (only running apps are listed)
2. Choose **Enabled** in the menu
3. The first time you enable it, you will be asked for Accessibility permission. Click Open System Settings, turn SendBlocker on in **System Settings → Privacy & Security → Accessibility**, then choose **Enabled** again

To remove a target app, choose the item with **✕** next to its name in the Target Apps list.

---

## Features

- **Key swap** — Return ↔ Shift+Return (combinations with Command / Option / Control are not converted)
- **Per-app targeting** — works only in the apps you register (nothing is converted when no app is registered)
- **Enable / disable** — from Enabled in the menu. If target apps are registered, it is enabled automatically at launch
- **Open at Login** — stays in sync with Login Items in System Settings
- **Hide Menu Bar Icon** — hides the menu bar icon; conversion keeps working. To bring the icon back, launch SendBlocker again from the Finder
- **English / Japanese** — follows your system language

---

## Notes

- If you turn off Accessibility permission while SendBlocker is running, key input may stop responding for a few seconds to about 10 seconds (it then recovers, and Enabled is unchecked in the menu). Quit SendBlocker before turning the permission off
- Turning the permission back on does not resume conversion automatically. Choose Enabled in the menu again

---

## Privacy

SendBlocker makes no network connections and does not record or store the keys you type. The only thing it saves is your list of target apps, in
`~/Library/Application Support/SendBlocker/settings.json`.

---

## Uninstall

- Installed with Homebrew: `brew uninstall --cask sendblocker` (to remove settings too: `brew uninstall --zap --cask sendblocker`)
- Installed manually: quit SendBlocker and move `SendBlocker.app` to the Trash. To remove settings too, delete `~/Library/Application Support/SendBlocker/`

---

## System requirements

macOS 13.0 Ventura or later / Apple Silicon (arm64) only / Notarized by Apple

---

Copyright © 2026 EVA Titer. All rights reserved.
