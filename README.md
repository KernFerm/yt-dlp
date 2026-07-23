# KernFerm yt-dlp

Custom Windows build of `yt-dlp` for use with local projects and browser integration.

This fork is based on upstream `yt-dlp`, with local security cleanup and a custom Windows executable build.

## Current Build

- Version: `2026.07.05`
- Platform: `Windows x64`
- Executable: `dist/yt-dlp.exe`
- Build date: `2026-07-23`
- Origin: `KernFerm/yt-dlp`

## Verified

The current executable was tested with:

```powershell
.\dist\yt-dlp.exe --version
.\dist\yt-dlp.exe --help
.\dist\yt-dlp.exe --list-extractors
```

The executable reports:

```text
2026.07.05
```

## Basic Usage

Download a video:

```powershell
.\dist\yt-dlp.exe "https://example.com/video-url"
```

Show available options:

```powershell
.\dist\yt-dlp.exe --help
```

List supported extractors:

```powershell
.\dist\yt-dlp.exe --list-extractors
```

## Updating

This build does not need to be updated constantly. Keep this version unless you need:

- site extractor fixes when websites change
- new upstream features
- upstream security fixes
- local fork changes

When a new custom build is needed, bump the version in `yt_dlp/version.py` using:

```powershell
python devscripts\update-version.py VERSION -r KernFerm/yt-dlp
```

Then rebuild the Windows executable:

```powershell
python -m bundle.pyinstaller
```

## Build Requirements

- Python 3.11+
- PyInstaller

Install build dependencies if needed:

```powershell
python devscripts\install_deps.py --include-group pyinstaller
```

Build:

```powershell
python -m bundle.pyinstaller
```

The output will be:

```text
dist/yt-dlp.exe
```

## Notes

- This is a custom fork build, not an official upstream yt-dlp release.
- The official upstream project is available at `https://github.com/yt-dlp/yt-dlp`.
- Keep `dist/yt-dlp.exe` for your browser project or local tooling.
