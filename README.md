# amux releases

[English](README.md) | [简体中文](README.zh-CN.md)

Official binary downloads for [amux](https://amuxos.com/).
This repository contains release assets and installation instructions. The
application source is maintained separately in `amuxos/amux`.

## Install

Install and authenticate Codex, Claude, or Pi first, then download the installer:

```sh
curl -fsSL https://github.com/amuxos/amux-releases/releases/latest/download/install.sh -o /tmp/amux-install.sh
bash /tmp/amux-install.sh --runtime codex
```

Use `--runtime claude` or `--runtime pi` to select another installed agent.
Add `--feishu` for optional bot setup. Native agent credentials stay managed by
the agent. Use `--version vX.Y.Z` to select a specific release.

Supported packages: macOS (Apple Silicon and Intel), Linux (x86-64 and ARM64),
Windows (x86-64 via Setup.exe).
Claude also requires Node.js 22 or newer.

### Windows

1. Install and authenticate Codex, Claude, or Pi first.
2. Download `amux_<version>_windows_amd64.tar.gz` and extract it.
3. From the extracted folder (Administrator), run:

```text
Setup.exe --runtime codex
```

Phase 1 Setup requires a successful Feishu (飞书) QR/browser bind and registers
a Windows Service that starts the hub on boot. There is no App ID/Secret manual
fallback in phase 1. You can also download the standalone
`amux_<version>_windows_amd64_Setup.exe` asset; it must still sit next to the
extracted `amux.exe` / `amuxd.exe` / `amuxlet.exe` siblings.


Local Expert authoring requires a separately configured Agent Pack Contract
runtime, which is not included in these packages. Without it, installation and
updates succeed with a warning that local Expert authoring is degraded.

## Update

```sh
amux update --restart
```

Updates preserve configuration and user data. Release assets include SHA256
checksums and a `latest.json` platform manifest. Versioned assets are immutable;
the latest-release URL selects the current stable version.

## Releases

[Download a release](https://github.com/amuxos/amux-releases/releases).
Builds and tests run in the source repository. Only installation scripts,
compiled packages, checksums, and release metadata are published here.
License and third-party notices are included in each package.
