# CALL-ANALYTICS: Usage Tracking & Analytics for Call Recording, Transcription & Summarization

**Type:** Epic
**Priority:** High
**Product Area:** WhatsApp Business Calling
**Owner:** PM - WhatsApp Business Calling & Voice AI
**Labels:** `analytics`, `calling`, `recording`, `transcription`, `summarization`, `instrumentation`
**Plan:** Pro, Business, Enterprise

---

## Summary

Instrument end-to-end usage tracking for the Call Recording, Transcription, and Summarization features so that the PM team can monitor adoption, engagement, and feature success across all customer segments.

## Why This Matters

We are launching three high-value capabilities (Recording, Transcription, Summarization) that directly impact customer retention and upsell potential on Business/Enterprise plans. Without proper tracking, we cannot:
- Measure feature adoption rates post-launch
- Identify friction points (e.g., users enabling then disabling features)
- Validate whether these features reduce churn and drive plan upgrades
- Make data-driven decisions on the roadmap for Voice AI

---

## Success Metrics (KPIs to Track)

### Segmentation Dimensions

All metrics below must support slicing by these dimensions:
- **Plan Type**:   Pro / Business / Enterprise
- **ACV Band** 
- **Region**: India, ROW, etc
- **Timestamp**: Daily, weekly, monthly roll-ups
- Industry: Healthcare, Financial Services etc. 

### Adoption Metrics
| Metric | Definition |
| --- | --- |
| **Recording Activation Rate** | % of eligible accounts (Pro/Business/Enterprise) that have recording enabled where eligible is the subs that have already enabled calling |
| **Transcription Activation Rate** | % of accounts with transcription enabled |
| **Summarization Activation Rate** | % of accounts with summarization enabled |
| **Feature Toggle Churn** | % of accounts that enable then disable a feature within 7 days |

### Volume & Usage Metrics (Absolute Counts)
| Metric | Definition |
| --- | --- |
| **Accounts with Recording ON** | Total active accounts that currently have call recording enabled |
| **Accounts with Transcription ON** | Total active accounts that currently have transcription enabled |
| **Accounts with Summarization ON** | Total active accounts that currently have summarization enabled |
| **Total Recording Minutes** | Cumulative minutes of call recordings produced |
| **Avg. Recording Minutes per Account** | Total recording minutes / # of accounts with recording ON |
| **Total Transcriptions Generated** | Count of successfully generated transcriptions |
| **Total Summarizations Generated** | Count of successfully generated AI summaries |
| **Transcription-to-Recording Ratio** | Total transcriptions generated / Total recordings completed |
| **Summarization-to-Recording Ratio** | Total summaries generated / Total recordings completed |
| **Recording Minutes per ACV Band, Industry and Plan type** | Total recording minutes grouped by customer ACV band, Industry and Plan Type |
| **Power Users (Top 10%)** | Accounts in the top 10th percentile by recording minutes |

### Engagement Metrics
| Metric | Definition |
| --- | --- |
| **Calls Recorded / Total Calls** | % of calls that produce a recording (among enabled accounts) |
| **Pause/Stop Usage Rate** | % of recorded calls where an agent manually paused or stopped recording |
| **Transcription View Rate** | % of call logs where the transcript was opened/viewed |
| **Summary View Rate** | % of call logs where the AI summary was opened/viewed |
| **Recording Playback Rate** | % of recordings played back at least once |

---

## Events to Instrument

### Feature Configuration Events

| Event Name | Trigger |
| --- | --- |
| `call_recording.enabled` | Admin toggles recording ON for a number |
| `call_recording.disabled` | Admin toggles recording OFF |
| `call_transcription.enabled` | Admin toggles transcription ON (note: auto-fires when summarization is enabled) |
| `call_transcription.disabled` | Admin toggles transcription OFF |
| `call_summarization.enabled` | Admin toggles summarization ON |
| `call_summarization.disabled` | Admin toggles summarization OFF |

### Recording Lifecycle Events

| Event Name | Trigger |
| --- | --- |
| `call_recording.started` | Recording begins automatically on call connect |
| `call_recording.paused` | Agent clicks "Pause" button |
| `call_recording.resumed` | Agent clicks "Resume" after pause |
| `call_recording.stopped` | Agent clicks "Stop" button manually |
| `call_recording.completed` | Recording finishes (call ends or manual stop) |
| `call_recording.failed` | Recording fails to save or process |

### Transcription & Summarization Events

| Event Name | Trigger |
| --- | --- |
| `call_transcription.generated` | Transcription completes processing |
| `call_transcription.failed` | Transcription processing fails |
| `call_summary.generated` | AI summary completes processing |
| `call_summary.failed` | Summarization processing fails |
---
