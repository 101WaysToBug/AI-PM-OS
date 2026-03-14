# Release Notes — v0.5.0 (2026-03-14)

## Summary

AI PM OS adds **PRD Generator** — an interactive PRD writing assistant that guides PMs from raw feature idea to structured, evidence-backed PRD through Socratic questioning, using your existing research tools as input.

---

## New: PRD Generator

PRD Generator removes the blank-page problem. It loads your company context, surfaces feature ideas from the Nugget Synthesizer and Competition Researcher, and guides you through a structured dialogue before writing a single word of the PRD.

- Reads `company_context/`, `nugget-synthesizer/insights/`, and `competition_researcher/insights/` at session start — no copy-pasting context
- Presents available feature topics from your insight files; falls back to asking for a brief if folders are empty
- Prompts template selection between two formats: **Lenny's PRD** (lightweight, 7 sections) or **Carl's PRD** (two-phase Problem/Solution Alignment)
- Runs **3–5 Socratic questions** before drafting — covering problem clarity, solution rationale, success criteria, constraints, and strategic fit
- **Offers 2–3 answer options** when a PM is unsure, so the session never stalls
- Saves output to `prd/FEATURE-NAME-prd.md`, creating the folder if it doesn't exist

## New: Socratic Questioning Framework

The `frameworks/socratic-questioning.md` file defines five question categories with guidance on how to pick the right questions, what red flags to listen for, and how to coach PMs through weak answers. The goal is a thought partner, not an interrogator.

After questioning, the PM has:
- A clear, specific problem statement with evidence
- Justification for why this solution, not another
- Concrete success criteria (quantitative + qualitative)
- Explicit scope boundaries
- A strategic narrative for why this matters now

## Changed: README + Workflow Diagram

The root `README.md` now lists PRD Generator as Tool #1 and includes an updated end-to-end workflow diagram showing the full pipeline: research → PRD → metrics → ticket.

---

*Part of [AI PM OS](https://github.com/101WaysToBug/AI-PM-OS) — AI-powered tools for Product Managers built on Claude Code.*

---

# Release Notes — v0.4.0 (2026-03-09)

## Summary

AI PM OS adds **Competition Researcher** — a Claude Code-powered tool that conducts deep competitive intelligence on any feature or product domain using parallel AI agents, and synthesizes findings into a structured competitive landscape matrix.

---

## New: Competition Researcher

Competition Researcher automates the most time-consuming parts of competitive analysis. Describe the feature domain you care about, point it at your competitors, and it does the rest — deep web research, structured briefs, and a consolidated matrix ready for roadmap and positioning decisions.

- Launches **one research agent per competitor in parallel** — no waiting for each to finish before the next starts
- Each agent searches product pages, pricing, docs, changelogs, G2/Capterra reviews, blog posts, and app store listings
- Outputs a **structured competitor brief** per company covering: features, pricing tiers, target market, strengths, weaknesses, and a direct head-to-head comparison to your product
- Distinguishes between **GA features**, **beta/EAP**, and **announced-but-not-shipped** — writes "Not publicly documented" rather than guessing
- Includes a built-in **review and correction loop** — after research completes, flag inaccuracies and provide URLs for the tool to self-correct
- Generates a **competitive landscape matrix** at `insights/competitive_landscape_matrix.md` covering feature comparison, pricing analysis, universal market gaps, strategic positioning, and ranked product opportunities

## New: Interactive Session Workflow

The tool guides you through each research run conversationally:

1. Asks which feature/domain to research
2. Checks `competitors/` for existing profiles — reuses them and asks if you want to add more
3. Launches all competitor agents simultaneously
4. Prompts for a gap-check and correction pass before finalizing
5. Builds the landscape matrix only after you sign off on the briefs

## Changed: README

The root `README.md` now lists Competition Researcher as Tool #1 and includes an updated workflow diagram showing the competitive research → landscape matrix flow.

---

*Part of [AI PM OS](https://github.com/101WaysToBug/AI-PM-OS) — AI-powered tools for Product Managers built on Claude Code.*

---

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
