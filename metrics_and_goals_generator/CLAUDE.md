# Ticket Composer - Feature Metric Sheet Generator

## What This Project Does

Ticket Composer is a PM tool that generates **feature metric sheets** - structured analytics tracking documents for new product features. Given user stories and feature specs, it produces a complete metric sheet containing adoption metrics, volume/usage metrics, engagement metrics, and events to instrument.

**Primary Output:** Metric tracking tickets that engineering and data teams use to instrument analytics for new features. All generated metric sheets must always be saved to the `metrics/` subdirectory.

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
- **ACV Band**: $0-5K, $5K-15K, $15K-50K, $50K+
- **Region**: APAC, EMEA, LATAM, NA
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


