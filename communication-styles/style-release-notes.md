# Communication Style: Release Notes

## Purpose
Clear, structured announcement of what changed in a release — aimed at users, stakeholders, or the broader team so they can quickly understand new capabilities, improvements, and breaking changes.

## Format Rules
- **Length:** As long as needed; one section per notable change (typically 200-500 words)
- **Tone:** Informative, neutral, slightly celebratory for big features
- **Structure:**
  - **Header:** Version number + date (e.g., `v1.2.0 — 2026-03-06`)
  - **Summary:** 1-3 sentence overview of the release theme
  - **Sections per change:** Use `## New:`, `## Improved:`, `## Fixed:`, `## Changed:`, `## Deprecated:`, `## Removed:` prefixes
  - **Bullets:** Concise descriptions under each section — lead with *what* changed, then *why* it matters
  - **Migration Notes:** If there are breaking changes or required actions, add a `## Migration Notes` section at the end
- **Include:** Feature names, brief context on value, links to docs where helpful
- **Avoid:** Internal jargon, implementation details, commit-level granularity, overly technical language
- **Focus:** What the user/stakeholder gains from the change

## Example

**Input:** We added a new dashboard with real-time analytics, fixed a bug where CSV exports silently dropped rows over 10K, improved search speed by 3x, and deprecated the v1 webhook format (removal in 90 days).

**Output:**

# Release Notes — v2.4.0 (2026-03-06)

## Summary

This release adds a real-time analytics dashboard, dramatically improves search performance, and fixes a data-loss bug in CSV exports.

---

## New: Real-Time Analytics Dashboard

A new dashboard gives you live visibility into key metrics — active users, feature adoption, and conversion rates — without waiting for overnight batch jobs. Available under **Settings → Analytics**.

- Updates every 30 seconds
- Filterable by date range, segment, and region
- Exportable as PNG or PDF

## Improved: Search Performance (3x Faster)

Search queries across projects and documents now return results up to 3x faster thanks to an updated indexing strategy. No action required — the improvement applies automatically.

## Fixed: CSV Export Dropping Rows

Exports with more than 10,000 rows were silently truncating data. This has been fixed — all rows are now included regardless of export size.

## Deprecated: v1 Webhook Format

The legacy v1 webhook payload format is now deprecated and will be removed in 90 days. Please migrate to the v2 format before June 2026. See the webhook migration guide for details.

---

## Migration Notes

- **Webhooks:** If you are still consuming v1 webhook payloads, switch to v2 before the removal date. The v2 format includes structured metadata and event typing.
