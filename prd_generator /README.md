# PRD Generator

An AI-powered PRD writing assistant built on [Claude Code](https://docs.anthropic.com/en/docs/claude-code). It loads your company context, surfaces feature ideas from your research tools, guides you through structured Socratic questioning, and outputs a polished PRD using your template of choice.

## What it generates

- **Structured PRD** — using either Lenny Rachitsky's lightweight template or Carl's two-phase Problem/Solution Alignment template
- **Evidence-grounded sections** — pulled from nugget-synthesizer insights and competitive research, not written from scratch
- **Clarified requirements** — through Socratic questioning that surfaces assumptions, success criteria, and strategic fit before a single word is drafted

## How it works

1. **Loads company context** — reads `company.md`, `product.md`, and `persona.md` at session start
2. **Surfaces feature ideas** — reads all synthesis files from `nugget-synthesizer/insights/` and `competitive_landscape_matrix.md` from `competition_researcher/insights/`; presents each feature idea with a rationale grounded in both customer evidence and competitive signals
3. **Feature selection** — asks you to pick a feature (enter a number or type your own); waits for your answer before moving on
4. **Template selection** — asks you to choose between two PRD templates; one question, waits for your answer
5. **Socratic questioning** — asks 3–5 targeted questions one at a time; each question includes 2–3 numbered answer options grounded in your company context, or you can type your own answer
6. **Drafts the PRD** — grounds every section in loaded context and your answers
7. **Saves output** — writes the final PRD to the `prd/` folder

## Usage

```bash
cd "prd_generator "
claude
# Claude will:
# 1. Load company, product, and persona context
# 2. Show feature ideas with customer evidence + competitive rationale
# 3. Ask you to select a feature (enter a number or type your own)
# 4. Ask which PRD template you'd like to use
# 5. Ask 3–5 Socratic questions one at a time (numbered options or type your own)
# 6. Draft and save the PRD
```

Output is saved to `prd/FEATURE-NAME-prd.md` (folder is created automatically if it doesn't exist).

## Templates

| Template | Best for | Structure |
|---|---|---|
| **Lenny's PRD** | Early-stage features, quick alignment | 7 sections: Description, Problem, Why, Success, Audience, What, How, When |
| **Carl's PRD** | Complex features, cross-functional alignment | Two phases: Problem Alignment → Solution Alignment → Launch Planning |

## Directory Structure

```
prd_generator/
├── CLAUDE.md              # Agent instructions (the brain of this tool)
├── README.md              # This file
├── prd-templates/
│   ├── Lennys-PRD-Template.md
│   └── Carls-PRD-Template.md
├── frameworks/
│   └── socratic-questioning.md
└── prd/                   # Output folder (auto-created)
```

## Dependencies

This tool reads from sibling directories. Make sure these exist and are populated:

- `../company_context/` — `company.md`, `product.md`, `persona.md`
- `../nugget-synthesizer/insights/` — synthesis files from the Nugget Synthesizer tool
- `../competition_researcher/insights/` — landscape matrix from the Competition Researcher tool

If the insights folders are empty, the tool will ask you for a feature brief or suggest ideas based on company context.

## Sensitive Files

The following directories contain customer research, competitive intelligence, and output files. They are excluded from git via `.gitignore` and should never be committed:

- `nugget-synthesizer/insights/` — user research synthesis files
- `competition_researcher/competitors/` — individual competitor research reports
- `competition_researcher/insights/` — competitive landscape matrix
- `metrics_and_goals_generator/metrics/` — internal metrics and goal tracking
- `prd_generator/prd/` — generated PRD output files

## Prerequisites

- A paid [Claude](https://claude.ai) subscription (Pro, Max, Team, or Enterprise)
- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
