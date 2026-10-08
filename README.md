# BNW releases

Downloads for **BNW**, a local-first peer-to-peer network for sharing AI capabilities (models, MCP tools, agents, search) across people, devices, and organizations, with no central operator. Every node runs the same software; there is no authoritative server.

This repository holds release builds only. Each [release](https://github.com/cellmobs/bnw-releases/releases) has signed macOS, static Linux, and Windows binaries and their checksums.

## Install

macOS and Linux:

```bash
curl -fsSL https://github.com/cellmobs/bnw-releases/releases/latest/download/install.sh | sh
```

The installer downloads the newest release, checks it against `SHA256SUMS`, installs `bnw` to `~/.local/bin`, and offers to run `bnw setup`. `bnw setup` creates this device's identity, starts the node at login, and opens the web client. Set `BNW_VERSION` to install a specific version, or `BNW_INSTALL_DIR` to install elsewhere.

With Homebrew:

```bash
brew install cellmobs/bnw/bnw
```

Windows, in PowerShell:

```powershell
irm https://github.com/cellmobs/bnw-releases/releases/latest/download/install.ps1 | iex
```

It installs `bnw.exe` to `%LOCALAPPDATA%\Programs\bnw`, adds it to your `PATH`, and offers to run `bnw setup`. With Scoop: `scoop bucket add bnw https://github.com/cellmobs/scoop-bnw`, then `scoop install bnw/bnw`. Windows builds aren't code-signed yet, so SmartScreen may ask before the first run.

The documentation is at [bnw.cellmobs.com/docs](https://bnw.cellmobs.com/docs/).

## Manual download

| File | Platform |
|---|---|
| `bnw-X.Y.Z-universal-apple-darwin.tar.gz` | macOS, Apple silicon and Intel (signed and notarized) |
| `bnw-X.Y.Z-x86_64-unknown-linux-musl.tar.gz` | Linux x86-64, fully static |
| `bnw-X.Y.Z-aarch64-unknown-linux-musl.tar.gz` | Linux ARM64, fully static |
| `bnw-X.Y.Z-x86_64-pc-windows-msvc.zip` | Windows x64 (not code-signed yet) |

Check an archive before unpacking it:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

## Feedback

BNW is early, and we want to hear what breaks and what's missing. [Open an issue](https://github.com/cellmobs/bnw-releases/issues/new/choose) for a bug, an idea, or a question; please leave out secrets and private content, since issues are public. For anything private, including pilots and the iPhone beta, use the [contact form](https://bnw.cellmobs.com/contact).

## License

Copyright (c) 2026 Vertical Logic, LLC

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE) or [MIT license](LICENSE-MIT), at your option.
