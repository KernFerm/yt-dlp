# yt-dlp 2026.07.05 for Windows

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
2026.07.05
```

## What Changed

- Bumped the custom fork version from upstream `2026.07.04` to `2026.07.05`
- Included local CodeQL security cleanup for parser, URL handling, and loopback socket binding checks
- Added fork-specific documentation for the Windows build
- Built a standalone Windows x64 executable with PyInstaller

## Security Notes

This build includes local cleanup for GitHub CodeQL findings from the fork. The
socket binding cleanup keeps empty local interface values on loopback instead of
binding to all network interfaces.

The remaining test-only CodeQL noise was reviewed separately and dismissed where
it only applied to test coverage, not runtime behavior.

## File Details

- Version: `2026.07.05`
- Release date: `2026-07-23`
- Platform: `Windows x64`
- File size: `26,145,533 bytes`
- SHA256: `2E6BDD0875A5B88C5C3BBDD72F4C56DC4163B9A7A50033AF1F8BB6E55EF3B542`

## Verification

The executable was verified on Thursday, July 23, 2026 with:

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
