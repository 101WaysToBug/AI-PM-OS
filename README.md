# AI PM OS

AI-powered tools that turn a Product Manager into an AI-Assisted Product Manager. Built on [Claude Code](https://docs.anthropic.com/en/docs/claude-code), these tools automate repetitive PM workflows — from generating analytics metric sheets to drafting JIRA/YouTrack tickets — so PMs can focus on strategy instead of formatting.

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

### 2. Task/Ticket Generator

Converts metric sheets, PRDs, or Notion documents into **execution-ready tickets** with testable acceptance criteria.

**Supported ticket prefixes:**
| Prefix | Team |
|--------|------|
| `[Data]` | Data/Analytics |
| `[Eng]` | Backend Engineering |
| `[FE]` | Frontend |
| `[Design]` | Design |
| `[DevOps]` | Infrastructure |
| `[QA]` | Quality Assurance |

**Usage:**
```bash
cd task_generator
claude
# Provide a source document (metric sheet, PRD, or Notion link), then ask:
# "Create a [Data] ticket to build the dashboard for this metric sheet"
```

Tickets are always created as **drafts first** so the PM can review before sharing with the team.

## Workflow

```
User Stories / PRD
        |
        v
[Metrics Generator] --> metrics/FEATURE-TRACKING.md
        |
        v
[Task Generator]    --> Draft Ticket (YouTrack / JIRA)
        |
        v
   PM Review --> Publish to Team
```

## Integrations

- **Notion** — fetch source PRDs and documents
- **YouTrack / JIRA** — create and manage draft tickets
- **GitHub** — version control for metric sheets and configs

## Prerequisites

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- (Optional) Notion MCP configured for fetching source documents
- (Optional) YouTrack MCP configured for ticket creation

## Customization

Both tools are driven by `CLAUDE.md` instruction files. You can adapt them to your own product by editing:

- **Product context** — company description, capabilities, stage
- **User personas** — names, roles, pain points, priorities
- **Segmentation dimensions** — plan tiers, ACV bands, regions
- **Writing style** — tone, formatting rules, terminology

## License

MIT
