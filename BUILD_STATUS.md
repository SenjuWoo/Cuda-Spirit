# Build status — Cuda Spirit 2.4.3

## Source status

The complete source passes the bundled structural, XAML, resource, navigation, SQLite, prior compiler-regression, Obsidian geometry, and packaging validators.

## Windows compilation

The application is a Windows WPF project. `publish.bat` and the GitHub Actions workflow perform the authoritative Windows compile with warnings treated as errors and require a real main window during the smoke test.

## SDK behavior

The projects target .NET 10. Local builds use any stable .NET 10 or newer SDK already installed (`global.json` pins 10.0.100 with `rollForward: latestMajor`); `publish.bat` and `tools/Build-NexusRelease.ps1` refuse older SDKs with a clear message. A compiled self-contained Nexus release created by `BUILD_NEXUS_RELEASE.bat` requires no .NET runtime or SDK for end users.


## V2.4.1 overlay hotfix

Transparent overlay icons now use vector paths instead of font glyphs or emoji, with device-pixel rounding and layered-window-safe grayscale rendering.
