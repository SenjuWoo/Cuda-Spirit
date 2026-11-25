# Troubleshooting

## The release zip will not start

- Keep the extracted files together and run `CudaSpirit.exe` from a folder outside Program Files.
- Unblock the zip (file Properties, Unblock) before extracting if Windows SmartScreen stops it.
- The exe is self-contained; no .NET runtime is needed.

## Building from source fails

- Install any stable .NET 10 or newer SDK; `publish.bat` and `BUILD_NEXUS_RELEASE.bat` refuse older SDKs with a message.
- Confirm Windows can reach NuGet for the package restore.
- Temporarily allow PowerShell and `dotnet.exe` through security software.
- Run `python tools/validate_source.py` on a clean tree; it names the file and rule that failed.

## The app opens but rendered official pages fail

Install or repair the Microsoft Edge WebView2 Runtime. Basic cached guides, deterministic safety engines, market APIs, and local data can still work when rendered fallback is unavailable.

## A source is degraded

Open **Live Data Center**. Cuda Spirit keeps cached records and retries degraded sources after a controlled interval. Maintenance, regional website changes, API limits, or bot protection can temporarily affect one feed without disabling the others.

## Profile sync fails

- Confirm the official adventurer profile is public.
- Paste the complete profile link.
- Confirm the app region matches the profile region.
- Retry after website maintenance.

## Reset local app data

Close Cuda Spirit and rename or delete:

```text
%APPDATA%\CudaSpirit
```

Back it up first to preserve tasks, settings, decisions, and history.
