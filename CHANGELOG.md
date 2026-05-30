# Changelog

All notable changes to File Organizer are documented here.  
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).  
This project uses [Semantic Versioning](https://semver.org/).

---

## [1.1.0] — 2026-05-29

### Added
- **Protected path blocking** — hard exit if the target is a system or known
  game directory (`C:\Program Files`, `/Applications`, Steam, GOG, Epic, etc.)
- **Game installation detection** — scans for 30+ game/engine file signatures
  (Unreal, Unity, Bethesda, Blizzard, Valve, id Software, Ubisoft, Wwise …)
  and prompts before continuing if 3+ are found
- **Executable confirmation prompt** — lists `.exe`, `.dll`, `.pak`, `.bin`
  and similar risky files, then offers Skip / Move / Quit before proceeding
- **Recursion guard** — prints a notice when sub-folders are present,
  confirming they will never be entered or modified
- `--force` flag to bypass all interactive safety prompts for automation
- Expanded `rules.json` with Design, 3D-Models, Disk-Images, Subtitles,
  and Torrent categories; broader RAW image format coverage

### Changed
- Version bumped to 1.1.0 in script header

---

## [1.0.0] — 2026-05-29

### Added
- Core file organiser: moves loose files into category sub-folders by extension
- 11 built-in categories: Images, Videos, Audio, Documents, Spreadsheets,
  Presentations, Archives, Code, Executables, Fonts, Ebooks
- `--dry-run` / `-n` flag — preview all moves without touching files
- `--undo` — reverses the last run using `~/.file_organizer_undo.json`
- `--config FILE` / `-c` — load a custom category → extension JSON rules file
- `--skip-unknown` — leave unrecognised files in place instead of `Other/`
- Collision-safe moves — appends `_1`, `_2` … rather than overwriting
- Works on macOS, Windows, and Linux with no third-party dependencies
