---
title: "LinkedIn InMail Pipeline"
type: concept
tags: [linkedin, inmail, outbound, list-building, enrichment, signal, cold-outreach]
created: 2026-07-09
updated: 2026-07-09
sources: [nickabraham-linkedin-inmail-pipeline]
---

# LinkedIn InMail Pipeline

The infrastructure and list-qualification system required to send LinkedIn InMails at scale without triggering LinkedIn's credit freeze. Documented by [[Nick Abraham]] from 250,000+ InMails/month across 15+ concurrent campaigns.

## Why InMail Requires a Different Pipeline

Cold email and LinkedIn InMail share the same ICP + copy logic, but InMail has a hard constraint cold email doesn't: a finite, non-replenishable credit pool that, if depleted, shuts down *all* sending — including the free tier.

- **50 paid InMail credits** per [[Sales Navigator]] license per month
- **400–800 free sends** to Open Profiles per month
- **Credit freeze cascade:** paid credits hit zero → LinkedIn freezes everything, including free sends

3–5 non-open profiles per day is enough to drain the paid balance in a week. Standard cold email has no equivalent failure mode — deliverability problems are gradual. InMail failures are sudden and complete.

## The 5-Step Pipeline

```
GetLeads (raw list)
    → NetNut (open-profile enrichment + split)
        Open bucket → Apify (active user filter)
            → AI agent (ICP qualification)
                → Sequencer (open queue only)
        Non-open bucket → (hold or email channel)
```

### Step 1 — Pull Raw List

Tool: [[GetLeads]]. Only one field required: the LinkedIn profile URL. Email, phone, and company domain are not needed to run the InMail pipeline.

### Step 2 — Enrich for Open-Profile Status

Tool: [[NetNut]] API. Flags which contacts have Open Profile enabled. Output: two lists — open profiles (free to message) and non-open (paid credit required).

**This is the non-negotiable gate.** Teams that skip segmentation and load a mixed list into a sequencer burn through paid credits silently, then wake up frozen.

### Step 3 — Filter for Active Users

Tool: [[Apify]]. Identifies contacts who posted or commented on LinkedIn in the last 30–60 days. Active users respond at significantly higher rates across every outbound channel. Apply to the open-profile bucket before qualification.

### Step 4 — Validate ICP Fit

Tool: AI qualification agent. Confirms industry, profile, and role against the ICP definition. Sends are finite — each one must go to a well-qualified contact. ICP validation and credit conservation are the same decision.

### Step 5 — Segment Before Loading Sequencer

Open profiles into the InMail sequence. Non-open profiles into a separate channel (cold email, LinkedIn connection request, or hold). Never mix in a single sequence.

## Open-Profile Density by List Source

| Source | Open-Profile Rate |
|--------|------------------|
| Standard lead database | 5–8% |
| Sales Navigator scrape | 30–40% |

Sales Navigator sorts Open Profiles toward the front of search results — a Sales Nav list naturally skews toward people who can receive free InMails. This is one of the operational reasons to prefer Sales Nav for InMail campaigns specifically.

## The Send-Time Sequencer Requirement

Open-profile status is not permanent. A contact enriched as "open" today may flip to "closed" before the sequencer sends. A sequencer that doesn't recheck open-profile status at send time burns a paid credit on every stale profile.

**Sequencer selection for InMail must include this capability.** It is a functional requirement, not a preference.

## Relation to TAM Mapping and Signal Infrastructure

The ICP qualification step (Step 4) is the [[TAM Mapping]] principle at list level: define ICP in machine-sortable variables, apply them before any send, never work an unqualified list.

The active-user filter (Step 3) is a behavioral [[Signal Infrastructure]] layer applied inside the send list: LinkedIn activity in the last 30–60 days is a signal of prospect engagement and receptivity. The same logic that drives [[Trigify]] (detecting LinkedIn engagement as a buy signal) applies here at the list-hygiene level.

## See Also

- [[sources/nickabraham-linkedin-inmail-pipeline|Nick Abraham — LinkedIn InMail List Pipeline]] — primary source
- [[entities/nick-abraham|Nick Abraham]] — author; 250K+ InMails/month
- [[entities/getleads|GetLeads]] — list building (Step 1)
- [[entities/netnut|NetNut]] — open-profile enrichment (Step 2)
- [[entities/apify|Apify]] — active user filter (Step 3)
- [[concepts/tam-mapping|TAM Mapping]] — ICP-in-variables principle applied to list qualification
- [[concepts/signal-infrastructure|Signal Infrastructure]] — LinkedIn activity as behavioral signal
- [[concepts/enrichment-waterfall|Enrichment Waterfall]] — email-focused enrichment; InMail pipeline is the LinkedIn analog
- [[entities/sales-navigator|Sales Navigator]] — higher open-profile density than standard databases
