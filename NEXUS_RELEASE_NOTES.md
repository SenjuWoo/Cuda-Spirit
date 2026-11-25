# Cuda Spirit 2.4.3

- Built on .NET 10 LTS (.NET 8 support ended); still one self-contained exe, nothing to install.
- Farm Route Optimizer: Start and Destination now show place names instead of an internal type name.
- The sidebar shows the real version; boss rows without a note lose the stray separator.
- Microsoft.Data.Sqlite 11 and WebView2 1.0.4314.35.

2.4.2 added the bundled 77-zone grind catalog, 2026 AP/DP brackets, the real NA/EU world-boss rotation, season-character support and the Pearl Shop deal-rotation playbook. The full history is in CHANGELOG.md in the source repository.

# Cuda Spirit 2.4.1 — Obsidian UI

This is the major visual rework. The previous rounded, pill-heavy launcher appearance has been replaced by a sharper high-end desktop cockpit.

## Visual changes

- Matte OLED surfaces with restrained highlights
- Crisp 3–4 px corners across cards and controls
- Rectangular status labels instead of capsules
- Square selection controls and color swatches
- Underline tabs instead of rounded tab buttons
- Flat navigation with a narrow active accent rail
- Geometric Cuda Spirit mark instead of circular ornamentation
- Reduced shadows, glow, saturation, and page-motion distance
- Reworked main title bar, command palette, sidebar, HUD, and advisor overlay

## Installation behavior

The public Nexus package is the self-contained EXE produced by `BUILD_NEXUS_RELEASE.bat`; users of that compiled package need no SDK or runtime. Building from source needs any stable .NET 10 or newer SDK (`global.json` rolls forward to newer majors).


## V2.4.1 overlay hotfix

Transparent overlay icons now use vector paths instead of font glyphs or emoji, with device-pixel rounding and layered-window-safe grayscale rendering.
