# Nugget Synthesizer

A PM tool that transforms raw user feedback — support tickets, meeting notes, survey responses, and sales notes — into structured, actionable insight reports.

## What It Does

Given a collection of user feedback across multiple sources, Nugget Synthesizer produces a consolidated synthesis containing:

- Top pain points with cross-source frequency counts
- Supporting user quotes with source attribution
- Survey demand data segmented by role
- Competitive intelligence from lost deals
- Use cases categorized by theme
- Feature requests ranked by priority (impact vs. effort)
- Actionable next steps for product, engineering, and design

## How It Works

Four specialized agents process each feedback source **in parallel**, each producing a persisted analysis file in `insights/`. After all agents complete, a final consolidation step merges all four into one unified synthesis report.

| Agent | Input | Output |
|-------|-------|--------|
| Meeting Notes Analyst | `meeting-notes/` | `insights/meeting-notes-analysis.md` |
| Survey Analyst | `surveys/` | `insights/survey-analysis.md` |
| Support Analyst | `support-tickets/` | `insights/support-tickets-analysis.md` |
| Sales Analyst | `sales-notes/` | `insights/sales-analysis.md` |
| **Consolidation** | All 4 agent files | `insights/TOPIC-NAME-synthesis.md` |

## Directory Structure

```
nugget-synthesizer/
├── CLAUDE.md              # Agent instructions and rules
├── README.md              # This file
├── meeting-notes/         # Customer call and interview notes
├── surveys/               # Survey responses (CSV)
├── support-tickets/       # Raw support tickets and complaints
├── sales-notes/           # Lost deal notes and competitor intel
└── insights/              # Generated output (agent analyses + final synthesis)
```

## Usage

1. Add feedback files to the appropriate source directories
2. Run Claude Code from this directory
3. The tool reads all sources, runs parallel agents, and produces the synthesis in `insights/`

## Output

After a full run, `insights/` contains exactly **5 files**: 4 per-agent analyses and 1 final consolidated synthesis report. Both tiers persist for traceability.

See `CLAUDE.md` for the full report structure, table formats, segmentation rules, and content guidelines.
