# Competitor Brief: Respond.io

Last Updated: March 2026
Analyst: Wati Product Team



## Overview

Respond.io is an AI-powered customer conversation management platform founded in 2017 by Gerardo Salandra, Hassan Ahmed, and Iaroslav Kudritskiy. Headquartered in Malaysia, the company raised $7 million in a Series A round in September 2022 led by Headline Asia, with participation from AltaIR Capital, Smart Partnership Capital, Sterling Oak Group, and Calendula Ventures, bringing total funding to approximately $8.8 million. As of 2025, the company reports approximately $18.5 million in ARR, 169 employees, and 10,000+ brand customers across 126 countries including notable enterprise names such as Toyota, McDonald's, British Airways, Radisson, Hertz, Klook, and Decathlon.

Respond.io positions itself as an omnichannel, AI-first conversation platform built for B2C companies. Its core angle is unifying all customer messaging channels — WhatsApp, Facebook Messenger, Instagram, TikTok, email, webchat, and VoIP — into a single AI-powered inbox. Unlike Wati, which is focused almost exclusively on the WhatsApp ecosystem for SMBs, Respond.io targets mid-market to enterprise B2C businesses that need multi-channel orchestration, workflow automation, and AI agents that work across text and voice simultaneously.

The company launched "Respond 3.0" in March 2024, a significant platform redesign, followed by a major Voice AI Agent announcement in January 2026. This trajectory — from shared inbox to full conversational AI platform including native WhatsApp Business Calling API support and Voice AI — makes Respond.io one of the most directly relevant competitors to Wati's own WhatsApp Calling and Astra Voice AI roadmap. G2 reviewers rate Respond.io at 4.8/5, and G2 itself lists Wati as Respond.io's top alternative, confirming direct head-to-head competition.



## Key Features

### WhatsApp Calling

Respond.io has native integration with Meta's WhatsApp Business Calling API and is one of the few BSPs (Business Solution Providers) to publicly document full support for this feature:

- **Inbound calls**: Businesses can receive incoming WhatsApp calls from customers directly within the Respond.io inbox
- **Outbound calls**: Agents can initiate outbound WhatsApp calls to contacts using the business's WhatsApp number; billed per minute by Meta with rates that vary by destination country and volume (charged in 6-second increments)
- **Call recording**: All WhatsApp calls are recorded; Respond.io automatically generates transcripts of recorded calls (transcription available on Growth plan and above)
- **AI-generated call summaries**: Automatic post-call summaries with highlights, action items, and next steps
- **AI Voice Agent for inbound calls**: AI agents can automatically answer inbound WhatsApp calls, greet callers, collect information, and qualify leads; calls are capped at 3 minutes for AI-handled interactions (Voice AI available on Advanced plan and above)
- **Call-to-human transfer**: Real-time call handover from AI agent to a live human agent, passing full call transcript and chat history
- **Call analytics**: Track total calls, call duration, and team call activity metrics
- **Missed call automation**: Trigger automated workflows when a call is missed — send acknowledgment messages, share business hours, assign follow-ups, or tag conversations
- **Business hours via Meta Business Suite**: Calls received outside configured hours are auto-rejected by Meta and do not count against pickup rate
- **Workflow triggers on calls**: Automated workflows can be triggered post-call (completed call, missed call, or permission request events)
- **Unified inbox**: WhatsApp calls, Messenger calls, and VoIP calls appear in the same conversation thread as text messages and emails
- **Permission-gated outbound calling**: Businesses must send a call permission request first; customers must approve; one request per 24 hours, max two per week to the same customer
- **No setup fees or per-call markups**: Respond.io passes through Meta's official per-minute rates with no added markup
- **Outbound calling requires messaging threshold**: Business WhatsApp number must have a minimum messaging limit of 2,000 business-initiated conversations per rolling 24-hour period to enable WhatsApp calling
- **Call CTA buttons in templates**: Interactive message templates support call-to-action buttons including calling prompts (part of WhatsApp interactive message framework)

Note: Wati's WhatsApp Calling page (as of research date) is live; Respond.io's own competitor comparison blog post noted that "Wati hasn't announced supporting WhatsApp Business Calling API" — this claim appears outdated given Wati's current feature set, and should be monitored.

### Voice AI / Conversational AI

Respond.io launched Voice AI Agents in January 2026, positioning them as a replacement for legacy IVR systems:

- **Human-like voice responses**: Voice AI agents answer inbound calls with natural, human-sounding voices using ElevenLabs Flash v2.5 as the underlying TTS model
- **32 languages supported**: Automatic language detection and in-call language switching based on the caller's spoken language
- **Natural language understanding**: Agents understand conversational speech, can ask follow-up questions, and collect structured information in real time (not a press-1/press-2 IVR)
- **Preconfigured templates**: Ready-made AI agent templates for Sales Agent, Support Agent, and AI Receptionist — with common conversation flows and best practices pre-built (no-code quick-start)
- **AI Agent Actions**: Voice AI agents can update CRM fields, change contact lifecycle stages, add internal notes, send HTTP requests to external systems (e.g., booking tools, order platforms), and route qualified leads to human agents
- **Lead qualification on voice**: AI asks qualifying questions, collects prospect details, and passes only qualified leads to human sales agents with full call context
- **Meeting/appointment booking**: AI agents can send booking links during calls and integrate with external scheduling tools
- **Built-in guardrails**: AI will not handle payments or make binding business commitments; designed for predictable, safe first-contact handling
- **Multimodal AI Orchestrator**: Underlying AI Orchestrator coordinates micro-agents specialized in retrieval, routing, and actions; handles text, images, audio, and files in parallel
- **Available on Advanced plan and above only**: Voice AI for calls is gated to the $279/month Advanced plan; chat-only AI agents are available from the $159/month Growth plan
- **24/7 availability**: AI agents handle calls outside business hours automatically
- **Failure branches**: Two explicit failure branches when AI cannot resolve: "Speak to Human" or "AI is Unable to Answer" — ensuring graceful handover rather than dropped calls
- **Call cap**: AI-handled inbound WhatsApp calls are currently capped at 3 minutes per interaction

### Core Platform Capabilities

- **Omnichannel inbox**: Unifies WhatsApp, Facebook Messenger, Instagram DMs, TikTok messaging, email, website live chat, VoIP, and WhatsApp/Messenger voice calls in a single shared team inbox
- **Visual workflow automation**: Drag-and-drop workflow builder for routing, tagging, auto-assignment, escalation, and complex multi-step business process automation; single unified workflow canvas (vs. Wati's flow builder, which some reviewers find more limited)
- **CRM integrations**: Native integrations with HubSpot, Salesforce, Zoho; also supports Zapier and direct API; AI agents can push data to CRMs in real time during conversations
- **Broadcast and campaigns**: Bulk WhatsApp message broadcasting with segmentation and personalization; advanced targeting available on Growth and above
- **Analytics and reporting**: Built-in performance dashboards for response times, conversion rates, call metrics, and agent performance; custom reporting on Advanced plan
- **Meta Product Catalog integration**: WhatsApp commerce via Meta product catalog (launched April 2024)
- **Mobile app**: iOS/Android app with inbound and outbound calling, AI Assist for drafting replies, real-time message translation
- **3,000+ integrations**: Via Zapier and API ecosystem

### Notable Strengths

- Full native WhatsApp Business Calling API support with AI voice agents — one of the most complete implementations among BSPs
- Unified omnichannel inbox across 10+ channels including voice, chat, email, and social — far broader channel coverage than Wati
- AI Orchestrator architecture (multi-agent, multi-modal) built for reliability at scale, with published uptime of 99.999%
- Strong enterprise brand credibility (Toyota, McDonald's, British Airways, Decathlon) while also serving SMBs
- Transparent pricing with no per-call markups and no hidden fees on WhatsApp calling rates

### Missing / Weak Areas (vs. Wati)

- **Voice AI gated to highest self-service tier**: Voice AI agents require the Advanced plan at $279/month — significantly more expensive than Wati's approach where WhatsApp Calling is available across Growth, Pro, and Business plans
- **No documented outbound AI voice calling**: Respond.io's Voice AI handles inbound calls only (AI answers calls); there is no publicly documented capability for AI-initiated outbound voice call campaigns comparable to Wati's Astra outbound model
- **3-minute AI call cap**: Inbound WhatsApp calls handled by AI are capped at 3 minutes, which may be insufficient for complex sales or support conversations
- **Outbound calling permission friction**: The "call permission request" requirement (max 2 per week per customer) significantly limits outbound call volume and use cases, reducing the utility for high-volume outbound sales
- **WhatsApp-only calling via native API**: Calling is limited to WhatsApp Business Calling API and VoIP (Telnyx); no dedicated voice channel independent of WhatsApp for markets with lower WhatsApp penetration
- **No verified business badge differentiation on calls**: No specific mention of leveraging Meta's verified business badge as a trust signal on calls, which Wati highlights explicitly
- **Starter plan has no AI or automation**: The $79/month entry-level plan includes no automation or AI, making it essentially a basic shared inbox — a significant limitation for SMBs that want affordable AI-assisted calling



## Pricing Tiers

| Plan | Price (monthly) | Key Inclusions |
| --- | --- | --- |
| **Starter** | $79/month | Up to 5 users, unlimited MACs, unified inbox, no AI, no automation, no WhatsApp calling AI |
| **Growth** | $159/month | 1,000 MACs included (+$12/100 MACs), AI Agents (chat only), workflow automation, broadcasts, call transcripts, WhatsApp calling (human agents) |
| **Advanced** | $279/month | 1,000 MACs included (+$15/100 MACs), all Growth features + Voice AI Agents (calls), custom integrations, HTTP requests, multi-workspace, advanced security |
| **Enterprise** | Custom | Unlimited users, custom MACs, SLA, dedicated support, all features |

Additional call charges: Meta's per-minute rates for outbound WhatsApp calls (passed through at cost); inbound calls are free from May 1, 2025 onward. Outbound rates vary by destination country and volume tier (volume discounts apply, reset monthly). AI usage is included at no extra cost on Growth, Advanced, and Enterprise plans. Annual billing offers a 20% discount. 7-day free trial available on Growth plan features.

**Analysis**: Respond.io's entry price of $159/month (Growth) to access meaningful AI and automation — and $279/month (Advanced) to unlock Voice AI on calls — is substantially higher than Wati's tiered SMB pricing. Wati's positioning of WhatsApp Calling across all three paid plans (Growth, Pro, Business) gives it a significant pricing advantage for cost-sensitive SMBs who want voice calling without paying enterprise-tier prices.



## Target Market

**Primary**: Mid-market to large B2C businesses managing high conversation volumes across multiple messaging channels (WhatsApp + Instagram + TikTok + Messenger + email); companies in retail, e-commerce, hospitality, education, healthcare, and financial services; particularly strong in Southeast Asia, Middle East, and LATAM.

**Secondary**: Enterprise brands (10,000+ contact volumes) requiring multi-workspace management, custom integrations, advanced security compliance, and dedicated support; franchises and multi-location businesses.

**Less focused on**: Micro-businesses and very early-stage SMBs (Starter plan is essentially a basic inbox with no AI/automation); businesses whose entire communication stack is WhatsApp-only with no need for other channels; companies seeking low-cost, WhatsApp-first simplicity rather than a full omnichannel platform.



## Strengths

- **True omnichannel platform**: The only major WhatsApp BSP that natively unifies calls, chat, and social (TikTok, Instagram, Messenger) in one inbox — a clear differentiator vs. Wati's WhatsApp-centric model
- **Early and comprehensive WhatsApp Business Calling API adoption**: One of the first BSPs to build full calling support including AI voice handling, call recording, transcription, and workflow automation on top of the calling API
- **Voice AI Agents launched January 2026**: A fast-moving product org that shipped Voice AI within months of Meta's calling API going global — using ElevenLabs Flash v2.5 for high-quality, low-latency voice
- **Enterprise credibility at scale**: Trusted by globally recognized brands; 99.999% uptime; positioned as production-ready at B2C scale
- **AI Orchestrator architecture**: Multi-agent, multi-modal AI that handles text, images, audio, and files — more architecturally sophisticated than single-model chatbot approaches
- **Transparent, no-markup pricing on WhatsApp calling**: Passes Meta's official rates directly with no hidden per-call fees, which is a trust-building differentiator
- **Strong content and SEO moat**: Extensive blog, help docs, and comparison pages (including "Wati vs Respond.io") that drive inbound organic traffic and shape competitive perception



## Weaknesses

- **High price floor for AI features**: The $159/month Growth plan is required for any AI or automation; Voice AI on calls requires the $279/month Advanced plan — pricing SMBs out of key capabilities that Wati offers at lower tiers
- **No outbound AI voice calling**: Voice AI is limited to answering inbound calls; Respond.io has not publicly documented an AI-initiated outbound call capability, which limits use cases like proactive lead follow-up, reminders, or re-engagement campaigns
- **3-minute AI call cap**: The 3-minute ceiling on AI-handled WhatsApp calls constrains complex sales conversations and reduces reliability for high-consideration purchases
- **Outbound calling gated by permission friction**: The call permission request system (1 per 24 hours, 2 per week per customer) limits high-volume outbound calling, which is a core use case for sales-driven SMBs
- **Messaging threshold requirement for calling**: Requiring a 2,000 business-initiated conversations per 24-hour rolling period to unlock WhatsApp calling excludes smaller businesses or newer accounts
- **Performance complaints at scale**: G2/Capterra reviewers note occasional platform slowness and limited bulk action functionality (bulk close, bulk assign) — relevant for high-volume operations
- **Limited analytics customization**: Some reviewers flag that analytics, while extensive, are not easily customizable or navigable — a potential gap vs. Wati's dedicated call analytics dashboard
- **Starter plan is underpowered**: At $79/month with no AI, no automation, and no calling AI, the entry plan offers minimal differentiation from a generic shared inbox tool



## Comparison to Wati

### Where Respond.io Wins:
- **Omnichannel breadth**: Supports 10+ channels including TikTok, Instagram, Messenger, email, and VoIP — Wati remains primarily WhatsApp-focused
- **Voice AI on WhatsApp calls**: Respond.io's January 2026 Voice AI Agent launch gives it a mature, shipping voice AI product for WhatsApp calls with 32 languages, ElevenLabs-powered voice, and AI action framework
- **Enterprise-grade AI Orchestrator**: Multi-agent, multi-modal architecture designed for reliability at scale; more sophisticated than most SMB-focused platforms
- **Call transcript + summary automation**: Auto-transcription of WhatsApp calls and AI-generated summaries are fully built out
- **Unified call + chat history**: Calls and messages live in the same contact thread, providing seamless context for agents
- **Brand credibility and case studies**: Public enterprise customer logos (Toyota, McDonald's, British Airways) provide strong social proof for mid-market buyers
- **Workflow automation flexibility**: Single visual workflow builder covers more complex multi-step business logic than simpler flow builders

### Where Wati Wins:
- **WhatsApp Calling available on all paid plans**: Wati makes WhatsApp Calling accessible on Growth, Pro, and Business — no $279/month Advanced plan requirement
- **Outbound AI voice with Astra**: Wati's Astra supports AI-initiated outbound voice calls — a use case Respond.io has not publicly documented
- **No-code Voice AI builder for non-technical teams**: Wati's Astra is positioned as SMB-accessible with a no-code builder explicitly designed for businesses without engineering resources; Respond.io's Voice AI, while it has templates, skews toward more technical configuration
- **SMB pricing and simplicity**: Wati's pricing model and product complexity are calibrated for SMBs; Respond.io's full feature set and higher price floor are better suited to mid-market and above
- **Inbound free + per-minute outbound model**: Wati's pricing model aligns with how SMBs think about call costs; Respond.io's model is similar but requires higher plan spend to access
- **Verified business badge on calls**: Wati explicitly leverages Meta's verified business badge as a trust signal during calls — not publicly highlighted by Respond.io
- **Call CTA in templates (documented for SMBs)**: Wati's call permission templates and CTA buttons are documented specifically for SMB use cases; Respond.io's implementation is available but documented more for mid-market workflows
- **15,000+ customers vs. 10,000+**: Wati has a larger absolute customer base, reflecting stronger SMB penetration
- **Focus on WhatsApp-first markets**: For businesses in Southeast Asia, India, Middle East, and LATAM operating primarily on WhatsApp, Wati's deep WhatsApp specialization (vs. Respond.io's broader omnichannel approach) can be a simpler, more affordable fit
- **Missed call notifications**: Explicitly documented as a Wati feature with dedicated UI; Respond.io handles this via workflow automation (more setup required)
- **Agent performance tracking on calls**: Wati's dedicated call analytics dashboard with agent-level performance tracking is a purpose-built feature; Respond.io's analytics are more general

### Strategic Positioning Against Respond.io:
Wati wins in the WhatsApp-first SMB segment by offering WhatsApp Calling and AI Voice (Astra) at lower price points with less configuration complexity — for businesses that live and breathe WhatsApp, Wati is the purpose-built specialist, while Respond.io requires a heavier investment (both financial and technical) to unlock comparable voice capabilities.

**Win scenarios:**
- When the prospect is an SMB (under 500 employees) with a WhatsApp-first customer engagement model and limited technical resources
- When budget sensitivity is a factor — Wati unlocks calling on lower-tier plans vs. Respond.io's $279/month Advanced requirement for Voice AI
- When the customer wants outbound AI voice calling (Astra) — Respond.io has no documented outbound AI voice capability
- When the customer operates primarily in markets where WhatsApp is the dominant channel (India, Southeast Asia, Middle East, LATAM) and has no need for TikTok/Instagram/email unification
- When the prospect values a dedicated WhatsApp specialist vs. an omnichannel generalist
- When the customer wants call permission templates, verified badge on calls, and missed call notifications as built-in, out-of-the-box features without needing workflow configuration
- When the customer's team is non-technical and needs a no-code voice AI setup with guided onboarding



## Recent Updates & Trends

- **January 2026 — Voice AI Agents launch**: Respond.io announced Voice AI Agents powered by ElevenLabs Flash v2.5, with 32-language support, natural conversation handling, AI actions (CRM updates, booking links, lead routing), and preconfigured templates for Sales, Support, and Receptionist personas. This is Respond.io's most significant competitive move against Wati's Astra.
- **January 2026 — Real-time call handover added shortly after Voice AI launch**: Call transfer with full transcript from AI to human agents introduced post-launch as a rapid follow-up release.
- **Q2 2025 — WhatsApp Business Calling API goes global**: Meta expanded calling availability globally, and Respond.io was among the first BSPs to fully implement and document the feature, including inbound-free pricing change effective May 1, 2025.
- **March 2024 — Respond 3.0 Phase One**: Major platform redesign reducing visual complexity, improving mobile experience, and introducing Click-to-Chat Ad workflow features.
- **April 2024 — Meta Product Catalog integration**: Launched WhatsApp commerce support via Meta product catalog, enabling product browsing and purchase flows within WhatsApp conversations.
- **January 2024 — AI Agent Builder and AI Agent Objective**: Introduced a dedicated AI agent builder UI and new objective-based agent configuration, laying the groundwork for the 2026 Voice AI launch.
- **September 2022 — $7M Series A**: Funded by Headline Asia; used to expand to Middle East, Europe, and LATAM and extend integration capabilities.

**Strategic Threat Level: HIGH**

Respond.io is the single most directly competitive platform to Wati on both WhatsApp Business Calling and Voice AI. Their January 2026 Voice AI Agents launch — covering inbound WhatsApp calls with 32-language AI, CRM actions, and human handover — mirrors Wati's Astra positioning almost point for point. The primary Wati advantages (lower pricing for SMBs, outbound AI voice, stronger WhatsApp specialization) must be actively communicated in competitive deals, as Respond.io will increasingly use its Voice AI capabilities to attack Wati's core differentiation.



## Recording, GenAI & Mobile Calling

### Call Recording

Call recording is available for all call-capable channels on Respond.io, including the WhatsApp Business Calling API and VoIP (Telnyx). Recording supports two modes configurable at the workspace level:

- **Automatic mode**: Recording starts immediately when the call connects; a recording indicator appears on-screen for the agent.
- **Manual mode**: Agents see Record / Pause / Resume buttons and can start or stop recording at any point during the call.

Recordings are stored within Respond.io's platform and are accessible from two locations: the **Reports: Calls** dashboard and the **Contact Drawer → Calls tab** on each contact's profile. Call reports (duration, outcome, participants) are stored indefinitely as long as the account is active. For Telnyx VoIP calls specifically, transcripts are accessible for up to 1 year; WhatsApp channel recordings follow Meta's provider storage policies. Call data, including recordings and transcripts, can also be pushed to external systems via webhook (webhook access requires the Advanced plan). Call recording is available on Growth plan and above; the plan requirement for recording itself versus transcription is not explicitly separated in public documentation, but transcripts are confirmed to require Growth plan or higher.

### AI Transcription & Summarization

Respond.io provides both automatic transcription and AI-generated summaries for recorded calls:

- **Transcription**: A transcript is automatically generated after each recorded call ends. Each line of the transcript includes a timestamp, speaker name, and transcribed text. Agents can tap or click a timestamp to jump to that point in the recording. Transcripts are available on Growth plan and above.
- **AI call summaries**: An AI-generated summary is produced automatically from the transcript after each call. The summary surfaces key points, action items, and next steps. Summaries can be viewed, copied, downloaded, and shared directly from the call detail view and from the mobile app.
- **AI model powering transcription/summarization**: Not publicly disclosed by Respond.io. The Voice AI Agent (for inbound AI-handled calls) uses ElevenLabs Flash v2.5 for text-to-speech, but the underlying model for post-call transcription and summarization of human agent calls is not named in public documentation.
- **CRM sync**: Transcripts, recordings, and AI summaries can sync to external CRMs via webhook, keeping call context alongside chat history in systems like HubSpot or Salesforce.

### Other GenAI on Voice

Beyond transcription and summarization, the following GenAI features are documented for voice calls on Respond.io:

- **AI Voice Agents (inbound call handling)**: Voice AI Agents can autonomously answer inbound WhatsApp calls, conduct real-time spoken conversations using RAG-grounded LLM responses, collect caller information, qualify leads, and trigger AI Agent Actions (update CRM fields, change contact lifecycle stage, send HTTP requests to external systems, route to human agents). Powered by ElevenLabs Flash v2.5 with 32-language support and automatic language detection mid-call. Available on Advanced plan and above only.
- **Call-to-human handover with full context**: When an AI-handled call transfers to a human agent, the full call transcript and chat history are passed to the receiving agent automatically.
- **AI Assist on mobile**: Agents can use AI Assist to draft text replies within the conversation thread on mobile, though this is a chat feature rather than a voice-specific one.

The following GenAI-on-voice capabilities are **not publicly documented** by Respond.io:

- Real-time sentiment analysis on human agent calls
- Agent coaching or live in-call suggestions to human agents
- Call highlight detection or "moment" tagging within recordings
- Automatic CRM field population from call transcript content (CRM sync is available via webhook but requires custom configuration; it is not an out-of-the-box auto-fill of structured CRM fields from call content)

### Mobile App Calling

Respond.io's native iOS and Android mobile apps support both inbound and outbound WhatsApp Business calls and VoIP calls. This is a fully shipped, documented feature — not web-only. Specific capabilities confirmed for mobile:

- **Make and receive WhatsApp calls**: Agents can initiate outbound calls to contacts and receive inbound calls directly in the mobile app.
- **Calls tab**: A dedicated Calls tab (phone icon) in the mobile app shows recent call activity including incoming, missed, ongoing, and completed calls — mirroring the web experience.
- **In-call controls**: Mute, speaker toggle, and call minimization (to continue using the app while on a call) are all supported on mobile.
- **Call transfer on mobile**: Agents can transfer a live call to another agent from the mobile app, with the ability to add a context note before transferring.
- **AI summary on mobile**: AI-generated call summaries are viewable, copyable, and shareable directly from the mobile app after each recorded call.
- **Push and in-app notifications**: Inbound call notifications are delivered via push notification (grouped by contact on iOS; grouped by workspace then contact on Android).
- **Source**: Respond.io's own help documentation at respond.io/help/mobile-app/calling-from-your-mobile confirms WhatsApp calling on mobile is available globally.

### Wati Comparison Note

Respond.io has a more complete call recording and GenAI stack for human agent calls — automatic or manual recording, auto-transcription, and AI summaries are all fully shipped and accessible on the Growth plan ($159/month), whereas Wati's equivalent post-call GenAI features (transcription, summarization) are not publicly documented as available for human agent WhatsApp calls as of March 2026. On mobile calling, both platforms support WhatsApp Business calls on iOS and Android native apps. Respond.io's Voice AI for inbound calls (Advanced plan, $279/month) is more mature than anything Wati has shipped in the equivalent inbound AI-answer category, though Wati's Astra covers outbound AI voice calling — a use case Respond.io has not publicly documented.
