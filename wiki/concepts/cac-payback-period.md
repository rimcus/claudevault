---
title: "CAC-to-Payback-Period"
type: concept
tags: [cac, unit-economics, metrics, north-star, saas]
created: 2026-07-15
updated: 2026-07-15
sources: [lukeharries-elevenlabs-growth-playbook]
---

# CAC-to-Payback-Period

*Using months-to-recoup-CAC, set per product line, as the operating ratio for growth spend decisions — instead of CAC-to-LTV.*

## Overview

[[entities/luke-harries|Luke Harries]] argues CAC:LTV is the wrong day-to-day steering metric because LTV is retroactive and unstable: CAC itself swings quickly, and in a multi-product/horizontal company LTV can expand unpredictably as a customer who entered on one product later adopts others (consumer → creator → enterprise, in [[entities/elevenlabs|ElevenLabs]]' case). CAC-to-payback-period is proposed as the more decision-useful ratio because it's forward-looking, per-channel, and directly actionable.

## Key Properties / Characteristics

- Payback-period targets are set *per product line*, not company-wide, because risk tolerance and contract structure differ by product.
- Each channel/product has an owner responsible for tracking this ratio and deciding pacing.
- The ratio is used as a **binary gas-pedal signal**, not a dial to fine-tune: above target → maximize speed; below target → treat as a deliberate, boundaried bet.
- Distinguishes *individual-channel* CAC trend (tends to rise as an audience saturates) from *blended company* CAC trend (can hold flat or fall as new channels, better conversion, and cheaper entry products are added).

## How It Works

1. **Set a payback-period target per product**: roughly 12 months for lighter/self-serve products, ~24 months as a typical default, up to 36 months for large multi-year enterprise contracts where retention confidence is high.
2. **If a channel is beating its target ratio**, the instruction isn't incremental (e.g. "raise spend 20%/week") — it's to grow as fast as possible while the window holds. A favorable ratio is treated as explicit permission to prioritize speed over caution.
3. **If a channel is below target**, that's acceptable *only* as a conscious bet — e.g., deliberately losing money on a new product for its first two years because the underlying thesis is believed in, not as an unexamined default.
4. **Track blended CAC separately from channel CAC.** Individual channels do tend to get more expensive over time (audience saturation, drift to a less-defined ICP at the margin) — but a company can keep blended CAC flat or falling by adding new channels, improving activation/conversion, and layering in a cheap consumer entry point that later upsells into pricier tiers.

## North Star for Enterprise Specifically

For the enterprise marketing motion, the tracked North Star is **marketing-sourced SQLs**: a lead identified by marketing (webinar signup, product signup, etc.) who has booked a call with an SDR, and been confirmed qualified by that SDR. Organic and enterprise channels are deliberately evaluated with *fuzzy, longer-horizon attribution* rather than single-channel ROI — e.g., comparing the relative lift in leads for a geo running a coordinated multi-channel push (billboards, podcasts, newsletters, on-the-ground events) against a comparable control geo, rather than crediting any one channel in isolation.

## Consumer/Prosumer Retention Nuance

Enterprise NRR is clean to read (account-level seat expansion, e.g. 150% NRR on a Slack-style land-and-expand deal even if some individual seats churn). Consumer/prosumer retention commonly looks *worse* at the individual-user level (Harries cites ~87% as an acceptable range) — but he argues the real picture is better than that number implies, because natural product virality (a user builds something on a tool, shares it, pulls in referrals) means the effective cohort/account-level NRR, once organic growth is counted, can exceed the raw per-seat figure. The mistake is judging consumer products by enterprise-style seat-retention math.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/lukeharries-elevenlabs-growth-playbook]] | ElevenLabs sets payback-period targets between 12 and 36 months depending on product/contract type | high (specific, practitioner-stated operating policy) |
| [[sources/lukeharries-elevenlabs-growth-playbook]] | Blended CAC can stay flat even as individual channel CAC rises, given new-channel addition + conversion improvement + cheap entry products | medium (directionally argued, no blended-CAC time series shown) |

## Contradictions & Open Questions

- No numeric example of an actual payback-period calculation (inputs, CAC, gross margin assumptions) is given — the framework is stated at the policy level, not the spreadsheet level.
- Tension with this wiki's paid-ads sources (Schneider's $1-in-$5-CLV-out framework): both use forward-looking unit economics, but Schneider's model assumes PMF and immediate paid scaling, while Harries explicitly gates any paid spend behind achieved PMF (see the "paid too early" mistake in [[sources/lukeharries-elevenlabs-growth-playbook]]). Not a direct contradiction, but a sequencing difference worth flagging for anyone applying both sources together.

## See Also

- [[concepts/gtm-agents]] — this wiki's existing paid-ads tactical spec ($1-in-$5-CLV-out), useful contrast on sequencing
- [[concepts/growth-hiring-order]] — hiring only follows once a channel/product shows a workable ratio
- [[sources/lukeharries-elevenlabs-growth-playbook]] — primary source
