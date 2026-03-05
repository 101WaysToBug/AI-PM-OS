# Ticket Composer - Task/Ticket Generator

## What This Project Does

Ticket Composer's task generator creates **structured project tickets** (YouTrack or JIRA) from Notion documents, metric sheets, PRDs, or conversational input. Given a source document and context, it produces a well-structured ticket ready for engineering, data, or design teams to execute.

**Primary Output:** Draft tickets in YouTrack/JIRA that cross-functional teams use to plan and execute work.

## Product Context

**What is Wati?**
Wati is the #1 end-to-end WhatsApp API solution for SMBs, providing a low-code customer engagement SaaS platform built on the WhatsApp Business API. Wati empowers 8,000+ businesses across 100+ countries to deliver personalized, real-time conversations at scale.

**Core Platform Capabilities:**
- **WhatsApp Business Calling** - Voice calls directly within WhatsApp Business workflows, no app-switching required. Agents place calls from the chat dashboard for consultations, deal closures, and complex issue resolution.
- **Voice AI (Astra)** - AI agent that qualifies leads 24/7, handles technical support via WhatsApp Calling, and routes queries for instant resolution with contextual intelligence.
- **No-Code Chatbots** - AI-powered, human-like bots for every use case (FAQ handling, lead capture, broadcast campaigns).
- **Unified Inbox** - Manage WhatsApp, website chat, Instagram, Facebook, SMS, and calls from one dashboard.
- **Broadcast & Campaigns** - Segmented promotional announcements and personalized outreach at scale.

**Your Role:**
Product Manager responsible for WhatsApp Business Calling and Voice AI

**Company Stage:**
- Series B startup ($23M round led by Tiger Global, with Sequoia Capital India and DST Global Partners)
- $35M total raised
- 150+ employees
- Growing ARR (crossed $9.6M in 2024) with current ARR at $25M
- 15,000+ active business customers across 100+ countries

## User Personas

**Priya - Marketing Manager (D2C / E-commerce)**
- Role: Head of Marketing at a mid-size D2C brand (50-200 employees)
- Cares about: Broadcast campaigns, customer re-engagement, conversion rates, ROI on WhatsApp spend
- Pain points: Low open rates on email, can't personalize outreach at scale, no visibility into campaign performance
- Quote: "I need to reach my customers where they already are - on WhatsApp - and know exactly what's working."

**Rahul - Sales Director (SMB)**
- Role: Sales lead at a growing services company (20-80 employees)
- Cares about: Lead qualification speed, WhatsApp calling for high-touch sales, pipeline visibility, CRM integration
- Pain points: Leads go cold before the team responds, reps juggle multiple apps, no call analytics
- Quote: "If I can't call a hot lead directly from the chat within seconds, I've already lost them."

**Anita - Customer Support Lead**
- Role: Head of Support at an e-commerce or SaaS company (100-500 employees)
- Cares about: First-response time, AI-powered auto-resolution, ticket deflection, CSAT scores
- Pain points: Overwhelming ticket volume, repetitive FAQs draining agent time, no 24/7 coverage
- Quote: "Our customers expect instant answers on WhatsApp. We can't scale support by just hiring more agents."

**David - Business Owner / Founder (Small Business)**
- Role: Founder or CEO of a small business (5-30 employees)
- Cares about: Easy setup (no-code), affordability, all-in-one platform, quick time-to-value
- Pain points: Too many disconnected tools, no technical team to build integrations, limited budget
- Quote: "I just want one tool that lets me message, call, and automate - without needing a developer."

**Neha - Sales Executive (IC)**
- Role: Individual sales rep at an SMB or mid-market company, handling 50-100+ leads daily
- Cares about: Fast lead response, click-to-call from WhatsApp chat, conversation history at a glance, quick template replies
- Pain points: Switching between CRM, phone dialer, and WhatsApp; losing context mid-conversation; no way to prioritize hot leads in the inbox
- Quote: "By the time I copy a number, open the dialer, and call - the lead has already gone to a competitor."

**Vijay - Customer Support Agent (IC)**
- Role: Frontline support agent handling 40-60 WhatsApp conversations per shift
- Cares about: Canned responses, AI-suggested replies, easy ticket escalation, call handoff for complex issues
- Pain points: Repetitive queries eating up time, no AI assistance for drafting replies, manually tagging and routing conversations
- Quote: "I answer the same 10 questions a hundred times a day. If the bot handled those, I could actually solve the hard problems."

## Ticket Structure

When generating a task ticket, always include these sections in order:

1. **Summary** - A clear, prefixed title (e.g., `[Data] Build Dashboard for...`, `[Eng] Implement...`)
2. **Overview** - One-to-two paragraph description of what needs to be built and why
3. **Why This Matters** - Business justification for the work
4. **Acceptance Criteria** - Checklist of specific, testable conditions that define "done"

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
