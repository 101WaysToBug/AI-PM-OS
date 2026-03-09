# Wati Competitive Landscape Matrix
Synthesized from 6 agent research reports — March 9, 2026
Sources: respond-io.md · infobip.md · twilio.md · zendesk.md · aisensy.md · interakt.md



## Feature Comparison Matrix

| Feature | Respond.io | Infobip | Twilio | Zendesk | AiSensy | Interakt | Wati |
|---|---|---|---|---|---|---|---|
| **Pricing model** | $79–$279/mo flat | Custom enterprise | Usage-based (no flat plan) | $55–$169/agent/mo | $45–$85/mo flat | $12–$63/mo flat | Tiered flat + per-min calls |
| **WhatsApp Calling (native)** | ✅ GA | ✅ GA (Jul 2025) | ✅ GA (dev API only) | ❌ None | ❌ Not shipped | ✅ GA (Advanced+ plans) | ✅ GA (all paid plans) |
| **Calling on all paid plans** | ⚠️ Growth+ ($159) | ❌ Enterprise only | ❌ Dev setup required | ❌ N/A | ❌ N/A | ⚠️ Advanced+ ($63) only | ✅ Differentiator |
| **Call recording** | ✅ Auto + manual | ✅ Auto (account-level) | ✅ Dev-configured only | ✅ Talk/phone only | ❌ Not documented | ✅ Free included | ⚠️ Opportunity |
| **AI transcription** | ✅ With timestamps | ✅ Real-time + post-call | ✅ $0.035/min | ✅ 35 languages (phone only) | ❌ Not documented | ✅ Free included | ⚠️ Opportunity |
| **AI call summaries** | ✅ Action items | ✅ On-demand in UI | ✅ $0.005/min/operator | ✅ Auto post-call (phone only) | ❌ Not documented | ✅ Free included | ⚠️ Opportunity |
| **Voice AI (WhatsApp-native)** | ✅ Jan 2026 (ElevenLabs) | ❌ No WhatsApp-native AI voice | ❌ Dev API only | ❌ Phone only, EAP | ⚠️ Early-stage bot only | ❌ Telephony IVR only | ✅ Differentiator (Astra) |
| **No-code Voice AI builder** | ⚠️ Advanced plan only | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ Differentiator |
| **Mobile app calling** | ✅ iOS & Android | ✅ iOS, Android, Huawei | ❌ App discontinued | ❌ No calling on mobile | ❌ Not on mobile | ❓ Not confirmed | ⚠️ Opportunity |
| **Missed call workflows** | ✅ Automated triggers | ❌ Not documented | ❌ Dev-configured | ❌ N/A | ❌ | ❌ Not documented | ✅ |
| **Call CTA buttons in templates** | ✅ | ✅ (1 per template) | ✅ Dev-configured | ❌ | ❌ | ❌ Not documented | ✅ |
| **Business hours call control** | ✅ Via Meta Biz Suite | ✅ | ✅ Via Meta console | ❌ N/A | ❌ | ❌ Not documented | ✅ |
| **Agent performance analytics** | ✅ | ✅ | ✅ Dev-configured | ✅ Talk only | ❌ | ✅ | ✅ |
| **30+ language Voice AI** | ✅ 32 languages | ✅ 100+ (phone/API) | ⚠️ 11 languages | ⚠️ English only (EAP) | ❌ | ⚠️ 22 Indian languages | ✅ Differentiator |
| **Multi-channel AI (Web+WA+Voice)** | ⚠️ WA + voice only | ❌ Separate products | ❌ Build it yourself | ❌ | ❌ | ❌ | ✅ Differentiator |
| **SMB-friendly onboarding** | ⚠️ Complex pricing | ❌ Enterprise sales only | ❌ Dev-first | ❌ Complex | ✅ Self-serve | ✅ Self-serve | ✅ |
| **Verified business badge on calls** | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ |
| **Threat level** | 🔴 HIGH | 🟡 MEDIUM | 🟡 MEDIUM | 🟡 MEDIUM | 🟡 MEDIUM | 🟠 MEDIUM-HIGH | — |



## Pricing Comparison

| Competitor | Entry Plan | Mid Plan | Enterprise | WhatsApp Calling Access |
|---|---|---|---|---|
| **Respond.io** | $79/mo (Starter, no calling AI) | $159/mo (Growth, human calling) | Custom | $279/mo for Voice AI on calls |
| **Infobip** | Custom only | Custom only | Custom | Enterprise contract required |
| **Twilio** | Usage-based (no flat plan) | Usage-based | Usage-based | Dev API + per-min usage charges |
| **Zendesk** | $55/agent/mo | $115/agent/mo | $169+/agent/mo | No WhatsApp calling at any tier |
| **AiSensy** | $45/mo | ~$85/mo | Custom | Not available at any tier |
| **Interakt** | $12/mo (no calling) | $49/mo (no calling) | Custom | $63/mo (Advanced plan) |
| **Wati** | Growth (calling included) | Pro (calling included) | Business (calling included) | Included on all 3 paid plans |

**Insight:** Wati is the only platform that includes WhatsApp Business Calling across all paid tiers without requiring an enterprise contract or a developer. Respond.io gates Voice AI to $279/month. Infobip requires a sales-led enterprise deal. This is Wati's clearest pricing moat in the SMB segment.



## Universal Weaknesses Across All Competitors

These gaps appear across every competitor — representing unmet market needs:

- **No WhatsApp-native Voice AI on calls** — Only Respond.io (Jan 2026) and Wati (Astra) have shipped this. Every other competitor's "Voice AI" runs on telephony/IVR, not inside WhatsApp calls.
- **Calling gated to expensive plans** — Every competitor that has calling either requires enterprise pricing (Infobip), developer resources (Twilio), or their highest-priced SMB tier (Respond.io $279, Interakt $63). Wati includes it from Growth upward.
- **No mobile calling** — Twilio discontinued its mobile app. Zendesk has no calling on mobile. AiSensy calling is web-only. Respond.io and Infobip support mobile calling but are the exception.
- **Recording & GenAI on calls = paid add-on everywhere** — Twilio charges $0.035/min for transcription. Zendesk requires the $50/agent Advanced AI add-on. Interakt bundles it free, which is a notable threat to this narrative.
- **Developer dependency** — Twilio requires engineering for every calling feature. This blocks the SMB buyer entirely.



## Wati's Strategic Positioning

**Core positioning: "The only WhatsApp platform where SMBs can call, record, and deploy a Voice AI agent — all from a single no-code dashboard."**

| Positioning Angle | Why It Works |
|---|---|
| Calling on all plans | Every competitor gates calling to expensive tiers or requires enterprise deals |
| WhatsApp-native Voice AI | Respond.io is the only peer — and charges $279/mo; Astra is Wati's clear differentiator |
| No-code for non-technical teams | Twilio requires developers; Infobip requires enterprise contracts; Wati is self-serve |
| Unified calling + messaging + AI | No competitor delivers all three natively in one WhatsApp-first SMB product |
| Global SMB reach | Infobip/Zendesk serve enterprises; Twilio serves developers; Wati serves SMBs at scale |



## Top Opportunities to Exploit

### 🥇 #1 — Own "WhatsApp-native Voice AI" before Respond.io captures the narrative
Respond.io launched Voice AI Agents in January 2026 (ElevenLabs-powered, 32 languages). They are marketing this aggressively. Wati's Astra was built for this — but marketing must move fast to establish Wati as the definitive WhatsApp Voice AI platform before Respond.io's narrative hardens in the market.

### 🥈 #2 — Win on "calling included in every plan" vs. competitors who gate it
AiSensy hasn't shipped calling. Interakt gates it to $63/month. Respond.io gates Voice AI to $279/month. Wati's SMB-accessible pricing for WhatsApp Calling is a genuine moat — make this explicit in sales materials and landing pages.

### 🥉 #3 — Ship call recording + AI transcription + summaries to close the Interakt gap
Interakt bundles recording, AI transcripts, and AI summaries for free with their calling plan. This is a credible competitive move. If Wati doesn't offer this natively, Interakt will use it as a sales wedge, especially in the Indian D2C market. This should be a near-term roadmap priority.

### 4️⃣ #4 — Win mobile calling before anyone else nails it
Twilio killed its mobile app. Zendesk has no mobile calling. AiSensy calling is web-only. Interakt mobile calling is unconfirmed. Respond.io and Infobip do support mobile — but Respond.io is expensive and Infobip is enterprise-only. A polished mobile calling experience for SMB agents is wide open.



## Immediate Product Priorities (Validated by Competitive Research)

| Priority | Feature | Competitive Rationale |
|---|---|---|
| 🔴 Ship now | Call recording | Interakt bundles it free — Wati needs parity; this is becoming table stakes |
| 🔴 Ship now | AI transcription on calls | Same as above; Respond.io, Infobip, Twilio, Zendesk, and Interakt all have this |
| 🔴 Ship now | AI call summaries | Every major competitor has post-call AI summaries; Wati gap is visible |
| 🔴 Q1 | Mobile app calling | Twilio app discontinued, Zendesk has none — first-mover advantage in SMB |
| 🟡 Q1–Q2 | Voice AI marketing push | Respond.io is marketing Voice AI Agents aggressively since Jan 2026 — Wati must counter |
| 🟡 Q2 | Expand Astra outbound AI voice | Respond.io has no documented outbound AI voice — Wati Astra's differentiation to protect |
| 🟡 Q2 | Sentiment analysis on calls | Infobip, Zendesk QA, and Twilio all offer this — growing expectation for voice AI platforms |



## Competitive Threat Summary

| Competitor | Threat Level | Primary Threat Vector | Key Wati Advantage |
|---|---|---|---|
| **Respond.io** | 🔴 HIGH | Voice AI Agents launched Jan 2026; full calling + GenAI stack; mobile calling | Wati is cheaper for SMBs; Astra has outbound AI voice Respond.io doesn't |
| **Interakt** | 🟠 MEDIUM-HIGH | Free recording/transcription/summaries bundled; Reliance Jio distribution in India | Wati calling on all plans; deeper calling feature set; better support SLA |
| **Infobip** | 🟡 MEDIUM | Enterprise-grade calling + recording + mobile; 195 countries | Wati is SMB-friendly and self-serve; Infobip is enterprise-only |
| **Twilio** | 🟡 MEDIUM | Deep GenAI on calls (Conversational Intelligence); developer ecosystem | Wati is no-code; Twilio requires developers; app discontinued |
| **Zendesk** | 🟡 MEDIUM | Enterprise brand + AI investment; upmarket push opening SMB gap | No WhatsApp Calling at all; mobile calling absent; too expensive for SMBs |
| **AiSensy** | 🟡 MEDIUM | Price leader ($45/mo); 100K+ customers; India SMB distribution | No WhatsApp Calling shipped (8 months after Meta GA); no recording/GenAI on calls |



---
*Research powered by 6 parallel agents using live web search — March 9, 2026*
*Individual reports: respond-io.md · infobip.md · twilio.md · zendesk.md · aisensy.md · interakt.md*
