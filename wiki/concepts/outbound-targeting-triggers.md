---
title: "Outbound Targeting via Firmographics + Triggers"
type: concept
tags: [sdr, targeting, icp, personalization, outbound]
created: 2026-08-10
updated: 2026-08-10
sources: [outboundsquad-armandfarrokh-sdr-playbook]
---

# Outbound Targeting via Firmographics + Triggers

*Firmographic ICP fit alone produces false-positive targets; layering trigger events on top isolates the ~10-15% of an addressable list that's in a genuine buying window. Account-research skill is best taught in isolation ("shuttle runs"), and personalization at SMB volume runs through ranked trigger templates, not freeform copy.*

## Overview

[[entities/armand-farrokh|Armand Farrokh]]'s central diagnostic claim: the large majority of prospecting failures trace back to poor targeting (wrong accounts or wrong personas), not weak email copy or calling technique — and, separately, the highest-activity reps he's coached are never the top performers, because past a minimum-viable activity threshold, extra volume becomes junk that dilutes quality rather than adding pipeline. This concept bundles three related practices from his time at [[entities/carta|Carta]]: the firmographic-plus-trigger targeting model, a deliberate-practice method for teaching account research, and a template system for personalizing at scale without writing every email from scratch.

## Key Properties / Characteristics

- Firmographic fit (industry, size, stage) is necessary but not sufficient — a "stale" account can match every firmographic filter and still have nothing to buy right now.
- Trigger events (funding recency, growth rate, stage-linked compliance windows) are what separate a technically-matching account from a live buying-window account.
- Account-research skill is trained in isolation before being combined with the full outbound motion, rather than trained end-to-end from day one.
- Personalization at volume is achieved via a small library of trigger-ranked templates, not per-account freeform writing.

## How It Works

**The "stale cap table" example.** At Carta (selling cap-table/stock-option management software), an account could fit the firmographic ICP exactly — Series A-F, 50-500 employees — and still be a bad target if headcount is flat and there's been no funding in three years: no new option grants being issued, no compliance-audit pressure, nothing to actually sell into. The fix: require trigger events on top of firmographics before outreach — recency of the last funding round, double-digit employee growth rate, and company stage relative to when compliance audits typically start (Series C, in this context) — which together isolate roughly the 10-15% of the list genuinely in a live buying window.

**"Shuttle runs" for teaching account research.** Rather than having a new rep work 10 accounts fully end-to-end (compounding roughly 17 different mistakes — wrong account, wrong persona, wrong trigger, wrong personalization angle, weak opener — before any single one gets caught), the sub-skill is isolated first: "go find 5 accounts matching this criteria," reviewed together (these are good fits, these aren't, go find 2 more good ones), repeated until the rep can reliably self-identify good accounts — only then does training move to contacts, then email, then the call. A deliberate-practice method: isolate one skill, get it reliable, then combine.

**Ranked trigger templates ("First is Best").** Credited to Farrokh's 30MPC co-host, referred to in-transcript as "Mark Koslow" (likely Mark Kosoglow [medium-high confidence]): since hand-personalizing every SMB-volume email isn't feasible, rank possible triggers by strength (e.g., #1 = funded yesterday, #4 = growing 20-30%), pre-build one message template per ranked trigger, and at send time it takes about 10 seconds to identify the applicable trigger and drop in the matching template — connecting account-level and person-level signal to the message without writing from scratch each time.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/outboundsquad-armandfarrokh-sdr-playbook]] | The large majority of prospecting failures trace back to targeting, not copy or calling skill | medium (strong, repeated practitioner claim; no quantified breakdown given) |
| [[sources/outboundsquad-armandfarrokh-sdr-playbook]] | Trigger-plus-firmographic filtering isolates roughly 10-15% of an addressable list as genuinely buying-window accounts | low-medium (specific figure given for one company's context — Carta/cap-table software — not established as a general benchmark) |

## Contradictions & Open Questions

- The 10-15% figure is specific to Carta's cap-table product and trigger set; no claim is made (or should be assumed) that this percentage generalizes to other products/categories.
- Open question: how does this human-era, rep-applied trigger model relate to this wiki's AI-native [[concepts/signal-infrastructure]] concept, which automates similar trigger detection at much larger scale? They appear to be the same underlying idea at two very different levels of tooling maturity — worth treating as a before/after pair rather than competing approaches.

## See Also

- [[concepts/icp-avatar]] — the AI-copywriting-side parallel: generic ICP targeting produces generic outreach that amplifies into noise
- [[concepts/signal-infrastructure]] — the AI-native, automated-at-scale version of the same firmographic-plus-trigger logic
- [[concepts/cold-email-copywriting]] — parallel personalization-at-scale mechanic via ACV-based segmentation rather than trigger ranking
- [[sources/outboundsquad-armandfarrokh-sdr-playbook]] — primary source
