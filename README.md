# AI PM OS

AI-powered tools that turn a Product Manager into an AI-Assisted Product Manager. Built on [Claude Code](https://docs.anthropic.com/en/docs/claude-code), these tools automate repetitive PM workflows — from generating analytics metric sheets to synthesizing user feedback — so PMs can focus on strategy instead of formatting.

## Tools

### 1. Metrics & Goals Generator

Transforms user stories and feature specs into structured **feature metric sheets** ready for engineering and data teams.

**What it generates:**
- **Adoption Metrics** — activation rates, toggle churn, feature uptake
- **Volume & Usage Metrics** — absolute counts of feature usage
- **Engagement Metrics** — interaction depth and frequency
- **Events to Instrument** — grouped by lifecycle stage (configuration, execution, processing, consumption, dashboard)
- **Segmentation Dimensions** — Plan Type, ACV Band, Region, Timestamp

**Usage:**
```bash
cd metrics_and_goals_generator
claude
# Paste your user stories, then ask:
# "Generate a feature metric sheet for this"
```

Output is saved as markdown to `metrics/FEATURE-NAME-TRACKING.md`.

### 2. Nugget Synthesizer

Transforms raw user feedback — support tickets, meeting notes, survey responses, and sales notes — into structured **insight reports** with cross-source analysis.

**What it generates:**
- **Top Pain Points** — ranked by cross-source frequency with supporting quotes
- **Demand Data** — survey results segmented by role
- **Competitive Intelligence** — lost deals, competitors, and revenue impact
- **Use Cases** — support ticket themes categorized by scenario
- **Feature Requests** — prioritized by impact vs. effort
- **Recommended Next Steps** — specific, actionable recommendations

**How it works:** Four parallel agents (Meeting Notes, Survey, Support, Sales) each produce a persisted analysis file, then a consolidation step merges all four into one unified synthesis.

**Usage:**
```bash
cd nugget-synthesizer
claude
# Add feedback files to source directories, then ask:
# "Synthesize the feedback on WhatsApp Calling"
```

Output is saved to `insights/` — 4 agent analyses + 1 final synthesis report.

## Companion Skills

These standalone Claude Code skills complement AI PM OS:

| Skill | What it does |
| --- | --- |
| [/communicate](https://github.com/101WaysToBug/communicate) | Transforms content into Executive Email, Slack Update, Notion Doc, or Release Notes |
| [/generate-ticket](https://github.com/101WaysToBug/generate-ticket) | Generates structured project tickets (YouTrack/JIRA) from user stories, PRDs, or metric sheets |
| [/one-pager-PRD](https://github.com/101WaysToBug/one-pager-PRD) | Generates a one-pager PRD using Lenny Rachitsky's framework |

## Workflow

```
User Stories / PRD
        |
        v
[Metrics Generator] --> metrics/FEATURE-TRACKING.md
        |
        v
[/generate-ticket]  --> Draft Ticket (YouTrack / JIRA)
        |
        v
   PM Review --> Publish to Team

User Feedback (tickets, notes, surveys, sales)
        |
        v
[Nugget Synthesizer] --> insights/TOPIC-synthesis.md
        |
        v
   PM Review --> Inform Roadmap

Any Content (findings, updates, decisions)
        |
        v
[/communicate skill]  --> Executive Email + Slack + Notion + Release Notes
        |
        v
   PM Review --> Share with Stakeholders
```

## Integrations

- **Notion** — fetch source PRDs and documents
- **YouTrack / JIRA** — create and manage draft tickets
- **GitHub** — version control for metric sheets and configs

## Prerequisites

- A paid [Claude](https://claude.ai) subscription (Pro, Max, Team, or Enterprise) — Claude Code is not available on the free plan
- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- (Optional) Notion MCP configured for fetching source documents
- (Optional) YouTrack MCP configured for ticket creation

## Setting Up Your Company Context

All tools load shared context from a `company_context/` folder at the root level. This keeps company, persona, and product information in one place instead of duplicating it across every tool's `CLAUDE.md`.

```
company_context/
├── company.md    # Company overview, stage, capabilities, your role
├── persona.md    # User personas with roles, pain points, and quotes
└── product.md    # Deep-dive on the feature(s) you own as a PM
```

**To adapt AI PM OS to your own company:**

1. **Create \****`company_context/company.md`** — Describe your company: what it does, core platform capabilities, your role, company stage (funding, ARR, team size, customer count).

2. **Create \****`company_context/persona.md`** — Define 4-6 user personas relevant to your product area. For each persona include: role, company size, what they care about, pain points, and a representative quote.

3. **Create \****`company_context/product.md`** — Document the specific feature(s) you own: capabilities, user flows, restrictions, pricing, analytics, and key use cases. Source this from your product's support docs, help center, or internal specs.

4. **Each tool's \****`CLAUDE.md`**\*\* loads this context automatically** at the start of every session. The instruction at the top of each `CLAUDE.md` tells Claude Code to read all three files before beginning any task:

   > Before starting any task, load the company context from `../company_context/company.md`, `../company_context/persona.md`, and `../company_context/product.md`.

## Further Customization

Each tool's `CLAUDE.md` file controls its specific behavior. You can adapt:

- **Segmentation dimensions** — plan tiers, ACV bands, regions
- **Writing style** — tone, formatting rules, terminology
- **Output structure** — sections, table formats, report templates
- **Immutable rules** — guardrails for what the tool should always/never do

## License

MIT
