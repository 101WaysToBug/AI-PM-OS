# Release Notes — v0.3.0 (2026-03-06)

## Summary

Communication Styles has been extracted from AI PM OS into a standalone Claude Code skill (`/communicate`), making it installable and usable independently across any project.

---

## Removed: Communication Styles directory

The `communication-styles/` folder has been removed from this repo. All four style templates (Executive Email, Slack Update, Notion Document, Release Notes) now live in the standalone [/communicate](https://github.com/101WaysToBug/communicate) skill.

## Changed: Companion Skills section in README

The README no longer lists Communication Styles as tool #4. Instead, a new **Companion Skills** table links to standalone skills that complement AI PM OS:

| Skill | What it does |
| --- | --- |
| `/communicate` | Transforms content into Executive Email, Slack Update, Notion Doc, or Release Notes |
| `/one-pager-PRD` | Generates a one-pager PRD using Lenny Rachitsky's framework |

The workflow diagram has been updated to reference the `/communicate` skill.

---

## Migration Notes

- If you were using the `communication-styles/` templates directly, install the `/communicate` skill instead: `claude skill add /path/to/communicate`
- The skill adds interactive style selection (pick one style or generate all four at once) which was not available in the directory-based approach
