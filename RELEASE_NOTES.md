# Release Notes — v0.3.0 (2026-03-06)

## Summary

Communication Styles and Task Generator have been extracted from AI PM OS into standalone Claude Code skills (`/communicate` and `/generate-ticket`), making them installable and usable independently across any project.

---

## Removed: Communication Styles directory

The `communication-styles/` folder has been removed from this repo. All four style templates (Executive Email, Slack Update, Notion Document, Release Notes) now live in the standalone [/communicate](https://github.com/101WaysToBug/communicate) skill.

## Removed: Task Generator directory

The `task_generator/` folder has been removed from this repo. Ticket generation now lives in the standalone [/generate-ticket](https://github.com/101WaysToBug/generate-ticket) skill. The skill takes user stories, PRDs, or metric sheets as input and produces structured tickets with team prefix selection (`[Data]`, `[Eng]`, `[FE]`, `[Design]`, `[DevOps]`, `[QA]`).

## Changed: Companion Skills section in README

The README now lists three companion skills:

| Skill | What it does |
| --- | --- |
| `/communicate` | Transforms content into Executive Email, Slack Update, Notion Doc, or Release Notes |
| `/generate-ticket` | Generates structured project tickets (YouTrack/JIRA) from user stories, PRDs, or metric sheets |
| `/one-pager-PRD` | Generates a one-pager PRD using Lenny Rachitsky's framework |

The workflow diagram has been updated to reference `/communicate` and `/generate-ticket` skills.

---

## Migration Notes

- If you were using the `communication-styles/` templates directly, install the `/communicate` skill instead: `claude skill add /path/to/communicate`
- If you were using the `task_generator/` directory, install the `/generate-ticket` skill instead: `claude skill add /path/to/generate-ticket`
- Both skills add interactive prompting (style selection, team prefix selection) which was not available in the directory-based approach
