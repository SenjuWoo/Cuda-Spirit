<p align="center">
  <img src="docs/images/logo.svg" width="72" height="72" alt="Cuda Spirit mark">
</p>

<h1 align="center">Cuda Spirit</h1>

<p align="center"><strong>A Black Desert recovery, safety, live-data, and decision cockpit.</strong></p>

<p align="center">
  Companion for the part of the game that punishes uncertainty: scattered reward inboxes, binding rules, irreversible item choices, deletion traps, and Pearl Shop offers that look better than they are.<br>
  Unknown or stale facts fail closed instead of becoming confident guesses.
</p>

<p align="center">
  <a href="https://github.com/ShugokiFable/Cuda-Spirit/actions/workflows/windows-release.yml"><img src="https://github.com/ShugokiFable/Cuda-Spirit/actions/workflows/windows-release.yml/badge.svg" alt="Windows Release Build"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-e07030?labelColor=14081f" alt="MIT License"></a>
  <a href="https://github.com/ShugokiFable/Cuda-Spirit/releases/tag/v2.4.2"><img src="https://img.shields.io/badge/release-v2.4.2-f4c45a?labelColor=14081f" alt="v2.4.2"></a>
</p>

<p align="center">
  <a href="https://github.com/ShugokiFable/Cuda-Spirit/releases/latest">Download</a>
  ·
  <a href="#quick-start">Quick start</a>
  ·
  <a href="#safety-boundary">Safety boundary</a>
  ·
  <a href="CHANGELOG.md">Changelog</a>
</p>

## Quick start

Latest release: **[v2.4.2](https://github.com/ShugokiFable/Cuda-Spirit/releases/tag/v2.4.2)** (`Cuda-Spirit-2.4.2-Nexus.zip`).

People downloading that compiled Nexus zip need neither a .NET runtime nor an SDK. Extract it and run `CudaSpirit.exe`.

First ten minutes are in [`COCKPIT_GUIDE.md`](COCKPIT_GUIDE.md): Customize → Recovery Center → Rewards / Item Intel / Pearl Shop Guard → Navigator.

Application data:

```text
%APPDATA%\CudaSpirit\
  settings.json
  cudaspirit.db
  imports\
```

Back up this folder before replacing an older build.

## Safety boundary

Cuda Spirit is a companion and decision-support app. It does **not** send keyboard or mouse input, move or fight for the player, inject DLLs, manipulate packets, read process memory, alter the game client, evade anti-cheat, install `.pak` files, or provide unattended gameplay.

The app cannot inspect the running game. A retirement “safe to delete” result proves that **you** checked each risk, not that deletion is magically reversible.

Cuda Spirit is not affiliated with Pearl Abyss.

## What you get

- **Navigator** — persistent priorities, due dates, pins, completion, custom tasks
- **Recovery Center** — one-click returner rescue, ordered plan, seven-day no-spend shield
- **Reward Claim Center** — coupons, Web Storage, Mail, Black Spirit’s Safe, Challenges, attendance, passes, events, guild rewards
- **Item Intel** and **Transfer Lab** — keep / store / transfer / unknown verdicts; storage, Magnus, maids, Family Inventory, market warehouse
- **Pearl Shop Guard** — deterministic value scoring plus current official notices
- **Farm Route Optimizer** — AP/DP fit, expected value, travel, risk, graph routing
- **Live Data Center** — source health, freshness, imports, search
- **AI Advisor** — source-attributed retrieval (OpenRouter key only if you want it)
- **Ctrl+K** command palette

## Honest status

Shipped as **2.4.2** (`VERSION.txt`). Verified in the 2.4.2 notes:

- Bundled catalog of 77 grind zones + 10 city hubs, version-gated so user imports are not overwritten
- 2026 AP table (100→449) and DP table (203→401+)
- NA/EU PC world-boss rotation with server-timezone conversion
- `tools/CudaSpirit.Smoke` against a live temp SQLite database

Not claimed:

- That the app can see hidden account state or the live client inventory
- That Pearl Shop or market advice is a substitute for the official UI
- A `ci.yml` workflow — the repo’s Actions file is [`windows-release.yml`](.github/workflows/windows-release.yml)

## Build from source

Windows 10 or 11 x64. Microsoft Edge WebView2 for rendered official-page fallback. `.NET 8` SDK (`global.json` rolls forward; the Windows release workflow uses 8.0.423).

```text
publish.bat
```

Publishes a self-contained single-file Windows executable, launches it, verifies that a window appears, and closes the test instance.

Public Nexus package:

```text
BUILD_NEXUS_RELEASE.bat
```

## Credits

Sources for grind, market, and Pearl notes are listed in [`DATA_SOURCES.md`](DATA_SOURCES.md) and [`PRIVACY.md`](PRIVACY.md). See also [`COCKPIT_GUIDE.md`](COCKPIT_GUIDE.md), [`UPGRADE_NOTES.md`](UPGRADE_NOTES.md), and [`VALIDATION_REPORT.md`](VALIDATION_REPORT.md).

Black Desert, Pearl Shop, and Pearl Abyss are trademarks of their owners. This project is unofficial.

## License

[MIT](LICENSE)

## Notes in 2.4.2

- Route Planner and Dashboard farm recommendations return real spots out of the box
- Gear “Next upgrades (bracket-aware)” is actually shown
- Season / Tuvala path support
- Pearl Shop deal-rotation playbook and Central Market tick-resolution card
- DataGrid / BoardRow restyle (Obsidian treatment)

Earlier 2.4.1 overlay hotfix and 2.3 recovery/cockpit work are in [`CHANGELOG.md`](CHANGELOG.md).
