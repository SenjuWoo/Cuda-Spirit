# Cuda Spirit validation report

## 2.4.3 automated source validation

`python tools/validate_source.py` on a clean checkout of the 2.4.3 source:

```text
PASS: Parsed 28 XAML/project files.
PASS: Parsed 3 JSON files.
PASS: Checked XAML classes and event wiring.
PASS: Checked 755 resource references against 80 declared keys.
PASS: Verified 2.4.3 release metadata and 19 shell navigation destinations.
PASS: Checked the Pearl Shop CS0165 definite-assignment regression.
PASS: Checked all prior Windows compiler regressions: Thickness arity and System.IO resolution.
PASS: Checked Obsidian UI geometry: no decorative ellipses, no radii above 4, and crisp shell contracts present.
PASS: Checked layered-overlay vector icons, DPI rounding, grayscale rendering, and emoji-free status text.
PASS: Checked compatible-SDK policy and self-contained Nexus release builder.
PASS: Lexically checked 84 C# files.
PASS: Executed 2 SQLite schema/FTS blocks and smoke-tested companion tables.
PASS: validation completed with no detected errors.
```

Exit code: `0`. The 2.4.3 checks add the sidebar version caption, `VERSION.txt`, the ComboBox
`DisplayMemberPath` template binding and the .NET 10+ SDK gate in `tools/Build-NexusRelease.ps1`.

`tools/CudaSpirit.Smoke` (route seeding, farm planner, 2026 brackets, boss rotation) ends with
`ALL SMOKE CHECKS PASSED`, and `BUILD_NEXUS_RELEASE.bat` produced the self-contained package whose
exe opened its main window.

## Native build boundary

Native Windows WPF compilation remains authoritative and is performed by `publish.bat`,
`BUILD_NEXUS_RELEASE.bat` or the GitHub Actions workflow, with warnings treated as errors and a
visible-window smoke test.

## 2.4.1 overlay icon regression fix

The transparent HUD and Advisor overlays now use vector geometry rather than Segoe MDL2 font glyphs or color emoji. Layered windows use layout rounding, device-pixel snapping, and grayscale text rendering to avoid missing boxes, substituted symbols, and DPI distortion.
