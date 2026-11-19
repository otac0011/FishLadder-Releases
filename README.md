# FishLadder

**Impedance matching for people who have never designed a matching network.**

> **Releases-only repository.** This repo hosts the prebuilt Windows installer for FishLadder. The source code is proprietary and lives in a private repository.

## Install

**Recommended: [Retinue Launcher](https://github.com/otac0011/RetinueLauncher-Releases).** Install the launcher once; its **Available tools** tab installs and updates this tool and the other PCB tools (CastGuidance, FishLadder, EyeOpener Lite) from their official release pages. Nothing is installed until you choose it, and each tool's own installer shows its license.

**Or download the installer directly:**

→ **[Download the latest release](https://github.com/otac0011/FishLadder-Releases/releases/latest)** (Windows installer, about 60 MB)

Run `FishLadder-Setup-<version>.exe`. The installer shows the End User License Agreement, which you must accept to install. It installs to `Program Files\FishLadder` (it asks for administrator rights), adds a Start Menu entry and an uninstaller (Settings → Apps). The app is self-contained: no separate .NET install is needed.

### Windows SmartScreen

The installer is not code-signed yet, so Windows may show **"Windows protected your PC"** the first time you run it. Click **More info → Run anyway**. You can check the download against the SHA-256 digest shown for the asset on the release page.

### System requirements

- Windows 10 or 11, 64-bit (x64)
- About 250 MB of disk space
- A CUDA or OpenCL graphics card is optional (it speeds up large EM solves)

## What it does

A Windows desktop tool for designing RF impedance-matching networks (lumped L/C ladders, PCB trace segments, open and shorted stubs, tapers and quarter-wave transformers) against a measured or vendor-supplied Touchstone load such as an antenna:

1. **Load**: the `.s1p`/`.s2p` of the thing you are matching, the band and the target.
2. **Build**: a ladder of blocks between the source and the load.
3. **Search**: let the optimizer tune parts and copper to stocked values.
4. **Results**: ranked buildable designs with Monte Carlo yield, worst-case corners and a live Explorer with a Smith chart.

It also checks a design with its own EM field solver and exports BOM, `.s2p`, DXF, ODB++ and stackup files. A command-line tool, `fishladder.exe`, is installed beside the app.

## License

Distributed under a **proprietary End User License Agreement**; see [`LICENSE`](LICENSE). Open-source components it ships are listed with their licenses in [`THIRD-PARTY-NOTICES.txt`](THIRD-PARTY-NOTICES.txt).

**Summary** (the file is authoritative):

- ✅ Install and use on any device you own: personal, educational, or commercial
- ✅ Share **unmodified** copies (no fee)
- ❌ Sell, sublicense, or rent
- ❌ Modify, reverse-engineer, or create derivative works
- ❌ Distribute in modified form
- ❌ Remove or obscure copyright notices

This is **not** open-source software. Source code is held privately.

## Reporting a bug

[Open an issue](https://github.com/otac0011/FishLadder-Releases/issues). Please include the version (Help → About, or `fishladder --version`), what you were doing, and a screenshot if applicable.

## Disclaimer

PCB designs and electronic circuits can pose safety and reliability risks. All values, recommendations, and outputs produced by FishLadder are **starting points for engineering judgment only**, not a substitute for qualified engineering review.

---

© 2026 FishLadder Developer. All rights reserved.
