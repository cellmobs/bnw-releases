# BNW releases

Downloads for **BNW**, a local-first peer-to-peer network for sharing AI capabilities (models, MCP tools, agents, search) across people, devices, and organizations, with no central operator. Every node runs the same software; there is no authoritative server.

This repository holds release builds only. Each [release](https://github.com/cellmobs/bnw-releases/releases) has signed macOS and static Linux binaries and their checksums.

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

Windows builds will follow.

## Manual download

| File | Platform |
|---|---|
| `bnw-X.Y.Z-universal-apple-darwin.tar.gz` | macOS, Apple silicon and Intel (signed and notarized) |
| `bnw-X.Y.Z-x86_64-unknown-linux-musl.tar.gz` | Linux x86-64, fully static |
| `bnw-X.Y.Z-aarch64-unknown-linux-musl.tar.gz` | Linux ARM64, fully static |

Check an archive before unpacking it:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

## License

Copyright (c) 2026 Vertical Logic, LLC

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE) or [MIT license](LICENSE-MIT), at your option.
