# CUK밥 Changelogs

Changelog files for the **CUK밥** app — an unofficial cafeteria menu app for Catholic University of Korea (가톨릭대학교).  
Each release's notes are maintained in four languages and consumed directly by the app to display the "What's New" screen.

---

## Repository Structure

```
CUK-changelogs/
├── announcements/           # Announcements per language
│   ├── en/
│   │   └── announcements.json
│   ├── ko/
│   │   └── announcements.json
│   ├── ja/
│   │   └── announcements.json
│   └── zn/
│       └── announcements.json
├── changelogs/              # Current changelogs
│   ├── en/
│   │   └── 2.2.0.md         # English (latest version)
│   ├── ko/
│   │   └── 2.2.0.md         # Korean (한국어)
│   ├── ja/
│   │   └── 2.2.0.md         # Japanese (日本語)
│   └── zn/
│       └── 2.2.0.md         # Chinese Simplified (中文)
└── changelogs_old/          # Archive of all previous release notes
    ├── en.md
    ├── ko.md
    ├── ja.md
    └── zn.md
```

### `announcements/`

Contains current announcements for each language. Each folder contains an `announcements.json` file.

### `changelogs/`

Contains the changelog for the **current (latest) release**, organized by language subdirectories and version-specific filenames (e.g., `2.2.0.md`). These files are what the app reads to display the "What's New" page on first launch after an update.

### `changelogs_old/`

A cumulative archive of release notes for **all previous versions**, going back to 1.0. When a new version is released, the previous changelog content should be merged into these files.

---

## Languages

| Code | Language |
|------|----------|
| `en` | English |
| `ko` | Korean (한국어) |
| `ja` | Japanese (日本語) |
| `zn` | Chinese Simplified (中文简体) |

All language files must be updated together for every release. The app defaults to English if a user's language is not supported.

---

## Changelog Format

Current changelogs (`changelogs/{lang}/{version}.md`) use structured headers to categorize changes:

```markdown
## Version X.Y.Z

### Added
* New feature description

### Changed
* What was modified

### Fixed
* What was broken and is now resolved

### Improved
* General improvements and polish
```

Old changelogs (`changelogs_old/{lang}.md`) use a flat bullet list format per version, as they predate the structured format:

```markdown
## Version X.Y.Z
- Change description
- Another change
```

---

## Updating for a New Release

1. Move the content of the previous version's changelog from `changelogs/{lang}/{prev_version}.md` into the top of the corresponding `changelogs_old/{lang}.md` files.
2. Create a new version-specific file (e.g., `2.3.0.md`) in each `changelogs/{lang}/` directory.
3. Update `version.json` with the new `versionName` and increment the `versionCode`.
4. If there are new announcements, update `announcements/{lang}/announcements.json`.

---

## Related

- **CUK-Menu** — the companion repo that parses cafeteria PDFs and generates the menu JSON the app reads: [https://github.com/CUKbab/CUK_Menu](https://github.com/CUKbab/CUK_Menu)
- **Contact:** cukqkq@gmail.com
