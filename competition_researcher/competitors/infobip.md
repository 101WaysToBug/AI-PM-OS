# Competitor Brief: Infobip

Last Updated: March 2025
Analyst: Wati Product Team



## Overview

Infobip is a Croatian-founded global cloud communications platform established in 2006. It reached unicorn status in 2020 and has grown into one of the largest CPaaS (Communications Platform as a Service) providers in the world, with over $2.3B in revenue in 2024, 3,400+ employees, 70+ offices across six continents, and operations spanning 195+ countries. The company raised $1.4B in total funding with a $520M line of credit secured in July 2025. Infobip is consistently named a Leader in the Gartner Magic Quadrant for CPaaS and handles 453+ billion interactions annually across its platform.

Infobip's core platform covers SMS, RCS, WhatsApp, Viber, email, voice, and 15+ other channels under a single API and product stack. Their positioning is squarely enterprise-grade omnichannel communications: they serve large telecoms, financial institutions, retailers, and global brands needing programmable, multi-channel communications at scale. Recent strategic moves include the launch of their Conversational Experience Orchestration Platform (CXOP) in June 2025, followed by the announcement of AgentOS — an AI-native orchestration layer — unveiled in February 2026 to celebrate their 20th anniversary.

As a Wati competitor, Infobip is relevant because they are a WhatsApp Business Solution Provider (BSP) with direct Meta API access, have launched native WhatsApp Business Calling (July 2025), and are building out AI voice assistant and agentic AI capabilities. While Infobip primarily targets enterprises and mid-market companies, their recent product investments in no-code tooling, voice AI, and WhatsApp calling put them on a trajectory that could increasingly overlap with Wati's SMB customer base — especially as they try to expand accessible tiers downmarket.



## Key Features

### WhatsApp Calling

Infobip launched native WhatsApp Business Calling via Meta's API in July 2025, making them one of the first BSPs to offer this capability:

- **Inbound and outbound calling** via WhatsApp Business numbers, using WhatsApp's native interface — customers never leave the app
- **Branded caller ID**: Verified business name, logo, and verified badge displayed on incoming calls
- **Business-initiated calling workflow**: Requires user permission before a business can place a call; permission can be granted via free-form interactive message (within 24-hour window) or call permission template (outside 24-hour window)
- **Call CTA button in templates**: One call button per WhatsApp template, supporting international-format phone numbers
- **Permission request limits**: Up to one call permission request per 24 hours; up to two within a 7-day period; up to five connected calls within a 24-hour window
- **End-to-end encryption** on all calls (WhatsApp-native security)
- **Call recording**: Supported via Infobip's Conversations integration (not natively via Meta's API — Infobip adds this layer). Configurable for inbound, outbound, or both. Each participant's audio can be recorded as separate or unified files
- **Agent handling via Conversations**: Agents receive inbound call pop-ups with accept/decline, and can handle WhatsApp calls alongside Viber voice calls in a single conversation thread
- **Call routing**: Calls can be routed through Infobip's contact center routing logic (skills-based, queue-based)
- **Analytics**: Call performance tracked within Infobip's broader analytics suite — average handling time, first response time, CSAT, agent performance
- **API integration**: Full programmatic access via the WhatsApp Business Calling API for custom deployments
- **No new phone numbers or infrastructure required**: Uses existing WhatsApp sender

Note: WhatsApp Calling is available via both the API (for developer-led implementations) and within the Conversations contact center product. It is an enterprise-grade implementation — dedicated onboarding and custom pricing apply. There are no publicly listed self-serve tiered plans that include WhatsApp Calling for SMBs.

### Voice AI / Conversational AI

Infobip has multiple overlapping voice AI products:

- **AI Voice Assistant** (native product): Pre-built AI-powered voice assistant for inbound and outbound phone calls. Features include:
  - Natural language processing with intent detection
  - 100+ language support with accent and regional dialect accommodation
  - Handles conversational pauses, fillers, and speech impediments
  - Natural turn-taking and tone adjustment
  - Seamless escalation to live agents with full conversation context
  - Channel switching: can route from voice call to WhatsApp or other digital channels
  - Available 24/7 with no human agent required
  - Drag-and-drop builder for creating call flows, combining IVR and AI logic
  - Synthetic AI voices powered by ML and natural language understanding

- **Clerk Chat Voice AI Partnership** (announced September 2025): Infobip selected Clerk Chat as its top-tier Voice AI partner, integrating Clerk Chat's conversational AI into Infobip's global voice infrastructure. Full global rollout planned throughout 2026. This partnership targets enterprise-scale deployments requiring sophisticated NLP and conversational intelligence.

- **Vocalize** (2025 feature in AI Hub): An AI-powered voice gamification tool — users compete by speaking phrases matched against an AI-scored waveform. Used in marketing campaigns (e.g., Nissan KSA WhatsApp campaign achieving 200% engagement uplift). Note: Vocalize is a marketing/engagement tool, not a customer service voice agent.

- **CXOP (Conversational Experience Orchestration Platform)**, launched June 2025: An agentic AI platform built on Microsoft Azure OpenAI. Supports no-code and full-code deployment of AI agents across WhatsApp, RCS, web chat, voice, and more. AI agents understand intent, execute context-sensitive workflows, and handle hybrid human-in-the-loop scenarios.

- **AgentOS**, announced February 2026 (GA April 2026): Infobip's fully AI-native platform layer unifying marketing, sales, and support into one agentic system. Operates autonomously across SMS, RCS, email, WhatsApp, voice, and 15+ channels. Integrates Model Context Protocol (MCP) servers for AI-to-third-party system interactions (e.g., booking, 2FA, CRM actions).

**Key gap**: Infobip's voice AI is enterprise-grade and requires significant technical integration. There is no documented "no-code AI voice agent builder for WhatsApp calling" equivalent to Wati's Astra. Their AI voice product and WhatsApp Calling product are separate — there is no publicly documented native integration between the two (i.e., a WhatsApp call answered by an AI voice agent natively within Infobip's platform) as of March 2026.

### Core Platform Capabilities

- **Omnichannel messaging**: SMS, WhatsApp, RCS, Viber, email, voice, LINE, Telegram, Apple Messages for Business, and 15+ channels from a single API and dashboard
- **Conversations (Contact Center)**: AI-powered cloud contact center with shared inbox, omnichannel agent panel, chatbot/IVR integration, auto-assignment, tagging, macros, workflow automation, CSAT, and real-time analytics. Natively handles WhatsApp, Viber, voice, and 15+ channel types in one agent interface
- **Answers (Chatbot Builder)**: No-code drag-and-drop chatbot builder with intent-based AI, named entity recognition (NER), multi-language support, multi-channel deployment (15+ channels), template library, and real-time analytics dashboard
- **Moments (Customer Journey Automation)**: Marketing automation and customer journey orchestration — behavioral triggers, audience segmentation, AI-optimized send timing, personalized campaigns across channels
- **Integrations**: Native CRM integrations with Salesforce, HubSpot, Zendesk, Microsoft Dynamics 365, Oracle Eloqua, Oracle Fusion Service. Open API for custom integrations

### Notable Strengths

- Gartner Magic Quadrant Leader for CPaaS — one of the most credible enterprise cloud communications brands globally
- 195+ country coverage with a direct carrier network, enabling reliable message delivery at massive scale
- Truly omnichannel: 15+ natively integrated channels under one platform, including rare channels like Viber and RCS
- Early mover on WhatsApp Business Calling (July 2025 launch via Meta API) with full call recording, routing, and agent management
- Deep enterprise integrations with Salesforce, HubSpot, Oracle, Microsoft Dynamics — strong for large organizations with complex CRM ecosystems

### Missing / Weak Areas (vs. Wati)

- **No documented native AI voice agent for WhatsApp calls**: Infobip's Voice AI and WhatsApp Calling are separate products with no publicly documented native AI-answers-WhatsApp-calls capability. Wati's Astra AI voice agent natively handles WhatsApp calls end-to-end
- **No self-serve SMB pricing for WhatsApp Calling**: Infobip requires custom quotes; there are no transparent tiered plans (Growth/Pro/Business style) with WhatsApp Calling included. Wati offers it on all three tiers
- **No-code Voice AI for WhatsApp calling not documented**: Wati's Astra uses a no-code builder specifically for voice AI on WhatsApp. Infobip's no-code tools exist for chatbots and IVR, but the integration between WhatsApp Calling and an AI voice agent in a no-code flow is not publicly documented
- **Complexity and onboarding burden**: Infobip requires significant technical expertise. Wati's SMB-friendly setup and WhatsApp-first simplicity wins for teams without dedicated engineering resources
- **Language switching in live calls not documented**: Wati's Astra supports live language switching during a call (30+ languages). Infobip supports 100+ languages for their AI Voice Assistant on traditional phone calls, but live language switching during a WhatsApp Business Call is not publicly documented



## Pricing Tiers

Infobip does not publish fixed tiered pricing. All plans are custom-quoted based on message volume, channels, countries, and product modules selected.

- **WhatsApp Messaging**: Charged per conversation (24-hour session), with pricing varying by category (Marketing, Utility, Authentication, Service) and destination country. First 1,000 user-initiated service conversations per month per registered WABA are free.
- **SMS**: Pay-as-you-go, per message, with volume discounts for enterprise
- **Platform/Conversations/Answers/Moments**: Custom enterprise pricing — requires a sales conversation. No publicly listed monthly subscription tiers
- **WhatsApp Business Calling**: No public per-minute pricing. Contact Infobip directly for call pricing. Likely enterprise-only contracts
- **AgentOS**: Available from April 2026; pricing not publicly disclosed

**Review sites note** (G2, Capterra, SaaSWorthy): Multiple reviewers cite cost as a barrier, noting Infobip is "more suitable for medium or large organizations" and that pricing complexity can be overwhelming for smaller businesses.

Analysis: Infobip's pricing model is fundamentally enterprise-oriented and opaque to SMBs. Wati's transparent tiered pricing (Growth/Pro/Business, per-minute outbound calls, inbound free) is a significant competitive advantage for SMBs evaluating both platforms. Wati wins on pricing accessibility and predictability; Infobip wins on volume discounts and contractual flexibility at enterprise scale.



## Target Market

Primary: Large enterprises, mid-market companies, telecoms, financial services, retail/ecommerce, healthcare, and government organizations needing multi-channel, high-volume communications infrastructure across multiple countries

Secondary: Mid-market businesses in APAC, MENA, and Eastern Europe seeking programmable communications with WhatsApp as a primary channel alongside SMS and voice

Less focused on: SMBs needing a simple, WhatsApp-first platform with self-serve onboarding, transparent pricing, and no need for developer resources. Infobip's complexity, custom pricing, and enterprise sales motion make them a poor fit for small teams under 50 employees or businesses wanting to get started in days rather than weeks.



## Strengths

- **Global scale and infrastructure**: 195+ countries, 453B+ annual interactions, direct carrier relationships, and enterprise-grade reliability and compliance
- **Gartner Magic Quadrant Leader**: CPaaS market recognition positions Infobip credibly with enterprise procurement teams and IT decision-makers
- **WhatsApp Business Calling early mover**: Launched native WhatsApp Calling via Meta API in July 2025, with inbound/outbound support, call recording, agent management, and CTA templates
- **Omnichannel breadth**: 15+ native channels (SMS, WhatsApp, RCS, Viber, email, voice, LINE, Telegram, and more) in a single platform — no competitor in SMB space matches this breadth
- **AI investment trajectory**: CXOP (June 2025), Clerk Chat Voice AI partnership (September 2025), and AgentOS (February 2026) signal aggressive AI-native evolution
- **Enterprise CRM integrations**: Deep, native integrations with Salesforce, HubSpot, Oracle, Zendesk, and Microsoft Dynamics — critical for enterprise workflows
- **Developer ecosystem**: Comprehensive APIs, SDKs, documentation hub, and a strong developer community for custom implementations



## Weaknesses

- **Pricing opacity**: No public pricing for any product tier, including WhatsApp Calling and Voice AI. Makes evaluation and self-serve adoption impossible for SMBs
- **SMB inaccessibility**: High complexity, required technical resources, and enterprise sales process create high friction for small businesses. Wati's self-serve model is far superior for SMBs
- **No integrated AI voice agent on WhatsApp calls**: The most notable gap — no publicly documented product that combines WhatsApp Business Calling with an AI voice agent in a unified, no-code flow. Wati's Astra does this natively
- **Voice AI via third-party partnership**: Infobip's flagship Voice AI going forward relies on a partnership with Clerk Chat (announced September 2025, full rollout 2026) rather than a fully proprietary native solution — introducing dependency risk
- **Complex UI and learning curve**: G2 and Capterra reviewers note the interface can be confusing, function naming conventions are non-intuitive, and onboarding requires significant time investment
- **Customer support challenges at scale**: Multiple G2 reviews cite slow support response times, unclear escalation paths, and limited hands-on integration support — particularly problematic for SMBs without dedicated IT teams
- **WhatsApp Calling is newer than Wati's**: Infobip's WhatsApp Calling launched July 2025; Wati launched earlier and has additional SMB-oriented features (missed call notifications, agent performance tracking, business hours control) that may not yet be fully matched in Infobip's enterprise-oriented implementation



## Comparison to Wati

### Where Infobip Wins:
- Omnichannel breadth: 15+ channels vs. Wati's WhatsApp-first focus
- Global infrastructure and enterprise-grade reliability at 200+ country scale
- Gartner recognition and enterprise brand credibility
- Deep native CRM integrations (Salesforce, Oracle, Microsoft Dynamics)
- Call recording natively integrated within contact center flows
- Broader AI platform vision (AgentOS, CXOP) for enterprise automation
- Language support breadth: 100+ languages for Voice AI vs. 30+ for Wati Astra
- Developer API flexibility and programmability

### Where Wati Wins:
- **WhatsApp Calling for SMBs**: Available on all three pricing tiers (Growth, Pro, Business) with transparent per-minute pricing — no custom quote needed
- **Native AI voice agent on WhatsApp calls (Astra)**: Wati's Astra is the only documented product that natively handles WhatsApp Business Calls with an AI voice agent in a no-code flow. Infobip has no equivalent integrated product as of March 2026
- **No-code simplicity**: Wati's no-code builder for Astra (AI voice agent) is accessible to non-technical SMB users. Infobip's AI and calling products require developer or integration effort
- **Live language switching during calls**: Wati Astra supports real-time language switching mid-conversation — not documented for Infobip's WhatsApp Calling product
- **Transparent, SMB-friendly pricing**: Wati publishes tier prices; Infobip requires a sales conversation. Wati wins on speed-to-value for SMBs
- **SMB onboarding speed**: Wati is designed for self-serve, days-to-launch onboarding. Infobip's enterprise motion means weeks-to-months implementation timelines
- **WhatsApp-specific feature depth for SMBs**: Missed call notifications, agent performance tracking per call, business hours control for WhatsApp Calling — Wati has purpose-built these for SMB workflows

### Strategic Positioning Against Infobip:
Wati is the only WhatsApp Business platform that gives SMBs both native WhatsApp Business Calling and an AI voice agent (Astra) in a single, no-code, self-serve product — Infobip requires enterprise contracts, custom integration work, and still lacks a documented native AI-voice-on-WhatsApp-calls solution as of early 2026.

Win scenarios:
- SMB or mid-market prospect evaluating WhatsApp-first communications needs — Wati's simplicity and transparent pricing win
- Any team without dedicated developer resources — Wati's no-code setup is deployable in days vs. Infobip's weeks
- Deals where the buyer specifically wants WhatsApp Calling with AI voice automation — Wati Astra is purpose-built for this; Infobip cannot yet match the integrated experience
- Price-sensitive customers or startups — Infobip's custom enterprise pricing is a non-starter for companies under ~$1M ARR
- Use cases requiring live language switching during AI voice calls — Wati Astra's 30+ language live-switch capability is documented; Infobip's is not for WhatsApp calls
- Companies that want to get started within a week — Infobip's enterprise onboarding timeline kills deals that require speed



## Recent Updates & Trends

- **July 2025 (Q3 2025)**: Infobip launches native WhatsApp Business Calling via Meta's API — inbound/outbound calls, branded caller ID, call recording via Conversations, CTA button templates, and API access. Major competitive milestone.
- **June 2025 (Q2 2025)**: CXOP (Conversational Experience Orchestration Platform) unveiled — agentic AI platform built on Azure OpenAI for orchestrating AI-driven customer journeys across WhatsApp, RCS, voice, and web chat with no-code and full-code options.
- **September 2025**: Infobip selects Clerk Chat as top-tier Voice AI partner — integrating advanced conversational AI into Infobip's global voice infrastructure (100B+ minutes/year). Full global rollout planned through 2026.
- **November 2025**: Nissan KSA campaign using Infobip's Vocalize AI gamification on WhatsApp achieves 200% engagement increase — demonstrates enterprise marketing AI capability.
- **February 2026**: AgentOS announced (GA April 2026) — AI-native orchestration layer unifying marketing, sales, and support. Integrates MCP servers for AI-to-third-party system actions. Positions Infobip as moving from CPaaS to "intelligent CX operating system."
- **Q2 2025**: Enhanced Salesforce, HubSpot, Oracle Eloqua, Oracle Fusion Service, and Microsoft Dynamics 365 integrations.
- **Ongoing 2025**: $520M line of credit secured July 2025 — signals continued aggressive investment in platform and geographic expansion.

Strategic Threat Level: MEDIUM

Infobip is a well-funded, technically sophisticated CPaaS leader that has now launched WhatsApp Business Calling and is aggressively building AI voice capabilities. However, their enterprise focus, opaque pricing, high complexity, and lack of a documented integrated AI-voice-on-WhatsApp-calls product (as of March 2026) mean they are not an immediate threat to Wati's core SMB market. The threat could escalate to HIGH if Infobip launches a simplified SMB-tier with transparent pricing for WhatsApp Calling + AI voice, or if their Clerk Chat Voice AI integration matures into a no-code product accessible to smaller customers.



## Recording, GenAI & Mobile Calling

### Call Recording

Call recording for WhatsApp Business calls is available via Infobip's Conversations contact center layer — it is not provided natively by Meta's WhatsApp Business Calling API; Infobip adds it as an additional integration layer on top.

**Automatic vs. manual**: Recording is configured at the account or route level via Conversations settings (Call add-ons page). When the recording toggle is enabled in Advanced options, all answered calls are recorded automatically — agents do not need to manually trigger recording per call. There is no documented per-call manual toggle that agents can start or stop mid-call from the agent interface.

**What gets recorded**: Audio-only, video-only, or both (audio + video) — configurable. Each participant's audio can be stored as separate files or a unified (mixed) file.

**Storage**: Two options — (1) Infobip cloud storage (default, stored indefinitely), or (2) SFTP server (recordings pushed to a customer-owned secure file transfer server for local storage). SFTP configuration is done via Conversations settings. The same storage configuration applies to WhatsApp Business calls managed through Conversations.

**Scope**: Recording applies to inbound calls, outbound calls, or both — configurable per route.

Sources: [Conversations: Calls](https://www.infobip.com/docs/conversations/calls), [Keep a Recording of Customer Communication](https://www.infobip.com/docs/tutorials/keep-a-recording-of-customer-communication), [How to manage recording settings](https://support.infobip.com/manage-recording-settings-in-infobip)

### AI Transcription & Summarization

**Transcription**: Available via Infobip's Calls API. Transcription is started and stopped programmatically using `start transcription` / `stop transcription` API methods on a call leg. The API supports receiving both INTERIM (real-time streaming) and COMPLETE transcripts, or COMPLETE transcripts only. The application must have a subscription that includes the `TRANSCRIPTION` event type.

Q2 2025 enhancements added: punctuation formatting, proper casing, numeral normalization (e.g., "five" → 5), disfluency filtering (removes filler words like "um," "uh"), and support for custom dictionaries to improve recognition accuracy for domain-specific vocabulary. Language selection is also configurable at the transcription start.

Transcription is positioned as an API/developer feature for long-duration calls or post-call full transcription — it is not documented as a one-click in-interface toggle for agents within the Conversations UI.

**AI Summarization**: Available. Infobip Conversations includes an on-demand AI-generated conversation summary. Agents click a button to generate a summary of the current or past interaction. The summary covers key topics, context, and history from both chatbot and agent turns in the conversation. Summarization language support includes English, Spanish, Portuguese, Arabic, Chinese (Simplified), and Croatian. Admins can configure which queues have access to the on-demand summary feature.

**Important limitation on transcription + summarization for WhatsApp calls specifically**: Transcription via the Calls API is documented for the Voice channel (traditional VoIP/PSTN calls and WebRTC). There is no publicly documented confirmation that the Calls API transcription endpoint is directly applicable to WhatsApp Business Calling call legs within the Conversations product. The AI conversation summary in Conversations is documented for text-based chat interactions; whether it synthesizes audio call transcripts into a post-call summary specifically for WhatsApp voice calls is not publicly documented as of March 2026.

Sources: [Start transcription - Infobip API](https://www.infobip.com/docs/api/channels/voice/calls/call-legs/call-start-transcription), [Conversations productivity docs](https://www.infobip.com/docs/conversations/conversations-setup/productivity), [Product Updates Q2 2025](https://www.infobip.com/product-updates/product-updates-q2-2025)

### Other GenAI on Voice

**Sentiment analysis**: Available within the Conversations platform. The platform surfaces automated sentiment analysis as part of agent and supervisor dashboards — agents and supervisors can view median sentiment scores per conversation across a selected time period. Infobip's documentation also references the ability to stream a call leg's audio to an external sentiment analysis service via the Calls API, meaning customers can pipe live audio to their own third-party sentiment engine.

**Supervisor/coaching on live calls**: Available via Infobip's conference call features. Supervisors can join a live call in a coaching or silent-monitoring role using role assignments in conference sessions — enabling private coaching (whisper to agent only), silent supervision (listen-only), or passive attendance without disrupting the customer experience. This is a developer/API-configured feature, not a one-click supervisor panel toggle.

**Real-time agent assist**: The Conversations platform includes an AI assistant that surfaces suggested replies, previous interaction summaries, macros, templates, and Knowledge Base content to agents during live conversations. Whether this AI assistant is triggered by voice call content in real-time (i.e., from live call audio) or is limited to text-based channel context is not publicly documented.

**CRM auto-fill from call content**: Not publicly documented.

**Call highlights**: Not publicly documented as a discrete feature.

**AI voice gamification (Vocalize)**: Available as a marketing-oriented tool — not a call analysis feature. Vocalize allows end customers to speak phrases scored by AI against a waveform, used in campaign activations (e.g., Nissan KSA WhatsApp campaign, November 2025). Not applicable to contact center call analysis.

Sources: [Conversations: Supervisor guide](https://www.infobip.com/docs/conversations/supervisor-guide), [Conversations: Analytics](https://www.infobip.com/docs/conversations/analytics), [AI Cloud Contact Center](https://www.infobip.com/conversations)

### Mobile App Calling

**Available on iOS and Android.** Infobip's Conversations mobile app is available on the Apple App Store (requires iOS 15.0+), Google Play Store, and Huawei AppGallery.

Agents can make and receive WhatsApp Business calls directly from the mobile app — the app supports phone calls, Live Chat calls, and WhatsApp calls in a single unified interface. WhatsApp calling support was added to the mobile app as part of the July 2025 WhatsApp Business Calling launch.

Agents can initiate or receive WhatsApp calls, switch from an active WhatsApp chat to a voice call within the same conversation, and maintain full conversation history context across the mobile interface — the same behavior as the web/desktop Conversations platform.

WhatsApp calling on mobile is not limited to web-only. Both inbound and outbound WhatsApp Business calls are supported from the Conversations iOS and Android apps.

Sources: [Conversations mobile app docs](https://www.infobip.com/docs/conversations/conversations-mobile-app), [App Store listing](https://apps.apple.com/us/app/infobip-conversations/id1537124685), [Google Play listing](https://play.google.com/store/apps/details?id=com.infobip.conversations), [Infobip brings voice calling to WhatsApp Business users](https://www.infobip.com/news/infobip-brings-voice-calling-whatsapp)

### Wati Comparison Note

Infobip has a more mature and configurable call recording infrastructure than Wati — supporting automatic recording with cloud or SFTP storage options, per-participant audio tracks, and API-driven transcription with Q2 2025 formatting enhancements — while Wati's call recording and transcription capabilities for WhatsApp Business Calling are not publicly documented at equivalent depth. On mobile calling, Infobip's Conversations app explicitly supports WhatsApp Business calls on iOS and Android, giving it parity or advantage over Wati here; Wati's mobile app calling support for WhatsApp Business Calling is not comprehensively documented publicly as of March 2026. The key gap that remains on Infobip's side is the absence of a native, no-code AI voice agent that answers WhatsApp calls autonomously — Wati's Astra does this end-to-end, which Infobip has not matched.
