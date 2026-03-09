# Competition Researcher

A PM tool powered by [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that conducts deep competitive intelligence on any feature or product domain. Point it at a set of competitors, describe what you want to research, and it launches parallel AI agents to build structured competitor briefs and a consolidated competitive landscape matrix.

## What It Does

Given a feature domain (e.g., "WhatsApp Business Calling and Voice AI") and a list of competitors, Competition Researcher:

- Launches **one research agent per competitor in parallel** — each does deep web research across product pages, pricing, docs, changelogs, G2/Capterra reviews, and public roadmaps
- Builds a **structured competitor brief** for each company covering features, pricing, target market, strengths, weaknesses, and a direct comparison to your product
- Asks you to **review and correct** findings — accepts URLs to fix inaccurate claims
- Synthesizes everything into a **competitive landscape matrix** with feature comparison, pricing analysis, universal market gaps, strategic positioning, and ranked product opportunities

## Example Output

```
competition_researcher/
├── competitors/
│   ├── respond-io.md               ← Full brief: features, pricing, comparison
│   ├── infobip.md
│   ├── twilio.md
│   ├── zendesk.md
│   ├── aisensy.md
│   └── interakt.md
└── insights/
    └── competitive_landscape_matrix.md   ← Consolidated matrix across all competitors
```

See [`insights/competitive_landscape_matrix.md`](insights/competitive_landscape_matrix.md) for an example matrix researching WhatsApp Business Calling and Voice AI across 6 competitors.

## Prerequisites

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- A terminal / command line

### Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

## Getting Started

### 1. Set up your company context

Fill in the three files in `../company_context/` (one level up from this folder):

```
company_context/
├── company.md    # Your company overview, stage, capabilities, your role
├── persona.md    # User personas with roles, pain points, and quotes
└── product.md    # Deep-dive on the feature(s) you own as a PM
```

These are loaded automatically at the start of every session so agents can frame all comparisons relative to your product.

### 2. Launch Claude Code

Open your terminal in this directory and start Claude Code:

```bash
cd competition_researcher
claude
```

### 3. Follow the interactive prompts

Claude Code will guide you through the full workflow:

1. **What to research** — Describe the feature or domain (e.g., "broadcast campaigns", "AI chatbot builder", "pricing and packaging")
2. **Which competitors** — If no competitor profiles exist yet, provide at least 5. If profiles already exist, choose whether to add more.
3. **Parallel research** — Agents launch simultaneously, one per competitor. Each does deep web research and saves a structured brief.
4. **Review & correct** — Claude presents a summary and asks if anything is missing or wrong. Provide URLs to fix inaccurate findings.
5. **Landscape matrix** — Once you confirm accuracy, Claude generates the consolidated matrix in `insights/`.

## How the Research Works

Each competitor agent searches across:
- Official product and pricing pages
- Help docs, changelogs, and public roadmaps
- G2 and Capterra reviews
- Blog posts and press releases
- App Store / Google Play listings (for mobile feature gaps)

Agents distinguish between **GA features**, **beta/EAP**, and **announced-but-not-shipped** — and write "Not publicly documented" rather than guessing.

## Project Structure

```
competition_researcher/
├── CLAUDE.md           # Full execution protocol and output formats (loaded automatically)
├── README.md           # This file
├── competitors/        # One .md brief per competitor
└── insights/           # Competitive landscape matrix
```

## Customizing for Your Product

The `CLAUDE.md` file controls how Claude conducts research and formats output. You can adapt:

- **Competitor brief sections** — add or remove sections to match your team's workflow
- **Matrix rows** — change which features appear in the feature comparison table
- **Research depth** — add specific sources or review sites to check per industry
- **Segmentation dimensions** — customize how pricing tiers and target markets are analyzed

## License

MIT
