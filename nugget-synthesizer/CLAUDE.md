# User Feedback Synthesizer

> **Before starting any task, load the company context from \****`../company_context/company.md`***\*, \****`../company_context/persona.md`***\*, and \****`../company_context/product.md`**\*\*.**

## What This Project Does

User Feedback Synthesizer is a PM tool that transforms raw user feedback — from support tickets, meeting notes, and feature requests — into structured, actionable insight reports. Given a collection of user feedback, it produces a synthesis containing top pain points with frequency counts, supporting user quotes, feature requests ranked by priority, and recommended next steps.

**Primary Output:** A two-tier output structure. First, each specialized agent produces its own persisted analysis file in the `insights/` subdirectory. Then, a final consolidated synthesis report is produced by reading all four agent files and merging them into one unified document. Both the per-agent analysis files and the final synthesis file persist in `insights/`.

## Feedback Source Directories

- `meeting-notes/` — Notes from customer calls, user interviews, and internal syncs
- `surveys/` — Customer survey responses (CSV or markdown; may include role segmentation)
- `support-tickets/` — Raw customer support tickets and complaints
- `sales-notes/` — Sales team notes on lost deals, competitor intelligence, and revenue impact

## Execution Protocol

When the user asks to synthesize feedback (e.g., "synthesize the feedback on X", "run the synthesizer", "analyze the feedback"), execute the following steps automatically:

### Step 1: Load Context
Read `../company_context/company.md`, `../company_context/persona.md`, and `../company_context/product.md`.

### Step 2: Check Sources
Scan each source directory (`meeting-notes/`, `surveys/`, `support-tickets/`, `sales-notes/`) to confirm which ones contain files. Only launch agents for sources that have data.

### Step 3: Launch Parallel Agents
Use the **Task tool** to launch up to 4 agents **in a single message** (parallel execution). Each agent must be a `general-purpose` subagent type. In each agent's prompt, include:
- The full company context (company, persona, product)
- The specific source files the agent should read (provide exact file paths)
- The agent's role, analysis instructions, and exact output file path in `insights/`
- The writing style, table format rules, segmentation dimensions, and content rules from this CLAUDE.md
- Instructions to use the Write tool to save the analysis file

Launch all agents in one tool-call block — do not wait for one to finish before starting the next.

### Step 4: Consolidate
After **all** agents complete, read all persisted agent output files from `insights/` and produce the final synthesis file (`insights/TOPIC-NAME-synthesis.md`) by merging findings from every agent file. Follow the Insight Report Structure and Consolidation Rules below.

## Agent Architecture

Four specialized agents process each source type independently. Each agent saves its own persisted analysis file to `insights/`. After all four agents complete, a final consolidation step reads all four agent output files and produces the unified synthesis report.

### Agent Roles and Output Files

**Agent 1: Meeting Notes Analyst** → saves `insights/meeting-notes-analysis.md`
- Reads all files in `meeting-notes/`
- Synthesizes pain points with cross-customer frequency counts
- Extracts exact supporting quotes with customer attribution
- Identifies opportunities distinct from pain points

**Agent 2: Survey Analyst** → saves `insights/survey-analysis.md`
- Reads all files in `surveys/`
- Calculates percentage of respondents requesting each feature
- Segments results by user role (PM, Engineer, Designer, etc.) if role data is available
- Outputs demand data as percentages (e.g., "72% of respondents requested X")

**Agent 3: Support Analyst** → saves `insights/support-tickets-analysis.md`
- Reads all files in `support-tickets/`
- Categorizes requests by use case (e.g., onboarding, billing, integration, feature gap)
- Identifies the most common scenarios and ticket themes
- Counts frequency by unique tickets, not mentions

**Agent 4: Sales Analyst** → saves `insights/sales-analysis.md`
- Reads all files in `sales-notes/`
- Identifies lost deals with revenue impact (ACV lost)
- Documents which competitors won each deal and what they offered
- Extracts competitive gaps and positioning weaknesses

### Output File Structure

After a full run, `insights/` contains exactly 5 files:

```
insights/
├── meeting-notes-analysis.md       ← Agent 1 output (persists)
├── survey-analysis.md              ← Agent 2 output (persists)
├── support-tickets-analysis.md     ← Agent 3 output (persists)
├── sales-analysis.md               ← Agent 4 output (persists)
└── TOPIC-NAME-synthesis.md         ← Final consolidated report
```

### Consolidation Rules

After all four agents complete and their files are saved to `insights/`, produce the **final synthesis file** (e.g., `insights/TOPIC-NAME-synthesis.md`) by reading all four agent output files and merging their findings. The consolidated report must include data from every agent file. The final report adds these sections beyond the standard structure:

- **Demand Data** — Percentage of survey respondents requesting each feature, segmented by role where available
- **Competitive Intelligence** — Lost deals, competitors involved, what they offered, and total revenue impact
- **Use Cases** — Common scenarios from support tickets, categorized by theme
- **Recommendation** — A final prioritized recommendation informed by all sources (pain point frequency + survey demand + revenue impact + competitive pressure)

## Insight Report Structure

The final synthesis report consolidates all four agent output files into one document. Each agent file persists in `insights/` for traceability. Include these sections in the final synthesis in order:

1. **Header** — Report title, date range, all feedback sources listed (meeting notes, survey, support tickets, sales notes), owner, product area
2. **Executive Summary** — One-paragraph overview of the key findings and their business impact across all sources
3. **Top Pain Points** — Ranked list of pain points with cross-source frequency count (3-column table: Pain Point, Sources, Frequency). Frequency = number of unique customers/respondents/tickets that raised the pain point.
4. **Supporting Quotes** — Direct user quotes mapped to each pain point with source attribution (3-column table: Pain Point, User Quote, Source)
5. **Demand Data** — Survey results showing percentage of respondents requesting each feature, segmented by role where available (3-column table: Feature, % Requesting, Role Breakdown)
6. **Competitive Intelligence** — Lost deals with competitor and revenue impact (4-column table: Deal, Competitor, What They Offered, ACV Lost)
7. **Use Cases** — Common scenarios from support tickets categorized by theme (2-column table: Use Case Category, Ticket Count)
8. **Opportunities** — Strategic opportunities identified from the feedback, distinct from pain points. Opportunities are forward-looking product bets, new verticals, or competitive positioning advantages (3-column table: Opportunity, Evidence Sources, Impact)
9. **Feature Requests by Priority** — Prioritized list using impact vs. effort with source attribution (4-column table: Feature Request, Priority, Rationale, Sources)
10. **Recommendation** — Final prioritized recommendation informed by all sources: pain point frequency + survey demand + revenue impact + competitive pressure
11. **Recommended Next Steps** — Concrete, actionable recommendations for product, engineering, and design

## Insight Report Rules

### Table Format

- Pain point tables use 3 columns: **Pain Point**, **Sources**, and **Frequency**
- Quote tables use 3 columns: **Pain Point**, **User Quote**, and **Source**
- Demand data tables use 3 columns: **Feature**, **% Requesting**, and **Role Breakdown**
- Competitive intelligence tables use 4 columns: **Deal**, **Competitor**, **What They Offered**, and **ACV Lost**
- Use case tables use 2 columns: **Use Case Category** and **Ticket Count**
- Opportunity tables use 3 columns: **Opportunity**, **Evidence Sources**, and **Impact**
- Feature request tables use 4 columns: **Feature Request**, **Priority** (P0/P1/P2/P3), **Rationale**, and **Sources**

### Segmentation (always include)

- **Plan Type:** Growth / Pro / Business / Enterprise
- **ACV Band:** $0–1K, $1K–3K, $3K–5K, $5K-10K, $10K+ 
- **Region:** India, ROW, LATAM, GCR, Europe 

### Content Rules

- Derive pain points and feature requests directly from the feedback provided
- Count frequency by number of unique **customers** (not individual mentions) who raised the pain point
- Use exact user quotes — do not paraphrase or sanitize language
- Prioritize feature requests using impact (user frequency + business value) vs. effort
- Recommended next steps must be specific and assignable (not vague suggestions)

## Writing Style

### Tone

- Clear and outcome-focused
- Active voice (not passive)
- Concise (2-sentence max paragraphs for most content)
- Use "we" not "I" in documentation
- Avoid jargon unless it's standard PM terminology

### Formatting

- Always use Oxford commas
- Use bullet points for lists (not numbered unless sequence matters)
- **Bold** key terms on first use
- Include "Why this matters" context for top pain points

## Product Terminology

- **"PM"** = Product Manager (not Project Manager)
- **"ACV"** = Annual Contract Value
- **"Insight Report"** = the feedback synthesis document we generate (not "spec," "PRD," or "metric sheet")
- **"Pain Point"** = a recurring user problem identified across multiple feedback sources
- **"Opportunity"** = a forward-looking product bet, new vertical, or competitive advantage surfaced from feedback (distinct from pain points)
- **"Frequency"** = number of unique customers referencing a specific pain point (cross-customer count, not in-conversation mentions)

## Immutable Rules

### ALWAYS

- Run **parallel specialized agents** (Meeting Notes, Survey, Support, Sales) to process each source type
- Each agent **saves its own persisted analysis file** to `insights/` (e.g., `insights/meeting-notes-analysis.md`)
- After all agents complete, produce a **final synthesis file** (e.g., `insights/TOPIC-NAME-synthesis.md`) by reading and merging all four agent output files
- The `insights/` directory must contain exactly **5 files** after a full run: 4 agent analyses + 1 final synthesis
- Save all output files to the `insights/` subdirectory
- Count pain point frequency by **unique customers/respondents/tickets affected**, not individual mentions within a single conversation
- Include a **Top Pain Points** section with cross-source frequency counts in every report
- Include **Demand Data** from survey results with percentages and role segmentation
- Include **Competitive Intelligence** from sales notes with lost deal revenue impact
- Include **Use Cases** from support tickets categorized by theme
- Include an **Opportunities** section separate from pain points — opportunities are forward-looking, pain points are current problems
- Include **Supporting Quotes** with real user language and source attribution for every pain point
- Include **Feature Requests by Priority** ranked by impact vs. effort with source attribution
- Include a **Recommendation** section that synthesizes pain point frequency + survey demand + revenue impact + competitive pressure
- Include **Recommended Next Steps** that are specific and actionable
- Map pain points back to the relevant user persona(s) when possible
- Derive all insights from the actual feedback provided — do not fabricate data

### NEVER

- Skip saving per-agent analysis files — every agent must persist its output to `insights/`
- Produce the final synthesis without first reading all four agent output files
- Create separate files per customer or per meeting within a single agent's analysis — each agent produces exactly one file
- Skip the "Top Pain Points," "Demand Data," "Competitive Intelligence," "Use Cases," "Opportunities," or "Supporting Quotes" sections
- Paraphrase or sanitize user quotes — use their exact words
- Count frequency by in-conversation mentions instead of unique customers/respondents/tickets
- Leave feature requests unranked or without a priority level
- Write vague next steps (e.g., "look into this") — be specific
- Forget region and timestamp in segmentation
- Use passive voice in recommendations
- Save output files anywhere other than the `insights/` subdirectory
