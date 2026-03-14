# Changelog

## 2026-03-14 (v0.5.0)

### Added
- **`prd_generator/`** — New PRD writing assistant with interactive Socratic questioning workflow
  - `CLAUDE.md` — Full session protocol: loads company context, surfaces feature ideas from nugget-synthesizer and competition researcher, prompts for template selection, runs Socratic questioning (with 2–3 answer options when user is stuck), and saves PRD output
  - `README.md` — Tool overview, workflow, template comparison table, directory structure, and dependencies
  - `prd-templates/Lennys-PRD-Template.md` — Lenny Rachitsky's lightweight 7-section PRD template
  - `prd-templates/Carls-PRD-Template.md` — Carl's two-phase Problem Alignment → Solution Alignment → Launch Planning template
  - `frameworks/socratic-questioning.md` — Five-category questioning framework (Problem Clarity, Solution Validation, Success Criteria, Constraints, Strategic Fit) with coaching guidance and red flag detection
- **Socratic answer scaffolding** — When a PM can't answer a question, Claude offers 2–3 concrete options grounded in company/product/persona context to react to

### Changed
- **`README.md`** — Added PRD Generator as Tool #1 with description, usage, and updated workflow diagram showing the full research → PRD → metrics → ticket pipeline

---

## 2026-03-09 (v0.4.0)

### Added
- **`competition_researcher/`** — New competitive intelligence tool with parallel agent architecture
  - `CLAUDE.md` — Full interactive execution protocol: loads company context, asks for research domain, checks existing competitor profiles, launches N parallel research agents, runs a review/correction loop, and generates the landscape matrix
  - `README.md` — Tool overview, architecture, usage guide, and project structure
  - `competitors/` — Six competitor briefs (Respond.io, Infobip, Twilio, Zendesk, AiSensy, Interakt) researching WhatsApp Calling, Voice AI, call recording, AI transcription/summaries, and mobile app calling
  - `insights/competitive_landscape_matrix.md` — Consolidated matrix with feature comparison, pricing analysis, universal market gaps, strategic positioning, top opportunities, product priorities, and threat summary
- **Interactive correction loop** in `competition_researcher/CLAUDE.md` — After research completes, Claude asks the user to flag inaccuracies and accepts URLs to self-correct findings before generating the matrix
- **Parallel agent protocol** — Competition Researcher launches one `general-purpose` subagent per competitor simultaneously in a single Task tool call block

### Changed
- **`README.md`** — Added Competition Researcher as Tool #1 with description, usage, and updated workflow diagram showing the competitive research → landscape matrix flow

---

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
