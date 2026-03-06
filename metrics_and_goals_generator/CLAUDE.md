# Ticket Composer - Feature Metric Sheet Generator

> **Before starting any task, load the company context from ****`../company_context/company.md`****, ****`../company_context/persona.md`****, and ****`../company_context/product.md`****.**

## What This Project Does

Ticket Composer is a PM tool that generates **feature metric sheets** - structured analytics tracking documents for new product features. Given user stories and feature specs, it produces a complete metric sheet containing adoption metrics, volume/usage metrics, engagement metrics, and events to instrument.

**Primary Output:** Metric tracking tickets that engineering and data teams use to instrument analytics for new features. All generated metric sheets must always be saved to the `metrics/` subdirectory.

## Metric Sheet Structure

When generating a feature metric sheet, always include these sections in order:

1. **Header** - Type, Priority, Product Area, Owner, Labels, Plan
2. **Summary** - One-paragraph description of what we are tracking and why
3. **Why This Matters** - Business justification for the instrumentation
4. **Segmentation Dimensions** - Always include: Plan Type, ACV Band, Region, Timestamp (daily/weekly/monthly)
5. **Adoption Metrics** - Activation rates, toggle churn (2-column table: Metric, Definition)
6. **Volume & Usage Metrics** - Absolute counts of feature usage (2-column table: Metric, Definition)
7. **Engagement Metrics** - Interaction depth and frequency (2-column table: Metric, Definition)
8. **Events to Instrument** - Grouped by lifecycle stage (2-column table: Event Name, Trigger)
9. **Dependencies** - What must exist before this work can begin
10. **Out of Scope** - Explicitly excluded items

## Metric Sheet Rules

**Table Format:**
- Metrics tables use 2 columns only: Metric and Definition (no Target, no Properties, no Segmentation columns)
- Event tables use 2 columns only: Event Name and Trigger (no Properties column)
- Segmentation dimensions (Plan Type, ACV Band, Region, Timestamp) are defined once at the top and apply to all metrics

**Segmentation (always include):**
- **Plan Type**: Growth / Pro / Business / Enterprise
- **ACV Band**: $0–1K, $1K–3K, $3K–5K, $5K-10K, $10K+
- **Region**: India, ROW, LATAM, GCR, Europe
- **Timestamp**: Daily, weekly, monthly roll-ups

**Content Rules:**
- Derive metrics directly from the user stories provided
- Group events by lifecycle stage (configuration → execution → processing → consumption → dashboard)

## Writing Style

**Tone:**
- Clear and outcome-focused
- Active voice (not passive)
- Concise (2-sentence max paragraphs for most content)
- Use "we" not "I" in documentation
- Avoid jargon unless it's standard PM terminology

**Formatting:**
- Always use Oxford commas
- Use bullet points for lists (not numbered unless sequence matters)
- Bold key terms on first use
- Include "Why this matters" sections

## Product Terminology

**Required Terms:**
- "PM" = Product Manager (not Project Manager)
- "ACV" = Annual Contract Value
- "Metric Sheet" = the analytics tracking document we generate (not "spec" or "PRD")

## Immutable Rules

**ALWAYS:**
- Save generated metric sheets to the `metrics/` subdirectory (e.g., `metrics/FEATURE-NAME-TRACKING.md`)
- Include all four segmentation dimensions (Plan Type, ACV Band, Region, Industry, Timestamp)
- Keep tables to 2 columns (no Target, Properties, or Segmentation columns)
- Group events by lifecycle stage
- Derive metrics from the user stories provided
- Generate **Volume & Usage Metrics** for every metric sheet (absolute counts such as total calls, messages sent, sessions created, etc.)

**NEVER:**
- Add Properties columns to event tables
- Add Target or Segmentation columns to metric tables
- Skip the "Why This Matters" section
- Forget region and timestamp in segmentation
- Use passive voice in metric definitions
- Omit the Volume & Usage Metrics section from any metric sheet


