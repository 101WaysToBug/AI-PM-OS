# Feature Metric Sheet Generator

A PM tool powered by [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that generates **feature metric sheets** from user stories. Paste your user stories into the Claude Code terminal, and get a structured analytics tracking document ready for engineering and data teams.

## What It Does

Given user stories and feature specs, Ticket Composer produces a complete metric sheet containing:

- **Adoption Metrics** - Activation rates, toggle churn
- **Volume & Usage Metrics** - Absolute counts of feature usage
- **Engagement Metrics** - Interaction depth and frequency
- **Events to Instrument** - Grouped by lifecycle stage

All metrics are automatically segmented by Plan Type, ACV Band, Region, and Timestamp.

## Example Output

See [`metrics/CALL-ANALYTICS-TRACKING.md`](metrics/CALL-ANALYTICS-TRACKING.md) for a complete example of a generated metric sheet tracking Call Recording, Transcription, and Summarization features.

## Prerequisites

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- A terminal / command line

### Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/101WaysToBug/metrics-and-goals-generator.git
cd metrics-and-goals-generator
```

### 2. Launch Claude Code

Open your terminal in the project directory and start Claude Code:

```bash
claude
```

Claude Code will automatically load the project instructions from `CLAUDE.md`, which contain the metric sheet structure, formatting rules, and segmentation standards.

### 3. Paste your user stories

In the Claude Code window, paste your user stories and ask Claude to generate a metric sheet. For example:

```
Here are the user stories for our new Broadcast Scheduling feature:

- As a marketing manager, I want to schedule WhatsApp broadcasts for a future
  date and time so that I can plan campaigns in advance.
- As a marketing manager, I want to see a calendar view of all scheduled
  broadcasts so that I can avoid overlapping campaigns.
- As a marketing manager, I want to cancel or reschedule a pending broadcast
  so that I can adjust to changing business needs.
- As a marketing manager, I want to receive a confirmation notification when
  my scheduled broadcast is sent so that I know it went out successfully.

Please generate a feature metric sheet for this.
```

### 4. Review and save

Claude will generate a complete metric sheet following the project's standards and automatically save it to the `metrics/` subdirectory. You can:

- **It saves automatically** - All metric sheets are saved to `metrics/` (e.g., `metrics/BROADCAST-SCHEDULING-TRACKING.md`)
- Ask for **revisions** - adjust metrics, add events, or refine definitions
- Ask Claude to **iterate** on specific sections

### 5. Tips for best results

- **Be specific with user stories** - The more detail you provide, the more targeted the metrics will be.
- **Include the persona** - Mention which user persona the stories are for (e.g., "As a sales director..." vs "As a support agent...") so Claude can tailor metrics accordingly.
- **Provide context** - If the feature interacts with existing functionality, mention it so Claude can include relevant cross-feature metrics.
- **Ask for changes** - You can ask Claude to add, remove, or modify any section after generation.

## Project Structure

```
metrics-and-goals-generator/
├── CLAUDE.md                          # Project instructions (loaded automatically)
├── README.md                          # This file
└── metrics/                           # Generated metric sheets
    └── CALL-ANALYTICS-TRACKING.md     # Example: Call Recording metrics
```

## Customizing for Your Product

The `CLAUDE.md` file contains all the rules Claude follows when generating metric sheets. Open it in any text editor and update the following sections to match your company and PM role.

### 1. Product Context

Replace the existing Wati-specific context with your own company details:

- **"What is [Your Company]?"** - Write a 2-3 sentence description of your product and who it serves.
- **Core Platform Capabilities** - List 3-5 top-level features of your platform. These help Claude understand what kinds of metrics and events make sense for your product.
- **"Your Role"** - Change this to reflect your actual PM scope (e.g., "Product Manager responsible for Checkout and Payments" or "PM for Growth and Activation"). This tells Claude which product area to focus metrics on.
- **Company Stage** - Update funding, headcount, ARR, and customer count. Claude uses this to calibrate metric sophistication (e.g., a seed-stage startup may not need ACV-band segmentation).

### 2. User Personas

Replace the example personas with your own. For each persona, include:

- **Name and role** (e.g., "Alex - Engineering Manager")
- **Company size** they work at
- **What they care about** - 3-4 priorities relevant to your feature area
- **Pain points** - What frustrates them today
- **Quote** - A one-liner that captures their mindset

Claude uses these personas to tailor metric definitions and ensure the tracking plan covers the right user journeys.

### 3. Segmentation Dimensions

Update the default segmentation values to match your business model:

- **Plan Type** - Replace `Growth / Pro / Business / Enterprise` with your actual plan tiers (e.g., `Free / Starter / Team / Enterprise`).
- **ACV Band** - Adjust the dollar ranges to reflect your pricing (e.g., `$0-1K, $1K-10K, $10K-50K, $50K+`).
- **Region** - Change `APAC, EMEA, LATAM, NA` if your business uses different regional groupings.
- **Additional dimensions** - Add any company-specific segments (e.g., `Industry`, `User Role`, `Cohort`) in the Segmentation Dimensions section and the Immutable Rules.

### 4. Metric Sheet Structure

Add or remove sections from the metric sheet template to fit your team's workflow:

- If your team doesn't track **Dependencies** or **Out of Scope**, remove them.
- If you need a **Funnel Metrics** or **Revenue Impact** section, add it to the ordered list.

### 5. Product Terminology

Update the **Product Terminology** section with terms specific to your company (e.g., "Workspace" vs "Organization", "Member" vs "User") so generated metric sheets use consistent language.

### 6. Writing Style

Adjust tone and formatting rules if your team prefers a different documentation style (e.g., numbered lists instead of bullets, different voice conventions).

## License

MIT
