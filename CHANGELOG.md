# Changelog

## 2026-03-06

### Added
- **`company_context/` directory** — Centralized shared context loaded by all tools at session start
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

### Changed
- **All 3 CLAUDE.md files** now load `company_context/company.md`, `persona.md`, and `product.md` at session start
- **Extracted** Product Context and User Personas from `metrics_and_goals_generator/CLAUDE.md`, `task_generator/CLAUDE.md`, and `nugget-synthesizer/CLAUDE.md` into shared `company_context/` files (removed duplicated sections)
- **Segmentation dimensions** updated across all tools to match:
  - ACV Band: $0–1K, $1K–3K, $3K–5K, $5K-10K, $10K+
  - Region: India, ROW, LATAM, GCR, Europe
- **Parent `README.md`** — Replaced old "Customization" section with "Setting Up Your Company Context" + "Further Customization"
- **Nugget synthesizer source references** — Fixed stale paths (`survey-results.csv` → `surveys/`, `sales-notes.md` → `sales-notes/`) to match actual directory structure
