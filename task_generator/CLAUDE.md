# Ticket Composer - Task/Ticket Generator

> **Before starting any task, load the company context from ****`../company_context/company.md`****, ****`../company_context/persona.md`****, and ****`../company_context/product.md`****.**

## What This Project Does

Ticket Composer's task generator creates **structured project tickets** (YouTrack or JIRA) from Notion documents, metric sheets, PRDs, or conversational input. Given a source document and context, it produces a well-structured ticket ready for engineering, data, or design teams to execute.

**Primary Output:** Draft tickets in YouTrack/JIRA that cross-functional teams use to plan and execute work.

## Ticket Structure

When generating a task ticket, always include these sections in order:

1. **Summary** - A clear, prefixed title (e.g., `[Data] Build Dashboard for...`, `[Eng] Implement...`)
2. **Overview** - One-to-two paragraph description of what needs to be built and why
3. **Why This Matters** - Business justification for the work
4. **High-Level Approach** - A brief technical or strategic approach outlining how the team should tackle this work. Include key architecture decisions, suggested implementation steps, or recommended tools/frameworks without being overly prescriptive.
5. **Acceptance Criteria** - Checklist of specific, testable conditions that define "done"

### Optional Sections (include when relevant):
- **Dependencies** - What must exist before this work can begin
- **Out of Scope** - Explicitly excluded items
- **Source Document Link** - URL to the Notion doc, metric sheet, or PRD this ticket derives from

## Ticket Generation Rules

**Summary Prefixes (use based on target team):**
- `[Data]` - Data/analytics team work (dashboards, pipelines, queries)
- `[Eng]` - Engineering/backend work (APIs, services, infrastructure)
- `[FE]` - Frontend work (UI components, UX changes)
- `[Design]` - Design work (mockups, prototypes, design systems)
- `[DevOps]` - Infrastructure and deployment work
- `[QA]` - Testing and quality assurance work

**Acceptance Criteria Rules:**
- Write as a checklist using `- [ ]` markdown format
- Each criterion must be specific, measurable, and testable
- Bold the key deliverable or component name in each criterion
- Include non-functional criteria where relevant (performance, access control, data refresh cadence)
- Derive criteria directly from the source document provided
- Group related criteria logically (e.g., all metric-related items together, all UX items together)

**Source Document Handling:**
- Always link back to the source Notion doc or metric sheet in the Overview section
- Extract requirements from the source document rather than inventing them
- When the source doc has detailed specs (metrics, events, schemas), summarize in the ticket and reference the full doc
- Do not duplicate the entire source document into the ticket - keep it concise

**Content Rules:**
- Keep the Overview to 2 paragraphs max
- "Why This Matters" should be 2-4 sentences connecting the work to business outcomes
- Acceptance criteria should cover functional requirements, non-functional requirements (performance, access), and data/integration requirements
- Include export/reporting criteria for data-related tickets

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
- Use markdown checklists (`- [ ]`) for acceptance criteria

## Product Terminology

**Required Terms:**
- "PM" = Product Manager (not Project Manager)
- "ACV" = Annual Contract Value
- "Metric Sheet" = the analytics tracking document (not "spec" or "PRD")

## Immutable Rules

**ALWAYS:**
- Include an **Overview** section with a link to the source document
- Include a **Why This Matters** section connecting work to business outcomes
- Include a **High-Level Approach** section outlining the recommended implementation strategy
- Include **Acceptance Criteria** as a testable checklist
- Prefix the summary with the target team tag (e.g., `[Data]`, `[Eng]`)
- Link back to the source Notion doc or metric sheet
- Create tickets as **drafts** first (not published) so the PM can review before sharing

**NEVER:**
- Skip the "Why This Matters" section
- Write vague acceptance criteria (e.g., "dashboard works well")
- Duplicate the entire source document into the ticket body
- Use passive voice in acceptance criteria
- Publish tickets directly without creating as draft first
- Invent requirements not present in the source document
