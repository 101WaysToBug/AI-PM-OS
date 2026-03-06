# Changelog

## 2026-03-06 (v0.3.0)

### Removed
- **`communication-styles/`** — Extracted into a standalone Claude Code skill ([/communicate](https://github.com/101WaysToBug/communicate)). The skill supports 4 styles (Executive Email, Slack Update, Notion Document, Release Notes) with interactive style selection.
- **`task_generator/`** — Extracted into a standalone Claude Code skill ([/generate-ticket](https://github.com/101WaysToBug/generate-ticket)). The skill takes user stories, PRDs, or metric sheets as input and generates structured tickets with team prefix selection.

### Changed
- **`README.md`** — Removed Communication Styles and Task Generator tool sections. Added both as companion skills in the "Companion Skills" table alongside `/one-pager-PRD`. Updated workflow diagram to reference `/communicate` and `/generate-ticket` skills.

---

## 2026-03-06 (v0.2.0)

### Added
- **`communication-styles/style-release-notes.md`** — Release notes communication style template for announcing changes to users and stakeholders (structured, neutral, value-focused)
- **`company_context/`**** directory** — Centralized shared context loaded by all tools at session start
  - `company.md` — Wati company overview, platform capabilities, role, and company stage
  - `persona.md` — 6 user personas (Priya, Rahul, Anita, David, Neha, Vijay)
  - `product.md` — Deep-dive on WhatsApp Business Calling and Voice AI (Astra), sourced from all 8 Wati support articles: capabilities, call flows, restrictions, pricing, analytics, Request Accepted view, call permission template localization, voice call CTA, and call availability/notifications
- **`nugget-synthesizer/`** — New feedback synthesis tool with parallel agent architecture
  - `CLAUDE.md` — Full agent instructions with execution protocol, report structure, and immutable rules
  - `README.md` — Tool overview, architecture, directory structure, and usage guide
  - Source directories: `meeting-notes/`, `surveys/`, `support-tickets/`, `sales-notes/`
  - Output directory: `insights/`
- **Execution Protocol** in nugget-synthesizer `CLAUDE.md` — Explicit 4-step instructions (load context, check sources, launch 4 parallel Task agents, consolidate) so Claude Code automatically spins up agents on synthesize requests
- **"Setting Up Your Company Context"** section in parent `README.md` — Step-by-step guide for PMs to create their own `company_context/` folder
- **Nugget Synthesizer** listed as tool #3 in parent `README.md` with description, usage, and updated workflow diagram
- **`communication-styles/`** — Three parallel communication style templates for transforming any content into stakeholder-ready formats
  - `style-executive-email.md` — Strategic 3-paragraph email for leadership (professional, data-driven, outcome-focused)
  - `style-slack-update.md` — Quick 2-4 line team update (casual, scannable, with emojis)
  - `style-notion-doc.md` — Comprehensive async reference document (detailed, well-organized, standalone)
- **Communication Styles** listed as tool #4 in parent `README.md` with usage, style table, and updated workflow diagram

### Changed
- **Company context loading** — Changed all 3 CLAUDE.md files to load context **once at session start** instead of before every task, to reduce token usage
- **All 3 CLAUDE.md files** now load `company_context/company.md`, `persona.md`, and `product.md` at session start
- **Extracted** Product Context and User Personas from `metrics_and_goals_generator/CLAUDE.md`, `task_generator/CLAUDE.md`, and `nugget-synthesizer/CLAUDE.md` into shared `company_context/` files (removed duplicated sections)
- **Segmentation dimensions** updated across all tools to match:
  - ACV Band: $0–1K, $1K–3K, $3K–5K, $5K-10K, $10K+
  - Region: India, ROW, LATAM, GCR, Europe
- **Parent \****`README.md`** — Replaced old "Customization" section with "Setting Up Your Company Context" + "Further Customization"
- **Nugget synthesizer source references** — Fixed stale paths (`survey-results.csv` → `surveys/`, `sales-notes.md` → `sales-notes/`) to match actual directory structure
