# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## Session Startup — Always Do This First

At the start of every session, load the company context by reading all three files:

- `../company_context/company.md` — Wati's mission, products, funding stage, and metrics
- `../company_context/product.md` — Deep detail on WhatsApp Business Calling and Voice AI (Astra)
- `../company_context/persona.md` — Six user personas (Priya, Rahul, Anita, David, Neha, Vijay)

Do not proceed to PRD generation without loading these. They inform tone, framing, audience, and feature prioritization throughout the session.

---

## PRD Generator Workflow

### Step 1 — Surface Feature Ideas

Check both insight sources in parallel:

1. **Nugget Synthesizer:** `../nugget-synthesizer/insights/` — look for `*-synthesis.md` files, each represents a synthesized topic from user research
2. **Competition Researcher:** `../competition_researcher/insights/` — look for `competitive_landscape_matrix.md` and any competitor briefs

Present the user with a numbered list of available topics/feature ideas drawn from these sources. If both folders are empty or have no relevant content, either:
- Ask the user to share a short write-up on the feature they want to PRD
- Offer 3–5 feature ideas grounded in the loaded product context and personas

### Step 2 — Choose a PRD Template

If the user has not specified a format, ask them to choose between the two templates in `prd-templates/`:

- **Lenny's PRD Template** (`Lennys-PRD-Template.md`) — Lightweight, 7-section format. Best for early-stage features or quick alignment docs.
- **Carl's PRD Template** (`Carls-PRD-Template.md`) — Structured, two-phase format (Problem Alignment → Solution Alignment). Best for complex features requiring cross-functional alignment.

### Step 3 — Socratic Questioning

Before drafting, use `frameworks/socratic-questioning.md` to ask the user 3–5 targeted questions. Follow the framework's guidance:

- Start with **Problem Clarity** (is the problem real and specific?)
- Move to **Solution Validation** and **Success Criteria**
- End with **Strategic Fit** (why now, why this?)
- Pick only the most relevant questions — quality over quantity
- Be a thought partner, not an interrogator
- If the user struggles to answer a question or says they're unsure, offer 2–3 concrete answer options grounded in the loaded company/product/persona context for them to choose from or react to

Use the user's answers to ground the PRD in evidence, not assumptions.

### Step 4 — Write the PRD

Draft the PRD using the selected template structure. Ground every section in:
- The loaded company/product/persona context
- Insights from nugget-synthesizer or competition research
- The user's answers from the Socratic questioning phase

### Step 5 — Output

Save the PRD to the `prd/` folder. Create it if it doesn't exist. Use a descriptive filename: `prd/{feature-name}-prd.md`.

---

## Directory Reference

```
prd_generator/
├── CLAUDE.md                  # This file
├── prd-templates/
│   ├── Lennys-PRD-Template.md
│   └── Carls-PRD-Template.md
├── frameworks/
│   └── socratic-questioning.md
└── prd/                       # Output folder (create if missing)

../company_context/
├── company.md
├── product.md
└── persona.md

../nugget-synthesizer/insights/     # *-synthesis.md files from user research
../competition_researcher/insights/ # competitive_landscape_matrix.md + competitor briefs
```

---

## Wati Context Snapshot

**Company:** Wati — #1 WhatsApp API SaaS for SMBs. Series B, $35M raised, 15,000+ customers, $25M ARR.

**PM Focus:** WhatsApp Business Calling + Voice AI (Astra)

**Key Personas:** Priya (Marketing), Rahul (Sales Director), Anita (Support Lead), David (Founder), Neha (Sales IC), Vijay (Support Agent)

**Core Products:**
- WhatsApp Business Calling — voice calls inside the Wati inbox, no app-switching
- Voice AI (Astra) — near-human AI agent, 30+ languages, no-code builder, multi-channel
