---
title: "Facebook Ads Andromeda Update: The Best Thing to Happen to B2B SaaS in 5 Years"
type: source
tags: [facebook-ads, andromeda, b2b, algorithm, creative-targeting, signal-infrastructure, saas]
created: 2026-06-16
updated: 2026-06-16
sources: [codyschneider-andromeda-b2b-facebook]
author: "Cody Schneider"
source_url: "https://x.com/codyschneider/status/2066943969204797773"
source_type: x-post
---

# Facebook Ads Andromeda Update: The Best Thing to Happen to B2B SaaS in 5 Years

**Author:** [[Cody Schneider]] (@codyschneider)
**Published:** 2026-06-16
**Context:** Explains the theoretical foundation behind Schneider's entire Facebook ads approach. This post is the "why" beneath [[sources/codyschneider-paid-ads-playbook]] (broad targeting, 10 creatives/week), [[sources/codyschneider-fb-ads-ugc-playbook]] (creative volume, click→conversion), and [[sources/codyschneider-transcript-personas]] (persona definitions as the new moat). Written the same day as the other two June 16 posts.

---

## Core Thesis

Meta's Andromeda algorithm update killed audience-first targeting. The algorithm no longer starts from who you pick — it reads your creative and landing page, predicts who will convert based on behavioral signals, and finds them. For B2B SaaS, this is transformative: the thing B2B was always bad at (defining a small, high-intent niche audience) is now the algorithm's job. It does it better than you can.

> "meta went from 'can't reach b2b buyers' to 'the best buyer-finding engine on the internet' if your creative and tracking are tight"

---

## The Historical Context: Why B2B Abandoned Facebook

For a decade, Facebook was useless for B2B:
- **Interest-based targeting** — the old model — was garbage for B2B. You can't reliably target "CFO who is evaluating spend management software" by interests
- **Customer match lists** (personal emails) worked for ABM, but only if you could acquire personal emails — a persistent limitation
- **The result:** B2B buyers fled to LinkedIn, paying $200 CPMs for demographic precision that Facebook couldn't match

---

## What Andromeda Changed

The algorithm now operates differently:
1. **Reads your creative** — the ad itself becomes a signal about who the message is for
2. **Reads your landing page** — the destination reinforces the creative signal
3. **Predicts converters from behavioral data** — who has historically converted for similar signals
4. **Finds them** — the algorithm does the audience-finding

The marketer no longer specifies the audience. The creative specifies the audience implicitly.

---

## The Two Input Controls That Now Matter

Everything else is noise. The new game is:

### 1. Creative — It IS Your Targeting Now

> "the thing b2b was always bad at (defining a tiny, weird, high-intent audience) is now the algorithms job. it is better than you, give it unwavering faith"

- Different angle per buyer = different creative = different audience found by the algorithm
- One perfect ad doesn't scale — the algorithm can only find one audience with one creative
- **You need packs** — creative volume is how you reach multiple buyer personas simultaneously
- This is the theoretical basis for testing 10+ creatives/week: each one finds a different cohort of converters

### 2. Signal — Clean Pixel + Conversion API + Real Events

> "no garbage in, no garbage out"

- Pixel must be clean and firing correctly
- Conversion API must be set up (server-side, bypasses browser tracking limits)
- **Real conversion events only** — signup and payment, not proxy events like page views or scroll depth
- The algorithm learns from what you tell it to optimize for; bad signal data = it finds the wrong people

Community warning (from [[sources/codyschneider-fb-ads-ugc-playbook]]): misfiring pixels cause half of apparent "creative fatigue." This post explains why that's catastrophic — a misfiring pixel corrupts the signal the algorithm uses to find buyers.

---

## The Moat Shift

| Old moat | New moat |
|----------|----------|
| Media-buying tricks | Persona definitions |
| Audience targeting skills | Creative volume |
| LinkedIn budget | Data infrastructure (clean pixel + Conversion API) |

> "the moat moved from media-buying tricks to persona definitions, creative volume and data infra"

This directly explains why:
- **[[sources/codyschneider-transcript-personas]]** matters: persona definitions are now the primary competitive advantage
- **[[AI UGC Ads]]** scales: creative volume (100+ per cycle) reaches more buyer cohorts
- **[[Data Warehouse for AI]]** is non-negotiable: clean signal data is what the algorithm learns from
- **$200 LinkedIn CPMs are now optional**: Meta finds B2B buyers if your creative and tracking are right

---

## Why This Matters for B2B Specifically

B2B SaaS previously faced an inherent Facebook limitation: the buyers are too specific, too professional, too niche to reach with interest-based consumer targeting. Andromeda removes this constraint:

- **Narrow audience definition** → algorithm's job, not marketer's job
- **High intent signals** → conversion events (signup + payment) teach the algorithm what "high intent" looks like
- **ABM reach** → customer match lists become less critical; creative targeting finds the right people directly

The implication: B2B SaaS teams that abandoned Facebook for LinkedIn due to targeting quality should reconsider. The cost differential ($200 LinkedIn CPM vs. Facebook's lower CPMs) is now recoverable without sacrificing audience precision.

---

## Entities Mentioned

- [[Cody Schneider]] — author
- [[Graphed]] — promoted (implied)
- Meta / Facebook Ads — the platform; Andromeda is Meta's internal algorithm name

## Concepts Touched

- [[AI UGC Ads]] — creative IS targeting; packs over single perfect ads; Andromeda is the "why" behind creative volume
- [[Signal Infrastructure]] — clean pixel + Conversion API is the signal layer; same principle as the GTM signal layer
- [[Data Warehouse for AI]] — "no garbage in, no garbage out" applies to Facebook's algorithm as much as to GTM agents
- [[ICP Avatar]] — persona definitions are the new moat; transcript-based personas feed the creative that feeds the algorithm
- [[GTM Agents]] — the Facebook Ads agent now has a theoretical foundation (Andromeda) and two clear inputs to manage

## See Also

- [[sources/codyschneider-transcript-personas]] — persona definitions: the moat Andromeda creates
- [[sources/codyschneider-fb-ads-ugc-playbook]] — execution detail: creative packs, click→conversion, clean pixel warning
- [[sources/codyschneider-paid-ads-playbook]] — the structural overview; "target all of Facebook" is correct because Andromeda does audience-finding
- [[sources/codyschneider-ai-ugc-ads]] — the original 100+ variations pipeline; now theoretically grounded by Andromeda
- [[concepts/ai-ugc-ads]] — creative volume: the mechanism Andromeda rewards
- [[concepts/signal-infrastructure]] — the data infra layer that feeds Andromeda's learning
