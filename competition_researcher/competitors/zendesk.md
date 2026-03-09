# Competitor Brief: Zendesk

Last Updated: March 2026 (WhatsApp Calling re-verified; Recording/GenAI/Mobile section updated)
Analyst: Wati Product Team



## Overview

Zendesk is a Copenhagen-founded (2007), San Francisco-headquartered customer experience software company that was taken private in June 2022 via a $10.2B acquisition by private equity firms Permira and Hellman & Friedman. The company generates approximately $1.93B in annual revenue (2024) with ambitions toward $3.4B by 2025. While Zendesk built its early reputation on SMB-friendly help desk ticketing, it has aggressively moved upmarket: over 50% of revenue now comes from enterprise clients, and it has 140 customers paying over $1M annually. It serves over 160,000 businesses globally across industries including retail, SaaS, financial services, and healthcare.

Zendesk's relevance to Wati is primarily as a large, well-resourced omnichannel customer service platform that supports WhatsApp as a messaging channel. Their integration lets support teams manage WhatsApp conversations inside the Zendesk Agent Workspace alongside email, chat, and social, creating a unified ticket-based inbox. However, Zendesk's WhatsApp support is fundamentally a text/messaging integration - it does not natively support WhatsApp Business Calling (voice calls via Meta's WhatsApp Business Calling API). Zendesk's voice strategy is built around its own VoIP product, Zendesk Talk, and a new contact center offering built on Amazon Connect - neither of which is native WhatsApp calling.

On AI, Zendesk is investing heavily. Through acquisitions (Ultimate in March 2024, Klaus in February 2024, Local Measure in May 2025, HyperArc in July 2025, Unleash in December 2025) and internal R&D, they have assembled a layered AI offering spanning AI Agents (chatbots), Agent Copilot (human-assist), voice AI (currently in EAP/early access, English-only), and an advanced analytics layer. Their stated ambition is to resolve 80% of support interactions autonomously via what they call the "Resolution Platform." This makes them a growing but still enterprise-focused competitive threat - particularly for larger businesses already using Zendesk for helpdesk who want to add WhatsApp support, rather than for SMBs looking for a native WhatsApp-first platform.



## Key Features

### WhatsApp Calling
- **No native WhatsApp Business Calling support — confirmed as of March 2026.** Zendesk's WhatsApp integration is messaging-only. This has been thoroughly verified against Zendesk's official product pages, support documentation, community forum, and all release notes through February 27, 2026. There is no WhatsApp Business Calling feature, no EAP, and no roadmap announcement.
- The underlying constraint is a Meta platform rule: once a phone number is registered with the WhatsApp Business API (as Zendesk requires for its integration), that number can no longer receive WhatsApp voice or video calls. Zendesk has not worked around this or built any feature to bridge it. This is explicitly documented in Zendesk's own support articles: "After you add your WhatsApp number for messaging, you will no longer be able to use that number to receive calls in WhatsApp."
- WhatsApp messaging integration is available on all Suite plans; it routes WhatsApp text messages into Zendesk tickets in the unified Agent Workspace.
- Supports inbound and outbound WhatsApp text messages, rich media (images, video, documents), and quick-reply buttons (via WhatsApp Templates).
- AI agents (chatbots) can be deployed on the WhatsApp channel for automated text-based interactions.
- **Meta launched the WhatsApp Business Calling API in July 2025.** As of March 2026 — approximately 8 months after Meta's launch — Zendesk has made zero announcements about integrating this API. No blog post, no EAP, no community post, no release note, no developer documentation. This is not a gap Zendesk is visibly working to close.
- Voice calling for customer support is handled through Zendesk Talk (VoIP, not WhatsApp) or through the Amazon Connect-based Zendesk Contact Center product — both of which are entirely separate from the WhatsApp channel.
- Third-party marketplace apps (e.g., PickyAssist, Scriba Vox) can add limited voice message transcription or WhatsApp audio recording tools on top of Zendesk, but these are not native Zendesk capabilities and do not provide live WhatsApp voice calling.

Sources: [Zendesk WhatsApp integration for business](https://www.zendesk.com/service/messaging/whatsapp-business/), [Adding WhatsApp channels to Agent Workspace](https://support.zendesk.com/hc/en-us/articles/4408842821786-Adding-WhatsApp-channels-to-the-Agent-Workspace), [Zendesk community thread: WhatsApp calls](https://support.zendesk.com/hc/en-us/community/posts/4699816067610-Whatsapp-calls), [Release notes through 2026-02-27](https://support.zendesk.com/hc/en-us/articles/10369773226394-Release-notes-through-2026-02-27)

### Voice AI / Conversational AI
- **Zendesk Voice AI Agents (EAP):** Currently in early access program (EAP opened February 12, 2026 per documentation). Available to customers with a Zendesk Voice (Talk) plan plus the AI Agents Advanced add-on.
- Voice AI agents are built on large language models (GPT-4/GPT-5 in collaboration with OpenAI) and can handle end-to-end phone support autonomously: greeting, intent capture, resolution, and wrap-up.
- Claims to resolve over 50% of incoming phone calls without human escalation, with long-term aspirations toward 80%+ resolution.
- Automatically creates a full transcript and call summary after every call.
- Supports seamless escalation to human agents with full conversation context carried into Agent Workspace.
- **English-only during EAP.** Multi-language voice support is planned but not yet available.
- Operates over traditional phone (Zendesk Talk / PSTN), not over WhatsApp.
- AI Agents for text/messaging (chat, email, WhatsApp) support 80+ languages and are generally available.
- Agent Copilot provides real-time AI suggestions during live voice calls for human agents (available on Advanced AI add-on).
- Voice AI is NOT available as a standalone WhatsApp voice product; it applies to phone line automation only.
- Acquired Local Measure (May 2025) to bolster Amazon Connect-based contact center voice AI capabilities at enterprise scale.

### Core Platform Capabilities
- **Omnichannel Unified Inbox:** Email, chat, phone (Talk), WhatsApp, Facebook Messenger, Instagram, X (Twitter), SMS all route into a single Agent Workspace with shared ticket history and context.
- **Zendesk Talk (VoIP):** Native cloud telephony with IVR, call recording, call transcription (AI-powered), group routing, call queues, CSAT, and usage-based per-minute billing. Local numbers available in many countries. Requires Suite subscription plus usage fees ($0.037/min inbound US/Canada, $0.022/min outbound US/Canada).
- **AI Agents (Chatbots):** AI Agents Essentials included in all Suite plans for messaging and email; AI Agents Advanced (add-on) adds conversation flows, API/orchestration, hybrid scripted+generative flows, and analytics. Pre-trained on billions of CX interactions. 80+ language support for text channels.
- **Automation & Workflows:** Triggers, automations, macros, SLAs, skills-based routing. New Action Builder (low-code, announced October 2025) connects to OpenAI, Shopify, Confluence, Microsoft Teams/Outlook/Excel. App Builder enables non-technical teams to build custom apps via natural language.
- **Analytics (Zendesk Explore):** Built-in reporting and dashboards. Advanced Insights powered by HyperArc (acquired July 2025) adds AI-narrative analytics, trend detection, and root cause analysis.
- **Knowledge Management:** Help Center (Guide), Knowledge Builder (auto-generates articles from past tickets), and Knowledge Connectors (integrates Confluence, Google Drive, SharePoint).
- **Quality Assurance:** Zendesk QA (from Klaus acquisition) for AI-powered call/chat quality scoring.
- **Workforce Management:** Staffing forecasting and scheduling (add-on, $25/agent/month).

### Notable Strengths
- Enterprise-grade omnichannel platform with 17+ years of market presence and deep integrations ecosystem (1,200+ marketplace apps).
- Aggressive AI investment: acquisitions of Ultimate, Klaus, Local Measure, HyperArc, Unleash in 2024-2025 have meaningfully expanded AI and voice capabilities.
- Zendesk Contact Center (built on Amazon Connect + AWS) is now a serious enterprise CCaaS competitor, strategic AWS partnership announced December 2025.
- Strong brand recognition and trust with mid-market and enterprise buyers; rated ~4.3/5 on G2 from 6,600+ reviews.
- AI Copilot for human agents with real-time suggestions, tone adjustment, ticket summaries, and smart macros - well-regarded in reviews.

### Missing / Weak Areas (vs. Wati)
- **No native WhatsApp Business Calling.** Does not support voice calls through WhatsApp at all - a fundamental gap versus Wati's WhatsApp Calling feature.
- **Voice AI (phone) is English-only during EAP** and tied to traditional phone lines, not WhatsApp. Wati's Voice AI (Astra) supports 30+ languages with live switching.
- **No no-code WhatsApp voice bot builder.** Zendesk's AI voice is enterprise-focused and requires the AI Agents Advanced add-on ($50/agent/month on top of a $115/agent/month plan).
- **Not WhatsApp-native.** Zendesk is a helpdesk that added WhatsApp as a channel. Wati is purpose-built for WhatsApp Business with deep Meta BSP integration, verified badge, campaign broadcasting, and WhatsApp-specific features.
- **SMB pricing is prohibitive for true SMBs.** A team of 5 agents on Suite Professional with Advanced AI would cost $825+/month vs. Wati's SMB-accessible plans.



## Pricing Tiers

**Zendesk Suite Plans (per agent/month, billed annually):**

| Plan | Price | Key Features |
|---|---|---|
| Suite Team | $55/agent/month | Ticketing, omnichannel messaging (WhatsApp included), help center, basic AI, Zendesk Talk (usage-billed separately) |
| Suite Growth | $89/agent/month | + Self-service portal, SLAs, multilingual support, CSAT |
| Suite Professional | $115/agent/month | + Skills-based routing, community forums, custom analytics, HIPAA compliance, AI Agents Advanced eligible |
| Suite Enterprise | $169+/agent/month (custom) | + Sandbox, custom agent roles, enterprise-grade security and scale |

**Key Add-Ons:**
- Advanced AI: $50/agent/month (requires Professional+) — includes Agent Copilot, intelligent triage, generative writing tools, advanced AI agents, voice AI EAP access
- Workforce Management: $25/agent/month
- Quality Assurance: $25+/agent/month
- Zendesk Talk usage: ~$0.037/min inbound, ~$0.022/min outbound (US/Canada); local numbers from $2/month
- AI automated resolutions: $1.50/AR (committed) or $2.00/AR (pay-as-you-go) beyond plan inclusion

**Zendesk Support Plans (ticketing-only, no voice/chat):**
- Support Team: $19/agent/month
- Support Professional: $55/agent/month
- Support Enterprise: $115/agent/month

Analysis: Zendesk's effective total cost for a team wanting omnichannel + AI + voice is $165-$300+/agent/month, making it 3-6x more expensive than Wati for an equivalent SMB team. Wati's per-conversation pricing model and flat subscription tiers are significantly more accessible for SMBs, while Zendesk's value proposition is designed for mid-market and enterprise buyers who can absorb per-agent costs across large teams.



## Target Market

Primary: Mid-market and enterprise companies (100-10,000+ employees) needing a scalable, multi-channel customer service platform with ticketing, automation, and analytics. More than 50% of Zendesk's revenue now comes from enterprise clients.

Secondary: Growth-stage startups and SMBs (especially tech-forward ones) that start on lower-tier plans and scale up. Zendesk still has a large SMB user base from its early days, though it has deprioritized this segment commercially.

Less focused on: Micro-businesses, solo operators, and SMBs primarily communicating through WhatsApp in emerging markets (Southeast Asia, India, Latin America, MENA). These customers typically find Zendesk too complex, too expensive, and not optimized for WhatsApp-first workflows. This is Wati's core territory.



## Strengths

- **Market leadership and brand trust:** One of the most recognized names in customer service software globally; widely deployed across SaaS, e-commerce, financial services, healthcare, and government.
- **Acquisitive AI strategy:** Five acquisitions in 2024-2025 (Ultimate, Klaus, Local Measure, HyperArc, Unleash) have rapidly expanded AI capabilities in voice, quality assurance, analytics, and knowledge management.
- **Enterprise voice and CCaaS:** The Amazon Connect-powered Zendesk Contact Center, combined with Local Measure's technology, positions Zendesk as a serious enterprise CCaaS competitor with AI-powered IVR and voice automation.
- **Omnichannel depth:** Genuinely unified inbox across 10+ channels with shared context, ticket history, SLAs, and routing - hard to replicate for WhatsApp-only platforms.
- **AI Copilot for agents:** Real-time in-call and in-ticket suggestions, tone adjustment, ticket summaries, and auto-assist procedures - rated highly by enterprise support teams in G2 reviews.
- **Developer ecosystem and integrations:** 1,200+ marketplace apps, open APIs, Zendesk Sunshine platform for custom data modeling, and strong partner network.
- **AWS strategic alignment:** Deep integration with Amazon Connect, AWS Bedrock (multi-model AI), and availability on AWS Marketplace - significant for enterprise IT procurement.



## Weaknesses

- **No native WhatsApp Business Calling — confirmed March 2026.** This is a structural gap. Zendesk's WhatsApp integration is text-only. Despite Meta launching the WhatsApp Business Calling API in July 2025, Zendesk had made zero announcements about integrating it as of March 2026 (8 months post-launch). There is no EAP, no roadmap announcement, no developer documentation, and no community post from Zendesk on the topic. For any business that wants to make or receive voice calls through WhatsApp, Zendesk cannot deliver this natively.
- **Voice AI is English-only and early-stage.** The Voice AI Agents EAP supports English only. Wati's Astra supports 30+ languages with live switching. For multilingual markets (Southeast Asia, Latin America, India), this is a significant gap.
- **Voice AI is phone-line only, not WhatsApp.** Zendesk's voice AI applies to traditional phone (Zendesk Talk / Amazon Connect), not to WhatsApp voice calls. These are completely separate stacks.
- **High complexity and setup cost for SMBs.** G2 reviewers consistently cite Zendesk's setup complexity, the need for dedicated admins, and the difficulty of managing triggers/automations over time. The mobile app is also criticized for lag and limited functionality vs. desktop.
- **Pricing is prohibitive for small teams.** Real-world total cost of $165-$300+/agent/month makes Zendesk inaccessible for true SMBs. Adding AI and voice features compounds cost quickly.
- **Not WhatsApp-first.** Zendesk treats WhatsApp as one of many channels in a ticket-based system. It lacks WhatsApp-specific features such as campaign broadcasting, contact-level WhatsApp opt-in management, WhatsApp-native call analytics, or WhatsApp verified badge management.
- **Upmarket shift creates SMB attrition risk.** Zendesk's strategic focus on enterprise has led to pricing increases and feature complexity that increasingly alienates the SMB segment it was originally built for - creating a natural opening for WhatsApp-native platforms like Wati.



## Comparison to Wati

### Where Zendesk Wins:
- Full omnichannel helpdesk (email, phone, chat, social, WhatsApp) in one platform - better for teams that support customers across all channels, not just WhatsApp
- Enterprise-grade ticketing, SLAs, skills-based routing, reporting, and governance
- AI Copilot for live agent assist with real-time suggestions during calls and tickets
- Traditional phone/VoIP support (Zendesk Talk) and enterprise CCaaS (Amazon Connect integration) at scale
- Knowledge base and Help Center with AI-generated article suggestions and external knowledge connectors (Confluence, Drive, SharePoint)
- Quality assurance (QA) capabilities from Klaus acquisition, scoring automated and human interactions
- Stronger brand recognition and enterprise sales motion in North America and Europe
- Better for regulated industries (HIPAA compliance, ISO 42001 AI certification, SOC2)

### Where Wati Wins:
- **Native WhatsApp Business Calling** - Wati has it, Zendesk does not. Inbound and outbound voice calls via WhatsApp, one-click call from chat, call CTA buttons in templates, business hours control, call analytics - none of this exists in Zendesk's WhatsApp integration.
- **Voice AI on WhatsApp (Astra)** - Wati's AI voice agent operates on WhatsApp natively. Zendesk's Voice AI runs on phone lines only, in English only. Astra supports 30+ languages with live language switching.
- **WhatsApp-first design** - Wati is purpose-built for WhatsApp Business API, with deep campaign, broadcast, template, and contact management capabilities that Zendesk's ticket-based approach does not replicate.
- **SMB accessibility** - Wati's pricing model (per-conversation + flat subscription) is dramatically more affordable for small and medium businesses vs. Zendesk's per-agent model with mandatory add-ons.
- **No-code AI agent builder** - Wati's no-code builder for chatbots and Voice AI (Astra) lowers the technical barrier significantly compared to Zendesk's configuration-heavy setup.
- **WhatsApp campaign management** - Broadcast templates, marketing campaigns, contact segments, opt-in management - Zendesk has none of this natively.
- **Verified business badge management** - As a Meta BSP, Wati helps businesses obtain and leverage WhatsApp's verified badge. Zendesk is not a BSP.
- **Multilingual voice AI** - Astra's 30+ languages and real-time language switching vs. Zendesk's English-only Voice AI EAP.
- **Emerging market fit** - Wati serves 15,000+ customers across 100+ countries, with strong presence in Southeast Asia, India, Latin America, and MENA where WhatsApp is the dominant communication channel.

### Strategic Positioning Against Zendesk:
Wati is the only platform that combines native WhatsApp Business Calling, multilingual Voice AI on WhatsApp, and SMB-accessible pricing — Zendesk is a powerful omnichannel helpdesk that treats WhatsApp as a secondary text channel and has no native WhatsApp voice capability at all. This gap has been re-verified as of March 2026: despite Meta launching the WhatsApp Business Calling API in July 2025, Zendesk had made zero moves to integrate it in the 8 months since. When a business's primary customer communication channel is WhatsApp, Wati delivers a depth of WhatsApp-native functionality — including live voice calling, AI voice agents (Astra), and call analytics — that Zendesk cannot match at any price point.

Win scenarios:
- Prospect is an SMB in Southeast Asia, India, Latin America, or MENA where WhatsApp is the dominant customer channel
- Prospect specifically needs WhatsApp voice calling or wants to use WhatsApp Calling AI to handle inbound queries
- Prospect wants to run WhatsApp marketing campaigns alongside support (Zendesk has no broadcast/campaign capability)
- Prospect has a non-English speaking customer base and needs multilingual voice AI (Zendesk is English-only in EAP)
- Prospect has 2-50 agents and finds Zendesk's $55-$165+/agent/month pricing model unaffordable
- Prospect wants a no-code setup without dedicated Zendesk admins or technical configuration overhead
- Prospect is replacing a WhatsApp-only workflow (manually managed via WhatsApp Web) and needs purpose-built tooling, not a generic helpdesk
- Prospect wants inbound WhatsApp calls routed to AI before escalating to a human agent - Zendesk cannot do this via WhatsApp at all



## Recent Updates & Trends

- **Q1 2024 - Klaus Acquisition (February 2024):** Acquired AI-powered quality management platform Klaus to add automated QA scoring for agent conversations across all channels.
- **Q1 2024 - Ultimate Acquisition (March 2024):** Acquired service automation provider Ultimate to expand AI agent capabilities and no-code bot-building. Integrated as Zendesk AI Agents Advanced.
- **Q2 2025 - Local Measure Acquisition (May 2025):** Acquired CCaaS/voice provider Local Measure (long-standing AWS/Amazon Connect partner) to build out enterprise contact center voice capabilities. Result: Zendesk for Contact Center product.
- **Q2 2025 - Meta WhatsApp Business Calling API Launch (July 2025):** Meta launched the WhatsApp Business Calling API. Zendesk has NOT announced integration with this API as of March 2026, though this represents a future risk area.
- **Q3 2025 - HyperArc Acquisition (July 2025):** Acquired AI-native analytics platform to power Advanced Insights (narrative AI analytics, trend analysis, root cause detection).
- **Q4 2025 - AI Summit / Resolution Platform Launch (October 2025):** Major product launch event. Announced Voice AI Agents (EAP), Admin Copilot, Action Builder (low-code automation), App Builder (natural language app creation), Knowledge Builder (AI article generation), Video Calling & Screen Sharing, and claimed 80%+ autonomous resolution capability.
- **Q4 2025 - AWS Strategic Collaboration Agreement (December 2025):** Announced at AWS re:Invent. Deep partnership to deliver Zendesk Contact Center via Amazon Connect on AWS Marketplace, using Amazon Bedrock for multi-model AI.
- **Q4 2025 - Unleash Acquisition (December 2025):** Acquired AI-powered enterprise search/knowledge platform to connect employee knowledge across Slack, Teams, and other internal systems.
- **Q1 2026 - Voice AI Agents EAP Opens (February 2026):** General availability of Voice AI Agents early access program. Requires Zendesk Voice + AI Agents Advanced add-on. English-only.
- **Q1 2026 - March 2026 Release Notes:** Forwarding caller ID (configurable caller ID for IVR/overflow forwarded calls), form messages across all social messaging channels, AI agent ticket default on, auto-assist event logging, pre-approved low-risk custom actions for auto assist. No WhatsApp Calling announcements in any release note through February 27, 2026.
- **Q1 2026 - WhatsApp Business Calling Gap Re-Verified (March 2026):** Thorough re-verification across Zendesk's product pages, developer docs, release notes, community forum, and third-party review sites confirms Zendesk has NO WhatsApp Business Calling integration — 8 months after Meta's July 2025 API launch. The gap remains structural and unaddressed.

Strategic Threat Level: LOW-MEDIUM (for Wati's core SMB/WhatsApp market)

Zendesk is a formidable enterprise CX platform but is not a direct competitive threat to Wati's core positioning today. It lacks native WhatsApp Business Calling, its Voice AI is phone-only and English-only, its pricing is 3-6x higher than Wati for SMB use cases, and it is structurally designed as a multi-channel helpdesk rather than a WhatsApp-native platform. The threat could escalate to MEDIUM-HIGH if Zendesk integrates Meta's WhatsApp Business Calling API and extends Voice AI to WhatsApp channels, particularly if they offer it at competitive SMB pricing. Watch the WhatsApp Calling API integration roadmap and any announcements around SMB-focused pricing changes as the key signal to re-rate this threat level.



## Recording, GenAI & Mobile Calling

*Section last updated: March 2026. WhatsApp Calling re-verified; call recording plan availability corrected; transcription pricing updated; mobile app status confirmed.*

---

### Call Recording

Zendesk Talk call recording is available and configured at the account level by admins. There are three modes:

- **Automatic (opt-out):** All calls are recorded by default; callers can opt out by pressing 3.
- **Automatic (opt-in):** Calls are not recorded by default; callers can opt in by pressing 3.
- **No recording:** Recording is disabled entirely.

Admins can grant agents the ability to pause and resume recording mid-call to avoid capturing sensitive data (e.g., payment card numbers), supporting PCI compliance workflows. This is a separate "agent recording controls" toggle in Admin Center.

**Storage and retention:** Recordings are stored within Zendesk and are excluded from general account data storage limits. Admins can set automatic deletion after a configurable time period or retain recordings indefinitely. Manual deletion is also supported. Recording incurs a per-minute storage charge of approximately $0.003/minute.

**Plan availability (updated March 2026):** Call recording is available on **all Zendesk Suite plans — Team, Growth, Professional, Enterprise, and Enterprise Plus** — when paired with a Talk Team, Professional, or Enterprise plan. This is broader than previously documented; the earlier finding that recording required Suite Professional or above was incorrect as of current plan structures. Note: recording on lower-tier plans still incurs the per-minute usage charge.

**WhatsApp-specific:** Not applicable. Zendesk's WhatsApp integration is messaging-only. There is no WhatsApp voice calling in Zendesk, and therefore no WhatsApp-specific call recording capability. All recording functionality documented here applies exclusively to Zendesk Talk (traditional phone/VoIP calls).

Sources: [Managing call recording options](https://support.zendesk.com/hc/en-us/articles/4408831738266-Managing-call-recording-options), [Call recording FAQ](https://support.zendesk.com/hc/en-us/articles/4408828042010), [Zendesk call recording FAQ (Secondary Brand)](https://secondary-brand.zendesk.com/hc/en-us/articles/38390915538196-Zendesk-call-recording-FAQ), [Best practices for call recording](https://support.zendesk.com/hc/en-us/articles/4408827179162-Best-practices-for-call-recording)

---

### AI Transcription & Summarization

Zendesk offers both post-call transcription and generative AI call summarization for Zendesk Talk (phone). These are generally available (not EAP) for qualifying plan holders.

**Transcription:**
- Post-call transcription automatically converts recorded calls to text, attached to the ticket as an internal note.
- Supports 35 languages with automatic language detection for post-call transcription.
- Real-time transcription (speech-to-text during a live call) is available and required for the real-time AI Copilot suggestions feature; it incurs additional per-minute fees ($0.027/minute of transcribed audio as of 2025 pricing).
- Post-call transcription is charged at approximately $0.01/minute.
- Automatic speaker labeling (identifying agent vs. customer utterances) was added in 2025.
- Keyword boosting allows admins to specify domain-specific terms that should be prioritized in transcription accuracy — added in 2025.
- PII and PCI redaction is available (Advanced Data Privacy and Protection add-on): automatically redacts names, locations, SSNs, card numbers, expiry dates, and CVV codes from transcripts. Also added in 2025.

**AI Summarization:**
- After each call, generative AI produces a written summary posted as an internal note on the ticket. Agents do not need to manually write call notes. Generally available as of July 10, 2024.
- Powered by Deepgram (speech-to-text) and OpenAI Enterprise (summarization). Neither vendor uses customer inputs to train their models.
- Call transcripts are also analyzed for intelligent triage signals: entity detection, caller intent, language, and sentiment predictions.

**Plan requirements (updated March 2026):**
- Full call transcription and AI summarization require the **Copilot add-on** (formerly called Advanced AI, $50/agent/month) or the **Zendesk QA add-on**. These require Suite Professional ($115/agent/month) or higher.
- If you have the Copilot add-on, transcripts and summaries attach to tickets.
- If you have the Zendesk QA add-on, transcripts and summaries flow into the QA review workflow.
- Basic voicemail transcription (not full call transcription) is available on lower-tier plans without the add-on.
- Real-time transcription (for Copilot live suggestions) has additional per-minute usage fees.

Sources: [Using generative AI to create call summaries and transcripts](https://support.zendesk.com/hc/en-us/articles/6170157307162-Using-generative-AI-to-create-call-summaries-and-transcripts-on-tickets), [Call transcription and summarization FAQ](https://support.zendesk.com/hc/en-us/articles/7470764710298-Call-transcription-and-summarization-FAQ), [Getting started with AI features in the Zendesk Copilot add-on](https://support.zendesk.com/hc/en-us/articles/5608652527386-Getting-started-with-AI-features-in-the-Zendesk-Copilot-add-on)

---

### Other GenAI on Voice

**Real-time AI suggestions (Agent Copilot for Voice):**
Calls are transcribed in real-time during a live phone call. As the conversation progresses, the agent can request AI-generated suggestions; the Copilot reads the live transcript to surface relevant Help Center content as bite-sized recommendations. This rolled out on October 2, 2025. Enabling this feature for a group causes all calls to that group to be transcribed in real-time. Requires the Copilot add-on plus Talk.

**Voice AI Agents (EAP, opened February 12, 2026):**
Fully autonomous AI agents that can handle end-to-end phone calls: greeting, intent capture, resolution, and wrap-up via natural language. Built on large language models (OpenAI collaboration). Resolves 50%+ of incoming calls without human escalation. Creates full transcripts and call summaries automatically. Supports seamless escalation with full context carried into Agent Workspace. English-only during EAP. Requires Zendesk Voice (Talk) + AI Agents Advanced add-on. Operates over traditional phone (PSTN) only — not over WhatsApp.

**Sentiment analysis (Zendesk QA / Klaus):**
Zendesk QA applies AI-powered sentiment analysis to 100% of voice call transcripts post-call. Flags negative sentiment, churn risk, escalation triggers, dead air, missing disclosures, and compliance gaps. Requires the Zendesk QA add-on ($25+/agent/month).

**Agent coaching:**
Zendesk QA's findings feed into a coaching workflow: managers can review flagged calls, annotate with specific feedback, and schedule 1:1 coaching sessions. Built into the QA product.

**Intelligent triage from call content:**
Post-call transcripts are analyzed for entity detection, intent, language, and sentiment to automatically categorize and route tickets.

**What is not publicly documented:** CRM auto-fill directly from call transcript (writing back structured data fields to external CRM records). Zendesk's auto-fill is limited to ticket fields and internal notes.

Sources: [Announcing real-time AI suggestions for Voice with Copilot](https://support.zendesk.com/hc/en-us/articles/9752147521818-Announcing-real-time-AI-suggestions-for-Voice-with-Copilot), [Announcing voice AI agents (EAP)](https://support.zendesk.com/hc/en-us/articles/10231529954074-Announcing-voice-AI-agents-EAP), [Understanding Voice QA in Zendesk QA](https://support.zendesk.com/hc/en-us/articles/7043759312154-Understanding-Voice-QA-in-Zendesk-QA)

---

### Mobile App Calling

**Agents still cannot make or receive Zendesk Talk (phone) calls from the Zendesk Support native iOS or Android mobile app — confirmed as of March 2026.** This limitation has not changed. The Zendesk Support mobile app is designed for ticket management, messaging (WhatsApp, chat, email), and agent status control — but it does not support the Talk softphone (voice call) interface. Agents who need to handle inbound or outbound phone calls must use the desktop browser-based Agent Workspace.

Zendesk's own support documentation states explicitly: "The Support mobile app doesn't allow call functionality within the app."

The 2025 community thread on the Zendesk help forum requesting Talk mobile calling (originally posted in 2021) remains open and unresolved — Zendesk has not shipped this capability.

The only Talk-related function available in the mobile app is setting agent availability status (online/offline/away for Talk).

**2025 mobile app updates:** Side conversations (email-based) are now available in the mobile app. A "new agent experience" toggle activates Agent Workspace compatibility on mobile. These improve ticket-handling on mobile but do not add voice calling.

**Workarounds documented by Zendesk:** Agents can configure Talk to route calls to a personal or desk phone number via PSTN forwarding. Call audio rings on the agent's physical mobile phone, but call controls (accept, transfer, hold, record) remain in the desktop Agent Workspace — this is not a native mobile app calling experience.

**Talk SDK (customer-facing, not agent-facing):** Zendesk provides a Talk SDK for iOS and Android that developers can embed in customer-facing apps, allowing end-users to initiate calls to a Zendesk Talk digital line. This is for customer use, not for agents.

**WhatsApp calling:** Not applicable. WhatsApp voice calling is not supported by Zendesk at all (neither on desktop nor mobile), so there is no WhatsApp-specific mobile calling capability.

Sources: [About the Zendesk Support mobile app](https://support.zendesk.com/hc/en-us/articles/4408846407066-About-the-Zendesk-Support-mobile-app), [Zendesk Talk Mobile App community thread](https://support.zendesk.com/hc/en-us/community/posts/4409222561562-Zendesk-Talk-Mobile-App), [How do I take calls on a personal or desk phone?](https://support.zendesk.com/hc/en-us/articles/4408821101338-How-do-I-take-calls-on-a-personal-or-desk-phone), [Talk SDK for iOS](https://developer.zendesk.com/documentation/classic-web-widget-sdks/talk-sdk/ios/introduction/)

---

### Wati Comparison Note

Zendesk has a materially more mature call recording and GenAI-on-voice stack than Wati for traditional phone calls: automatic recording available on all Suite plans, AI transcription in 35 languages (with speaker labeling, keyword boosting, and PII redaction), generative call summaries post-GA, real-time Copilot suggestions during calls, autonomous Voice AI Agents (EAP, English-only), and AI-powered QA scoring across 100% of voice interactions. However, all of this applies exclusively to Zendesk Talk (phone/VoIP) — none of it touches WhatsApp voice calls, which Zendesk does not support at all.

Wati's structural advantage: its entire voice stack (calling, recording, AI) operates natively over WhatsApp, which is the channel Zendesk cannot serve for voice. Additionally, Zendesk's mobile app still does not support agent calling from a phone (confirmed unchanged as of March 2026), while Wati's WhatsApp-based calling aligns naturally with how agents in WhatsApp-first markets already operate. Zendesk's Voice AI (phone) is English-only; Wati's Astra supports 30+ languages on WhatsApp.
