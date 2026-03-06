# Product Context — WhatsApp Business Calling & Voice AI

## WhatsApp Business Calling

### What It Is

WhatsApp Business Calling enables voice calls directly inside Wati's platform, built on Meta's WhatsApp Calling API. Agents place and receive calls from the chat dashboard — no app-switching, no separate dialer. Customers see a verified business name and badge during calls, and all calls are end-to-end encrypted.

### Plan Availability

Available on **Growth**, **Pro**, and **Business** plans.

### Core Capabilities

- **One-Click Call from Chat** — Initiate voice calls directly from the WhatsApp conversation window
- **Inbound & Outbound Calls** — Both business-initiated calls (BIC) and user-initiated calls (UIC) supported
- **Call CTA Buttons** — Add "Call Now" buttons to WhatsApp templates, messages, catalogs, and broadcasts
- **Call Deep Links** — Embed call links in websites and emails to trigger WhatsApp calls
- **Business Hours Control** — Define availability windows so calls only come through when the team is ready
- **Interactive Call Permission Templates** — Obtain explicit customer consent before outbound calls (Meta compliance requirement)
- **Verified Business Badge** — Customers see verified business identity during calls
- **Multi-Number Management** — Manage multiple WhatsApp numbers from a single dashboard
- **Missed Call Notifications** — Alerts for missed inbound calls with optional auto-permission request

### Call Flow

**Inbound Calls:**
- Incoming calls appear as a dialog box in the bottom-left corner of the Wati inbox
- All active operators and admins see the call simultaneously; first to answer gets connected
- Agents can receive up to 3 simultaneous incoming calls (but can only be on 1 active call at a time)
- Visibility restricted to operators assigned to the contact's team

**Outbound Calls:**
- Customers must grant permission before the business can call them
- Permission options: allow calls indefinitely, allow temporarily (7-day window), or deny
- If the chat window is closed, a call permission template is sent (billed as a utility template by Meta)
- If the chat window is open, a free-form permission message can be sent instead
- After approval, agents click "Call customer" to initiate

**During a Call:**
- "On Call" status indicator displayed
- Window can be minimized to continue other tasks
- Call details logged in the customer's conversation window post-call

### Restrictions & Guidelines

**Geographic Restrictions:**
- Business-Initiated Calls (BIC) **not available** in: USA, Canada, Egypt, Vietnam, Nigeria
- User-Initiated Calls (UIC) available wherever the Cloud API operates
- Business phone number's country code must belong to a supported country; customer can be from any Cloud API region

**Eligibility Requirements:**
- Business must have a messaging limit of at least **2,000 business-initiated conversations** in a rolling 24-hour period

**Call Frequency Limits:**
- Max **5 connected calls every 24 hours** per contact
- After 2 consecutive unanswered calls: system sends a reconsideration message
- After 4 consecutive unanswered calls: permission automatically revoked

**Permission Request Limits:**
- 1 permission request every 24 hours, max 2 requests per 7 days
- Limits reset after any connected call occurs
- 7-day window to call after contact approves
- 24-hour wait before resending after a decline

**Concurrency Limits:**
- **1,000 concurrent inbound** and **1,000 concurrent outbound** calls per business phone number

**Platform Restrictions:**
- Available only on the Wati web platform
- No API access to call recordings or transcriptions
- Not supported for co-existence accounts

### Pricing & Billing

- **Inbound calls:** Free
- **Outbound calls:** Charged per minute based on connected call duration, deducted from Wati wallet
- **Free credits:** $1 in free credits on first activation (~10 minutes of outbound calling)
- **Minimum balance:** ₹500 (INR plans) or $10 (USD plans) required to initiate outbound calls
- **Shared wallet:** WhatsApp Calling shares the same wallet as Campaigns
- **No charge** for calls that don't connect, are busy, or go unanswered
- If balance depletes mid-call, the call continues until manually ended (may result in negative balance)

### Request Accepted View

A dedicated tab (Team Inbox > WhatsApp Calls > Request Accepted) that shows all contacts with active outbound call permission. Agents use this as a ready-to-call queue instead of checking individual chats.

- Displays only contacts with valid permissions within the 7-day window; expired permissions auto-hide
- If a contact initiates an inbound call (even missed), WhatsApp treats it as callback permission — they appear automatically
- Real-time updates: new permissions appear immediately, expired ones disappear
- Clicking a contact opens their chat in the center panel for context review before calling
- Designed for sales teams, marketing, and support conducting WhatsApp outreach

### Call Permission Template Localization

Businesses can send call permission requests in recipients' preferred languages via auto-generated, language-specific templates.

- Templates follow the naming format: `whatsapp_call_permission_request_{language_acronym}` (e.g., `_hi` for Hindi)
- To generate: Settings > Team Inbox Settings > Call tab > select language from dropdown > Save — template is auto-created
- Per-line customization: set different languages for each WhatsApp Business number
- Previously generated templates persist even after switching language
- Most recently selected language becomes the default for Team Inbox requests
- Campaign integration: select the localized template when creating a campaign via Campaigns > Template Messages

### Voice Call CTA in Templates

A button added to WhatsApp templates that lets recipients start a call directly from the message.

- Two CTA types: **WhatsApp Voice Call CTA** (calls within WhatsApp) and **Telephony Call CTA** (standard phone call)
- Setup: Campaigns > Template Messages > WhatsApp > New Template Message > Add Button CTA under WhatsApp Voice Call section
- Templates require Meta approval after adding CTAs before deployment
- Multi-number support: select the specific WhatsApp number when creating the template
- Prerequisite: WhatsApp Calling must be enabled before creating templates with voice call CTAs

### Call Availability & Notifications

Operators control call interruptions through notification management without losing call history.

- Access: Profile icon > Manage Notifications > Call tab
- **Available to take calls** toggle: master control for call notifications and audio alerts
  - ON: receive all call notifications and audio alerts
  - OFF: hides all call notifications and silences ringing — no alerts appear
- **Ringing sound** checkbox: silence audio while remaining visually notified (toggle must be ON)
- Disabling notifications does not delete incoming calls — they remain in the "Incoming Calls" section for later review
- Settings control only notifications and availability status, not call data storage

### Analytics

**Access:** Team Inbox > Call icon for logs; dedicated analytics dashboard for metrics.

**Call Logs:**
- Filter by "Missed" and "All Call Logs"
- Tracked per call: timestamp, caller name, called phone number, agent who handled the call

**Analytics Dashboard Metrics:**
- **Total call volume** — total outbound attempted, inbound, and missed calls
- **Outbound connected** — outbound calls answered and connected
- **Outbound attempted** — all outbound calls tried
- **Inbound calls** — inbound calls received and answered
- **Missed calls** — inbound calls not answered
- **Average call duration** — average length of all answered inbound and outbound calls
- **Agent performance** — per-agent breakdown for comparing performance and identifying training opportunities

**Filters & Export:**
- Period dropdown for predefined date ranges, plus custom date filters (From/To)
- Multi-number selection for accounts with multiple WhatsApp Business numbers
- **CSV download** via the three-dot menu (⋮) on top right
- **Scheduled reports** — automatic weekly delivery with configurable timezone and day

### Key Use Cases

- **Sales & Lead Conversion** — Instant follow-ups from chat, real-time consultations, campaign-driven call CTAs
- **Customer Support** — Escalate text issues to voice for faster resolution of complex problems
- **Collections & Renewals** — Compliant outbound calling with consent verification
- **Appointments** — Confirm/reschedule via WhatsApp calls, post-consultation check-ins

### Business Impact Benchmarks

- 10–15x higher revenue from voice calls than web leads
- 76% of consumers want to seamlessly switch between messaging and calling
- 30% faster conversion through calls
- 28% higher retention among callers

---

## Voice AI (Astra)

### What It Is

Astra is Wati's AI agent platform that automates customer interactions across Web, WhatsApp, and Voice channels. It features a near-human voice engine with zero latency, infinite context, and support for 30+ languages with live language switching and accent adaptation.

### Core Capabilities

- **No-Code Builder** — Describe what you need in natural language to build and deploy AI agents
- **Multi-Channel Deployment** — Deploy to Web, WhatsApp, and Voice from a single configuration with continuous memory across all touchpoints
- **Near-Human Voice** — Listens, pauses, and responds like a real human with empathy and precision
- **30+ Languages** — Live language switching with accent adaptation
- **AI Actions** — Books meetings, updates CRMs, triggers workflows through connected tools
- **Lead Qualification** — Converts conversations into qualified leads with clear insights

### Key Use Cases

- **Lead Qualification** — Qualifies leads 24/7 via WhatsApp and voice
- **Customer Support** — Handles technical support, FAQ resolution, and ticket deflection
- **Sales** — Product recommendations, instant engagement, guided purchase flows
- **Routing** — Routes complex queries to human agents with full context

### Integrations

Deep integrations with Wati, HubSpot, Salesforce, Shopify, and other business tools.

### Performance Metrics

- 100% instant response rate
- 24/7 availability
- 99% user satisfaction
