# Task/Ticket Generator

A PM tool powered by [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that generates **structured project tickets** (YouTrack or JIRA) from source documents. Provide a metric sheet, PRD, or Notion doc, and get a draft ticket with acceptance criteria ready for engineering, data, or design teams.

## What It Does

Given a source document and target team, the Task Generator produces a complete ticket containing:

- **Summary** - Prefixed title with target team tag (e.g., `[Data]`, `[Eng]`, `[FE]`)
- **Overview** - What needs to be built and why, linked to the source document
- **Why This Matters** - Business justification connecting work to outcomes
- **High-Level Approach** - Recommended implementation strategy and key architecture decisions
- **Acceptance Criteria** - Specific, testable checklist defining "done"

All tickets are created as **drafts** so the PM can review before sharing with the team.

## Supported Ticket Types

| Prefix | Team |
|--------|------|
| `[Data]` | Data/Analytics (dashboards, pipelines, queries) |
| `[Eng]` | Backend Engineering (APIs, services, infrastructure) |
| `[FE]` | Frontend (UI components, UX changes) |
| `[Design]` | Design (mockups, prototypes, design systems) |
| `[DevOps]` | Infrastructure and deployment |
| `[QA]` | Testing and quality assurance |

## Prerequisites

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- A source document (metric sheet, PRD, or Notion link)

### Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

## Getting Started

### 1. Navigate to the project

```bash
cd task_generator
```

### 2. Launch Claude Code

```bash
claude
```

Claude Code will automatically load the project instructions from `CLAUDE.md`.

### 3. Provide a source document and request a ticket

In the Claude Code window, provide your source document and specify the target team:

```
Here is the metric sheet for our Call Analytics feature:
[paste metric sheet or provide Notion link]

Please create a [Data] ticket to build the analytics dashboard for this.
```

### 4. Review the draft

Claude will generate a complete ticket following the project's standards. You can:

- Ask for **revisions** — adjust acceptance criteria, refine the approach, or change scope
- Request **multiple tickets** — split work across teams (e.g., `[Eng]` for the API + `[Data]` for the dashboard)
- Ask Claude to **iterate** on specific sections

### 5. Tips for best results

- **Specify the target team** — Include the team prefix (e.g., `[Data]`, `[Eng]`) so Claude structures the ticket appropriately.
- **Provide rich source documents** — The more detailed your metric sheet or PRD, the more precise the acceptance criteria will be.
- **Mention dependencies** — If the work depends on other teams or existing infrastructure, mention it so Claude can include it in the ticket.
- **Ask for multiple tickets** — If a feature requires work from several teams, ask Claude to generate separate tickets for each.

## Project Structure

```
task_generator/
├── CLAUDE.md    # Project instructions (loaded automatically)
└── README.md    # This file
```

## Customizing for Your Product

The `CLAUDE.md` file contains all the rules Claude follows when generating tickets. Open it in any text editor and update the following sections to match your company and PM role:

- **Product Context** — Replace with your company description, capabilities, and stage
- **User Personas** — Update with your own personas, their roles, pain points, and priorities
- **Ticket Structure** — Add or remove sections to fit your team's workflow
- **Summary Prefixes** — Add custom team tags if your org uses different labels
- **Product Terminology** — Update with terms specific to your company

## License

MIT
