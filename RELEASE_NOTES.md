# Release Notes — v0.2.0 (2026-03-06)

## Summary

This release introduces centralized company context, a new feedback synthesis tool, and communication style templates. It also restructures how all tools load shared information to reduce duplication and token usage.

---

## New: Centralized Company Context (`company_context/`)

All tools now load company, persona, and product information from a single shared directory instead of each tool carrying its own copy. This makes it easy to update context in one place and have it propagate across the entire toolkit.

- **`company.md`** — Company overview, platform capabilities, PM role, and company stage
- **`persona.md`** — 6 user personas with roles, pain points, and representative quotes
- **`product.md`** — Detailed product reference for WhatsApp Business Calling and Voice AI (Astra), covering capabilities, call flows, restrictions, pricing, analytics, and 8 Wati support articles

Context is loaded once at session start to minimize token consumption.

## New: Nugget Synthesizer (`nugget-synthesizer/`)

A feedback synthesis tool that transforms raw user feedback into structured insight reports. It uses a parallel agent architecture — 4 specialized agents (Meeting Notes, Survey, Support, Sales) each analyze their respective source independently, then a consolidation step merges all findings into a single report.

- Automatically spins up 4 parallel agents when the user asks to synthesize
- Each agent persists its own analysis file to `insights/`
- Final synthesis includes: top pain points, supporting quotes, demand data, competitive intelligence, use cases, opportunities, prioritized feature requests, and recommended next steps
- Execution protocol with explicit step-by-step instructions for Claude Code

## New: Communication Styles (`communication-styles/`)

Four templates for transforming any content into stakeholder-ready formats. Supports parallel execution to produce all outputs at once.

- **Executive Email** — 3-paragraph strategic update for leadership with business impact and recommendations
- **Slack Update** — 2-4 line quick team update, casual and scannable
- **Notion Document** — Comprehensive async reference document with full context and supporting details
- **Release Notes** — Structured release announcement for users/stakeholders with clear sections for new, improved, fixed, changed, deprecated, and removed items

## Changed: Segmentation Dimensions

Standardized across all tools to reflect actual business segments:

- **ACV Band:** $0-1K, $1K-3K, $3K-5K, $5K-10K, $10K+
- **Region:** India, ROW, LATAM, GCR, Europe

## Changed: README

- Added Nugget Synthesizer as tool #3
- Added Communication Styles as tool #4
- New "Setting Up Your Company Context" section with step-by-step guide for PMs to customize for their own company
- Updated workflow diagrams to include all four tools

---

## Migration Notes

If you previously relied on Product Context or User Personas sections within individual `CLAUDE.md` files, those have been moved to `company_context/`. Each tool's `CLAUDE.md` now reads from the shared directory at session start.
