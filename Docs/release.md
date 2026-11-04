# yt-dlp 2026.11.04 for Windows

This is a custom Windows x64 build of `yt-dlp` from the `KernFerm/yt-dlp` fork.
It is intended for local use, including integration with a custom web browser or
other personal tooling that needs a standalone `yt-dlp.exe`.

This is not an official upstream `yt-dlp` release.

## Download

Download the Windows executable from this release:

- `yt-dlp.exe`

After downloading, you can run it from PowerShell or Command Prompt:

```powershell
.\yt-dlp.exe --version
```

Expected version:

```text
2026.11.04
```

## What Changed

- Bumped the custom fork version from `2026.10.28` to `2026.11.04`
- Refreshed all Python dependency locks and hashed requirement sets
- Upgraded `curl-cffi` to `0.17.0` with matching request-handler support
- Repaired Dependabot monitoring for Python, Docker, and GitHub Actions
- Removed the vulnerable Python 3.10 `filelock` development dependency path

## Security Notes

The dependency sets were regenerated and audited with `pip-audit`. No known
vulnerabilities were reported in the default, curl-cffi, Linux, development,
build, or PyInstaller requirement sets.

## File Details

- Version: `2026.11.04`
- Release date: `2026-11-04`
- Platform: `Windows x64`
- File size: `Pending rebuild`
- SHA256: `Pending rebuild`

## Verification

After rebuilding, verify the executable with:

- `yt-dlp.exe --version`
- `yt-dlp.exe --help`
- `yt-dlp.exe --list-extractors`

## When To Update

You can keep using this build until you need one of the following:

- extractor fixes for websites that changed
- new upstream features
- upstream security fixes
- additional local fork changes

## Notes

- This release is for Windows x64.
- The official upstream project is available at `https://github.com/yt-dlp/yt-dlp`.
- If Windows blocks the file after download, open the file properties and use the standard Windows unblock option.
