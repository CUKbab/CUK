# CUK밥 Changelogs

Changelog files for the **CUK밥** app — an unofficial cafeteria menu app for Catholic University of Korea (가톨릭대학교).  
Each release's notes are maintained in four languages and consumed directly by the app to display the "What's New" screen.

---

## Repository Structure

```
CUK-changelogs/
├── changelogs/              # Current changelogs (latest release)
│   ├── en.md                # English
│   ├── ko.md                # Korean (한국어)
│   ├── ja.md                # Japanese (日本語)
│   └── zn.md                # Chinese Simplified (中文)
└── changelogs_old/          # Archive of all previous release notes
    ├── en.md
    ├── ko.md
    ├── ja.md
    └── zn.md
```

### `changelogs/`

Contains the changelog for the **current (latest) release only**. These files are what the app reads to display the "What's New" page on first launch after an update. Each file contains only the notes for the most recent version — not the full history.

### `changelogs_old/`

A cumulative archive of release notes for **all previous versions**, going back to 1.0. When a new version is released, the previous `changelogs/` content should be merged into these files before being replaced.

---

## Languages

| File | Language |
|------|----------|
| `en.md` | English |
| `ko.md` | Korean (한국어) |
| `ja.md` | Japanese (日本語) |
| `zn.md` | Chinese Simplified (中文简体) |

All four files must be updated together for every release. The app defaults to English if a user's language is not supported.

---

## Changelog Format

Current changelogs (`changelogs/`) use structured headers to categorize changes:

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

Old changelogs (`changelogs_old/`) use a flat bullet list format per version, as they predate the structured format:

```markdown
## Version X.Y.Z
- Change description
- Another change
```

---

## Updating for a New Release

1. Move the current contents of `changelogs/*.md` into the top of the corresponding `changelogs_old/*.md` files (above the previous most-recent version).
2. Replace the contents of `changelogs/*.md` with the new version's release notes.
3. Make sure all four language files are updated.

---

## Related

- **CUK-Menu** — the companion repo that parses cafeteria PDFs and generates the menu JSON the app reads: [github.com/...](https://github.com)
- **Contact:** cukqkq@gmail.com
