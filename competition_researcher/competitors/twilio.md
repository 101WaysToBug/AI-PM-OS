# Competitor Brief: Twilio

Last Updated: March 2026
Analyst: Wati Product Team



## Overview

Twilio is a publicly traded cloud communications platform-as-a-service (CPaaS) company founded in 2008, headquartered in San Francisco. The company raised $240M across 13 funding rounds before going public (NYSE: TWLO) and has grown into one of the most prominent developer-first communications infrastructure companies in the world. As of late 2025, Twilio reported annual revenue of $5.07B (up 13.66% YoY) and serves over 349,000 active customer accounts across 180 countries. Its investor base has included Amazon, and it is recognized as a leader in the 2024–2025 IDC MarketScape for Worldwide Customer Data Platforms.

Twilio's core identity is as a developer infrastructure company: its platform exposes programmable APIs for voice, SMS, messaging, email, and video that developers use to embed communications into applications. In 2019, Twilio acquired Segment (a Customer Data Platform) for $3.2B, adding first-party customer data infrastructure to its communications stack. Its flagship products today span Programmable Messaging and Voice APIs, Twilio Flex (an enterprise contact center), Twilio Segment (CDP), Twilio Engage (marketing automation), and a growing AI product suite including ConversationRelay, Conversational Intelligence, Agent Copilot, and AI Assistants.

In the context of WhatsApp and messaging, Twilio is a Meta-authorized WhatsApp Business Solution Provider (BSP) and routes a significant volume of WhatsApp traffic globally. Twilio reported 35% year-over-year growth in WhatsApp usage during Cyber Week 2024. In July 2025, Twilio reached general availability (GA) of WhatsApp Business Calling, making it a direct competitor to Wati in the voice-over-WhatsApp space. However, Twilio's approach remains fundamentally developer-centric: its WhatsApp Calling requires API integration and TwiML configuration, as opposed to Wati's no-code, SMB-first inbox experience.



## Key Features

### WhatsApp Calling

- **WhatsApp Business Calling via Meta's official API**: Reached GA on July 15, 2025, built on Twilio Programmable Voice. Officially Meta-compliant and uses the Cloud API.
- **Inbound (user-initiated) calls**: Supported globally across all Meta Cloud API countries. Customers tap a call button within the WhatsApp chat to reach the business.
- **Outbound (business-initiated) calls**: Supported in most Meta Cloud API countries, with explicit exclusions for business numbers registered in the US, Canada, Nigeria, Egypt, Vietnam, and Turkey.
- **Call-to-action templates**: Businesses use interactive call templates (VOICE_CALL_REQUEST) to request customer consent before placing outbound calls. Call permission is valid for 5 calls per 24-hour window, up to 7 days before re-consent is required.
- **Business hours control**: Can be configured in the WhatsApp Business Account Manager (Meta console) to control when the call button is visible and when customers can initiate calls.
- **Verified business badge**: Blue checkmark displayed on call screens, business profile, context cards, and incoming call screen — consistent with Meta's WhatsApp Business verification.
- **IVR and DTMF support**: Full Twilio Programmable Voice feature set is available on WhatsApp calls, including IVR flows, DTMF keypad input, call recording, and speech recognition.
- **Integration with Flex**: WhatsApp calls can be routed to Twilio Flex agents, enabling human agent handling of inbound voice contacts from WhatsApp.
- **AI integration on calls**: WhatsApp calls can be connected to ConversationRelay (AI voice agents), Conversational Intelligence (transcription and analytics), and Voice Intelligence operators.
- **Call Insights Dashboard**: Twilio's existing Call Insights Dashboard (aggregated metrics, call quality trends, call log filtering) extends to WhatsApp calls.
- **Missed call behavior**: After two consecutive missed calls, users are re-prompted to grant permission; after four consecutive missed calls, call permission is automatically revoked by Meta.
- **Implementation requirement**: WhatsApp Business Calling requires configuring a TwiML Voice Application SID and a messaging limit of at least 2,000 business-initiated conversations in a rolling 24-hour period (requires Meta Business Verification). This is a developer/API-first configuration — no out-of-the-box no-code setup within Twilio's own console.

### Voice AI / Conversational AI

- **ConversationRelay**: Twilio's core voice AI product. Enables developers to build natural language AI voice agents using any LLM (bring your own model). Integrates real-time streaming, speech-to-text (STT), text-to-speech (TTS), interruption handling, and expressive voices. Priced at $0.07/minute.
- **STT/TTS provider flexibility**: ConversationRelay supports third-party STT/TTS providers including ElevenLabs, Deepgram, Google, and Amazon — allowing businesses to choose voice quality and language coverage.
- **LLM flexibility**: Supports integration with OpenAI (including Realtime API for Speech-to-Speech), Mistral, and other LLMs via standard API patterns.
- **OpenAI Realtime API integration (August 2025)**: Twilio launched native integration with OpenAI's Realtime API, enabling direct Speech-to-Speech (S2S) with GPT-4o Realtime models — reducing latency in voice AI interactions.
- **Conversational Intelligence**: AI analysis layer that transcribes voice calls and text conversations into structured data and insights. Analyzes sentiment, task completion, interruptions, human escalation events, and virtual agent performance. Priced at $0.0035/minute for Language Operators. Renamed from "Voice Intelligence" as of 2025.
- **AI Assistants (Alpha/Beta)**: A higher-level framework for building autonomous conversational assistants with customer memory (via Segment), tool/API integrations, multi-channel deployment, and safety guardrails (prompt injection detection, content moderation). Described as "customer-aware." Still in alpha/expanded beta as of late 2025; native voice integration listed as an upcoming enhancement.
- **Agent Copilot (Flex, Public Beta)**: AI assistant for human contact center agents within Twilio Flex. Provides real-time response suggestions, customer profile summaries (via Unified Profiles/Segment), auto-generated wrap-up notes, sentiment analysis, topic/subtopic identification, and transfer summaries. Priced at $0.045/voice minute and $0.01/digital message when used in Flex.
- **Microsoft Azure AI Foundry partnership (May 2025)**: Multi-year strategic partnership announced at SIGNAL 2025. Focus areas include multi-channel AI agents for customer engagement automation, enhanced Agent Copilot capabilities, and multi-modal interaction tools.
- **Implementation profile**: Primarily developer-built. No standalone no-code voice AI agent builder comparable to Wati's Astra. Requires coding knowledge to configure ConversationRelay; low-code workarounds exist (e.g., Airtable for conversation flow management) but are not first-party no-code tools.
- **Language support**: Dependent on chosen STT/TTS providers. Deepgram, ElevenLabs, and Google cover broad language ranges, but Twilio does not publish a fixed "30+ languages supported" claim for its own product layer.

### Core Platform Capabilities

- **Programmable Messaging API**: Send and receive SMS, MMS, WhatsApp, and RCS messages globally. Pay-as-you-go, $0.005/message for WhatsApp.
- **Twilio Flex**: Fully programmable cloud contact center. Supports voice, WhatsApp, SMS, email, and chat. Priced at $1/active user hour or $150/named user/month. Used primarily by mid-market and enterprise teams.
- **Twilio Segment (CDP)**: Customer Data Platform with 700+ integrations, real-time event streaming, identity resolution, audience building, predictive traits, journey orchestration (Twilio Engage), and data residency controls. Named a Leader in 2024-2025 IDC MarketScape for CDPs.
- **Twilio Studio**: Low-code/no-code visual flow builder for building messaging and voice workflows in a drag-and-drop interface.
- **Twilio Verify / Lookup / SendGrid**: Additional products for authentication (OTP), phone validation, and transactional email.

### Notable Strengths

- Dominant CPaaS infrastructure brand with deep developer trust and ecosystem of 10M+ developers.
- Full-stack AI portfolio: ConversationRelay + Conversational Intelligence + Agent Copilot + AI Assistants covers voice AI, analytics, and human-assist use cases across channels.
- Official Meta WhatsApp BSP with enterprise-scale WhatsApp Calling now GA, with access to the full Programmable Voice feature set on WhatsApp calls.
- Segment CDP integration provides uniquely rich customer data context for personalization that no WhatsApp-first SMB tool can match.
- Microsoft Azure AI Foundry partnership positions Twilio for enterprise AI adoption at scale.

### Missing / Weak Areas (vs. Wati)

- No native no-code shared inbox for WhatsApp — Twilio is communication infrastructure, not a business inbox. Teams need third-party tools (Front, Hiver, Freshdesk) to get a shared WhatsApp inbox, adding cost and complexity.
- WhatsApp Calling requires developer configuration (TwiML, API integration, Meta Business Verification at 2,000+ conversation tier) — not accessible to non-technical SMB users.
- No out-of-the-box AI voice agent comparable to Wati's Astra: ConversationRelay requires LLM selection, STT/TTS provider configuration, and code-based setup. No published claim of 30+ language support at the product layer.
- No published per-minute pricing for WhatsApp Business Calling specifically (standard Programmable Voice rates apply: $0.0085/min inbound, $0.014/min outbound in the US, but WhatsApp-specific calling rates not clearly broken out).
- Business-initiated WhatsApp outbound calling explicitly not supported for businesses with numbers in the US, Canada, Nigeria, Egypt, Vietnam, and Turkey — a significant gap for customers in these markets.



## Pricing Tiers

Twilio does not sell fixed monthly plans in the traditional SaaS sense. Its pricing is usage-based (pay-as-you-go) with no required subscription, with volume discounts that apply as usage grows.

| Product | Pricing |
|---|---|
| WhatsApp messaging (inbound/outbound) | $0.005 per message (Twilio fee) + Meta per-template fee (varies by type: marketing, utility, authentication) |
| Programmable Voice (inbound) | $0.0085/min (US) |
| Programmable Voice (outbound) | $0.014/min (US) |
| WhatsApp Business Calling | Standard Programmable Voice rates apply; no separate WhatsApp-specific per-minute rate publicly documented |
| ConversationRelay (Voice AI) | $0.07/minute |
| Conversational Intelligence Language Operators | $0.0035/minute |
| Twilio Flex (contact center) | $1.00/active user hour OR $150/named user/month |
| Agent Copilot (Flex add-on) | $0.045/voice minute + $0.01/digital message |
| Flex Mobile Access | $49/user/month add-on |
| Twilio Studio (flow builder) | $0.0025/flow execution (first 1,000/month free) |
| Twilio Segment (CDP) | Separate pricing; free tier available; paid plans scale with Monthly Tracked Users |
| Support | Developer plan: free; higher plans scale with spend |

**WhatsApp Calling and Voice AI access**: Not gated to a higher tier — but both require developer setup and incur usage-based charges. There is no SMB-friendly flat-rate plan that bundles these features.

Analysis: Twilio's usage-based pricing makes it attractive for developers and high-volume enterprises but unpredictable and complex for SMBs. A typical SMB using WhatsApp Calling + ConversationRelay would pay stacked per-minute rates (Programmable Voice + ConversationRelay + Conversational Intelligence), plus meta template fees, plus any Flex or inbox tooling costs. Wati's flat per-minute outbound and free inbound WhatsApp Calling model is significantly simpler and more cost-predictable for SMBs.



## Target Market

Primary: Enterprise and mid-market companies with in-house engineering teams that want to build custom communications infrastructure on top of programmable APIs. Also strong with technology companies, SaaS platforms, and contact center operators using Twilio Flex.

Secondary: Mid-market and growth-stage businesses using Twilio Segment for CDP/marketing automation, and companies building AI-powered customer engagement products on top of Twilio's voice and messaging infrastructure.

Less focused on: Non-technical SMBs that need a ready-to-use WhatsApp inbox, SMB teams without developers, and businesses looking for a plug-and-play WhatsApp Business Calling + AI voice agent solution without engineering investment.



## Strengths

- **Brand and ecosystem**: Largest CPaaS provider globally; trusted by hundreds of thousands of businesses; 10M+ developer community provides compounding distribution advantage.
- **WhatsApp Business Calling (now GA)**: One of the first major BSPs to offer officially supported WhatsApp Business Calling via Meta's API at enterprise scale, giving Twilio a credible claim in the voice-over-WhatsApp space.
- **Full-stack AI voice infrastructure**: ConversationRelay + OpenAI Realtime API + Conversational Intelligence + Agent Copilot represents a mature, modular AI voice toolkit that no SMB WhatsApp platform has matched at the infrastructure level.
- **Segment CDP**: The ability to combine WhatsApp/voice interactions with rich customer data profiles (purchase history, behavioral signals, predictive traits) is a strong differentiation in the enterprise space.
- **Global scale and compliance**: Operations in 180 countries, HIPAA-eligible products (ConversationRelay), data residency controls, TCPA compliance toolkit, and Meta Business Verification support.
- **Microsoft Azure AI Foundry partnership**: Access to Microsoft's enterprise customer base and Azure AI capabilities positions Twilio for significant AI-driven growth through 2026 and beyond.
- **Revenue growth and financial strength**: $5.07B annual revenue (FY2025), 107% dollar-based net expansion rate (Q1 2025), publicly traded — well-capitalized to invest in product development.



## Weaknesses

- **Requires developers to operate**: WhatsApp Calling, ConversationRelay, and most advanced features require engineering resources to configure, maintain, and scale. Non-technical SMB teams cannot self-serve these capabilities.
- **No native shared inbox for WhatsApp**: Twilio does not offer its own team inbox product for WhatsApp; businesses must integrate third-party tools, adding cost, friction, and vendor complexity.
- **Unpredictable, complex pricing**: Stacked usage fees (Programmable Voice + ConversationRelay + Conversational Intelligence + Studio + Segment) make total cost of ownership opaque. SMBs frequently report bill shock and pricing complexity in reviews.
- **No-code Voice AI gap**: ConversationRelay has no visual no-code builder for non-developers. Wati's Astra offers a no-code AI voice agent builder; Twilio's equivalent requires code, LLM configuration, and STT/TTS provider selection.
- **WhatsApp outbound calling restricted in key markets**: Business-initiated WhatsApp calls not supported for numbers registered in the US, Canada, Nigeria, Egypt, Vietnam, and Turkey — blocking a major use case in some of the world's largest WhatsApp markets.
- **Customer support quality at SMB level**: G2 reviews consistently note that support responsiveness depends on spend level. SMB accounts may wait multiple business days for ticket resolution. Wati scores 8.7 vs. Twilio's 8.0 on G2 Quality of Support.
- **Not an SMB product**: Twilio's interface, documentation, and sales motion are optimized for developers and enterprise buyers. SMBs comparing Twilio to Wati routinely cite the steep learning curve and the need for professional implementation (often $10,000s for bespoke setups).
- **AI Assistants still in alpha/beta**: Twilio's AI Assistants product (the highest-level no-code/low-code AI agent experience) is still in alpha/expanded beta as of late 2025, with native voice integration listed as "upcoming." This leaves a gap in accessible AI voice automation for non-enterprise customers.



## Comparison to Wati

### Where Twilio Wins:
- Enterprise scale: serves Fortune 500 companies and high-volume platforms that Wati cannot support
- Infrastructure depth: full Programmable Voice feature set (IVR, recording, transcription, DTMF) available on WhatsApp calls
- AI voice infrastructure maturity: ConversationRelay with OpenAI Realtime, ElevenLabs TTS, Deepgram STT — more sophisticated underlying AI stack
- Customer data platform: Segment CDP integration provides deeply personalized AI interactions using purchase history, behavioral data, and predictive signals — far beyond Wati's scope
- Multi-channel reach: SMS, RCS, voice, email, WhatsApp, and chat all on one platform — relevant for enterprise omnichannel programs
- Microsoft partnership: Azure AI Foundry integration opens doors to enterprise AI budgets
- Financial scale to invest: $5B+ revenue company vs. Wati's growth-stage SMB positioning

### Where Wati Wins:
- **Ease of use**: Wati is a ready-to-use WhatsApp inbox — no developers required. WhatsApp Calling works out of the box with a one-click call from chat UI.
- **No-code AI Voice (Astra)**: Wati's Astra is a deployable no-code AI voice agent with near-human voice, 30+ languages, live language switching, and built-in CRM actions. Twilio has no comparable no-code product GA.
- **SMB-friendly pricing**: Flat monthly plans (Growth, Pro, Business) with inbound calling free and predictable per-minute outbound rates — vs. Twilio's complex stacked usage fees.
- **WhatsApp-native inbox**: Shared team inbox, agent assignment, broadcast campaigns, chatbot builder, and call analytics all in one WhatsApp-focused product — no integration required.
- **Customer support**: Wati scores higher (8.7 vs. 8.0 on G2 Quality of Support) and is more responsive for SMB accounts.
- **Speed to value**: Wati customers can activate WhatsApp Calling and deploy an AI voice agent without writing a line of code. Twilio requires developer setup, Meta Business Verification at 2,000+ conversation tier, and ongoing engineering maintenance.
- **WhatsApp-first focus**: Wati's product decisions are 100% centered on WhatsApp Business use cases for SMBs, resulting in tailored features (missed call notifications, call permission templates, agent performance tracking, call CTA buttons in templates) that Twilio builds as API primitives, not finished features.
- **Outbound calling in key markets**: Wati supports outbound WhatsApp calling for businesses regardless of their registered country; Twilio explicitly excludes US, Canada, and other major markets for business-initiated outbound WhatsApp calls.

### Strategic Positioning Against Twilio:
Wati is the WhatsApp-first business platform built for teams that want to sell, support, and automate on WhatsApp without writing code — while Twilio is communications infrastructure that requires engineers to build and maintain. For SMBs choosing between a tool they can use tomorrow and a platform they need developers to configure, Wati wins on time-to-value, total cost, and WhatsApp depth.

Win scenarios:
- Prospect has no in-house developers and needs WhatsApp Calling live within days, not weeks
- Prospect wants a no-code AI voice agent on WhatsApp without selecting an LLM, configuring STT/TTS providers, or writing TwiML
- Prospect is a US or Canadian business that wants business-initiated outbound WhatsApp calls (Twilio does not support this for numbers registered in these countries)
- Prospect is managing a customer support or sales team and needs a shared inbox, agent assignment, and call analytics in one product — not stitched together from Twilio + third-party inbox tools
- Prospect has had sticker shock from Twilio's stacked usage pricing and wants predictable monthly costs
- Prospect needs 30+ language AI voice support quickly and cannot afford the integration work to configure Deepgram + ElevenLabs + LLM on ConversationRelay
- Prospect is an SMB (under 500 employees) for whom Twilio's implementation cost ($10K+ for bespoke setups) and ongoing engineering overhead is not viable



## Recent Updates & Trends

- **Q3 2025 (July 15, 2025)**: WhatsApp Business Calling reached General Availability on Twilio Programmable Voice, alongside GA of Event-Triggered Journeys in Twilio Engage and Data Residency for Email (EU). This is the most significant move making Twilio a direct Wati competitor in voice-over-WhatsApp.
- **Q2 2025 (May 14–15, 2025)**: SIGNAL 2025 conference in San Francisco. Major announcements included next-generation AI-powered Customer Engagement Platform, multi-year Microsoft Azure AI Foundry strategic partnership, ConversationRelay GA for voice AI, Conversational Intelligence (formerly Voice Intelligence) launch covering voice + messaging (messaging in private beta), Agent Copilot enhancements, Real-Time Personalization in Segment CDP.
- **Q2 2025 (May 2025)**: Twilio-Microsoft partnership announced to build multi-channel AI agents on Azure AI Foundry; focus includes Agent Copilot enhancements and multi-modal customer interaction tools targeting enterprise contact centers.
- **Q3 2025 (August 2025)**: Twilio launched native integration with OpenAI's Realtime API (Speech-to-Speech) for ConversationRelay, enabling lower-latency voice AI interactions.
- **Q4 2025 (FY2025)**: Twilio reported $5.07B annual revenue (+13.66% YoY), 349,000+ active customer accounts, and 107% dollar-based net expansion rate. Strong financial position to continue AI product investment.
- **Ongoing (2025)**: AI Assistants (autonomous multi-channel chatbot/agent framework) in expanded beta, with native voice integration listed as a coming enhancement — indicating Twilio is actively closing the no-code AI voice agent gap.
- **Ongoing (2025)**: WhatsApp usage on Twilio grew 35% YoY during Cyber Week 2024, signaling accelerating enterprise adoption of WhatsApp as a business channel through Twilio's infrastructure.

Strategic Threat Level: **MEDIUM**

Twilio is a credible and well-resourced threat in the WhatsApp Calling space following the July 2025 GA launch, and its AI voice infrastructure (ConversationRelay + Microsoft partnership) could become a genuine competitor to Wati's Astra if it launches a no-code voice AI builder. However, Twilio's developer-first model, complex pricing, and lack of a native SMB inbox mean it is not directly competing for Wati's core customer (non-technical SMB teams) today. The threat escalates if Twilio launches a no-code packaged product (through a partner channel or directly) targeting SMBs, or if a Twilio-powered ISV builds and markets a Wati-like product on top of Twilio's infrastructure.



## Recording, GenAI & Mobile Calling

### Call Recording

Call recording is available on Twilio WhatsApp Business Calling as part of the standard Programmable Voice feature set. Twilio's own documentation confirms that WhatsApp Business Calling exposes "the full array of Twilio Programmable Voice features, like Interactive Voice Response (IVR), Voice Intelligence, voice recording and speech recognition."

- **Automatic vs. manual**: Recording is not automatic. It must be explicitly configured by a developer using either the `<Record>` TwiML verb (to record the entire call) or the `<Start><Recording>` TwiML instruction (to start recording mid-call at a specific point in the flow). There is no one-click "enable recording" toggle in a console or UI for WhatsApp calls.
- **Trigger methods**: Recording can be initiated at the start of a call, mid-call at a developer-defined point, or programmatically via the REST API. Dual-channel recording (separate audio tracks for caller and agent) is now the default format, which improves transcription accuracy.
- **Storage**: Recordings are stored in Twilio's cloud by default. First 10,000 minutes of storage per month are free; above that, $0.0005 per minute per month for mono; dual-channel storage is billed at the same rate as mono as of the most recent pricing update. Alternatively, developers can configure external storage directly to an AWS S3 bucket at no additional Twilio charge (AWS storage fees apply separately).
- **Pricing**: No per-minute recording fee beyond storage. The underlying Programmable Voice per-minute rate ($0.0085/min inbound, $0.014/min outbound in the US) covers the call itself; storage is charged separately as above.
- **Limitation**: Entirely developer-configured. Non-technical users cannot enable or manage WhatsApp call recording without engineering involvement. No compliance consent flows (e.g., "this call may be recorded" prompts) are provided out of the box — developers must implement these themselves.

Sources: [Programmable Call Recording](https://www.twilio.com/en-us/call-recording), [How much does it cost to record a call?](https://help.twilio.com/articles/223132527), [WhatsApp Business Calling docs](https://www.twilio.com/docs/voice/whatsapp-business-calling), [External S3 storage changelog](https://www.twilio.com/en-us/changelog/external-storage-for-call-recording-is-now-available)

---

### AI Transcription & Summarization

Twilio's **Conversational Intelligence** product (renamed from Voice Intelligence in 2025) provides both transcription and AI-powered analysis of voice calls and messaging conversations.

- **Transcription**: Available in both post-call and real-time modes. Post-call transcription converts a completed call recording into a full text transcript. Real-time transcription processes live audio utterances during an active call. Priced at **$0.035 per minute** for transcription.
- **Call summarization**: Available as a pre-built Language Operator. Conversational Intelligence summarizes the key points of a call — what was discussed, action items, decisions made — using a generative AI LLM. This is a structured output, not a free-text field.
- **Language Operators pricing**: Each Language Operator (including summarization, sentiment, entity extraction, etc.) is priced at **$0.005 per minute** in addition to the base transcription rate. Multiple operators can be stacked on a single transcript.
- **WhatsApp support**: Conversational Intelligence explicitly supports WhatsApp as a messaging channel for text-based analysis. For WhatsApp voice calls, the product applies via the standard Programmable Voice integration, consistent with Twilio's documentation that WhatsApp Business Calling exposes the full Voice Intelligence feature set.
- **Supported languages**: English, Spanish, French, German, Italian, Portuguese, Dutch, Norwegian, Polish, Swedish, Danish. Custom Language Operators can extend to other languages using external AI models.
- **Agent Copilot (Flex add-on, Public Beta)**: For teams using Twilio Flex, Agent Copilot adds auto-generated wrap-up notes after each call (summarizing conversation, sentiment, disposition codes, and topic), real-time suggested responses during live calls, and an "Ask Copilot" interface for agents to query call context. Priced at **$0.045 per voice minute** as a Flex add-on.
- **Implementation requirement**: All of the above require developer configuration to connect Conversational Intelligence to a call recording or live call stream. There is no one-click "enable AI transcription" toggle for WhatsApp calls in a console.

Sources: [Conversational Intelligence product page](https://www.twilio.com/en-us/products/conversational-ai/conversational-intelligence), [Conversational Intelligence docs](https://www.twilio.com/docs/conversational-intelligence), [Language Operators docs](https://www.twilio.com/docs/conversational-intelligence/language-operators), [Introducing Conversational Intelligence blog](https://www.twilio.com/en-us/blog/introducing-conversational-intelligence)

---

### Other GenAI on Voice

Beyond transcription and summarization, Twilio's Conversational Intelligence and Agent Copilot stack includes the following GenAI capabilities applied to voice calls:

- **Sentiment analysis**: A pre-built Language Operator that uses a generative AI LLM to determine customer sentiment across the overall conversation (positive, negative, mixed). Available on both voice and messaging.
- **Topic and subtopic identification**: Pre-built operators identify what the call was about and categorize it — useful for call routing analytics, QA, and compliance.
- **Interruption detection**: Identifies points where one party spoke over another, useful for agent coaching and quality management.
- **Virtual agent performance monitoring**: Tracks task completion rates, escalation to human agents, and conversation flow adherence for AI-handled calls (ConversationRelay sessions).
- **Human escalation detection**: Identifies when a virtual agent hands off to a human — enabling funnel analytics.
- **Custom LLM-powered operators**: Developers can define custom Generative Operators using their own LLM logic for bespoke analysis tasks (e.g., compliance checklist completion, upsell detection, competitor mention tracking).
- **Real-time coaching (Agent Copilot, Flex only)**: During live calls in Flex, Agent Copilot surfaces next-best-action suggestions, knowledge base answers, and customer profile context to agents in real time. This is a live coaching layer, not a post-call report.
- **CRM auto-fill from call content**: Agent Copilot's wrap-up notes automatically populate structured fields after a call (sentiment, topic, disposition codes). These can be pushed to CRM systems via Twilio Flex integrations (e.g., Salesforce). However, this requires Flex and additional CRM integration work — it is not a turnkey CRM auto-fill feature.

Note: All of these features are delivered via API and require developer integration or Flex configuration. There is no standalone no-code dashboard where a non-technical SMB manager can view call sentiment or coaching reports without engineering setup.

Sources: [Conversational Intelligence product page](https://www.twilio.com/en-us/products/conversational-ai/conversational-intelligence), [Pre-built Language Operators](https://www.twilio.com/docs/conversational-intelligence/pre-built-operators), [Agent Copilot docs](https://www.twilio.com/docs/flex/admin-guide/setup/copilot)

---

### Mobile App Calling

**Twilio's native iOS/Android mobile app for agents (Flex Mobile) reached End of Sale (EOS) on September 30, 2025 and is no longer available to new users.**

- **What existed**: Twilio Flex Mobile was a pre-built iOS and Android app (available on the App Store and Google Play) that brought the Flex contact center experience to mobile devices. It supported accepting incoming calls, placing outbound calls, muting, holding, transferring, and handling messaging conversations (including WhatsApp messages with inline audio playback).
- **WhatsApp voice calls in Flex Mobile**: The app supported WhatsApp messaging and inline audio file playback. Whether agents could answer live WhatsApp Business voice calls (VoIP calls routed through Twilio Flex) from Flex Mobile was not explicitly confirmed in public documentation before EOS. The app's WhatsApp support appears to have been messaging-focused, not voice-call-focused.
- **EOS rationale**: Twilio stated that "a single mobile app can't capture the unique requirements of every organization" and chose to empower customers to build their own mobile solutions or use partner solutions rather than maintaining a single first-party app.
- **Current state (as of October 2025 and beyond)**: No native Twilio mobile app is available to new Flex customers. Existing Flex Mobile users (pre-September 30, 2025) may continue using the app, but it will not receive feature updates. Twilio directs new customers to third-party partner solutions (e.g., Fastcall for Salesforce-centric teams) or recommends building a custom mobile app using Twilio's Voice Mobile SDKs (iOS SDK and Android SDK).
- **WhatsApp Business Calling on mobile today**: For new Twilio customers, WhatsApp Business Calling is effectively API/web-only. Agents can handle WhatsApp calls via Twilio Flex in a web browser, or businesses can build their own mobile app using the Voice iOS/Android SDKs — but this requires engineering investment. There is no Twilio-provided native mobile agent app for WhatsApp calling.

Sources: [Flex Mobile EOS changelog](https://www.twilio.com/en-us/changelog/flex-mobile-eos), [Flex Mobile docs](https://www.twilio.com/docs/flex/flex-mobile), [Flex Mobile public beta announcement](https://www.twilio.com/en-us/changelog/flex-mobile-now-available-in-public-beta), [Voice Mobile SDKs](https://www.twilio.com/docs/voice/sdks)

---

### Wati Comparison Note

Twilio offers materially more sophisticated recording and GenAI infrastructure than Wati — call recording, real-time and post-call transcription, AI summarization, sentiment analysis, and live agent coaching are all available — but every feature requires developer configuration, making them inaccessible to the non-technical SMB teams that are Wati's core market. On mobile calling, Twilio is actually in a weaker position than Wati as of late 2025: Twilio's native agent mobile app (Flex Mobile) was discontinued as of September 30, 2025, leaving WhatsApp Business Calling as API/web-only for new customers, while Wati's mobile app (if available) would represent a meaningful ease-of-access advantage for agents working on the go.
