---
title: Install and update
description: How to install and keep SketchCraft up to date on macOS, Windows, and Linux.
sidebar:
  order: 2
---

:::note[Third-Party Application]
SketchCraft is an independent open-source modeler maintained by Jason Sutter and the SketchCraft contributors.
:::

## Downloads

Every build is on the [latest release](https://github.com/jasonsutter87/sketchcraft/releases/latest) page. To update, download the newest release and install it over the old one. Your models are `.sketchcraft` files and stay where you saved them.

## macOS

1. Download the `.dmg` from the latest release.
2. Open it and drag **SketchCraft.app** to your `Applications` folder.

macOS builds aren't notarized yet. If macOS says the app "can't be opened", open **System Settings › Privacy & Security**, scroll to the message about SketchCraft, and click **Open Anyway**. Or run `xattr -dr com.apple.quarantine /Applications/SketchCraft.app` in a terminal.

## Windows

Download the `.msi` installer or the setup `.exe` from the latest release. The Windows downloads aren't code-signed yet. If SmartScreen warns you, choose **More info**, then **Run anyway**.

## Linux

The release includes an `.AppImage` and a `.deb` for x86_64.

- **AppImage**: `chmod +x SketchCraft_*.AppImage`, then run it.
- **Debian and Ubuntu**: `sudo apt install ./SketchCraft_*.deb`

## Headless CLI

The engine also ships on its own as `sketchcraft`, with no window. It runs scripts, renders PNGs and serves the MCP server for AI agents. Download `sketchcraft-cli-<platform>.zip` from the release, unzip it, and put `sketchcraft` on your `PATH`.

```bash
sketchcraft run house.jsonl --save house.sketchcraft
```

## Optional: DWG and IFC files

SketchCraft reads and writes DXF on its own. Two formats use a free helper you install once:

- **DWG (AutoCAD)**: install [LibreDWG](https://www.gnu.org/software/libredwg/) (on macOS: `brew install libredwg`) or the free ODA File Converter. SketchCraft finds either automatically.
- **IFC (Revit, ArchiCAD)**: SketchCraft uses [IfcOpenShell](https://ifcopenshell.org). If it isn't installed, opening an IFC file shows the two Terminal commands that set it up.

## Build from source

You need Rust (stable) and Node.js 22.

```bash
git clone https://github.com/jasonsutter87/sketchcraft
cd sketchcraft
cargo build --release -p sketchcraft-core      # engine and CLI
cd app && npm ci && npm run tauri build         # desktop app
```

On Linux, install the WebKit development packages first: `libwebkit2gtk-4.1-dev`, `libappindicator3-dev`, `librsvg2-dev` and `patchelf`.
