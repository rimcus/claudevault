---
title: "HeyReach"
type: entity
entity_kind: tool
tags: [tool, linkedin, outreach, automation]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-linkedin-outbound-playbook]
---

# HeyReach

A LinkedIn outreach automation platform designed for agency-scale usage. Distinguishing feature: flat-fee pricing with unlimited LinkedIn profiles — avoids the per-seat cost model that makes other tools expensive at scale.

## Role in This Wiki

The outreach execution layer for [[SalesCaptain]]'s 7 LinkedIn workflows. Appears in 5 of the 7 workflows as the sending tool, typically receiving enriched leads from [[Clay]] after signal detection and qualification.

## Position in Stack

```
Signal (Trigify / Fibbler / LinkedIn) → Clay (enrich, qualify) → HeyReach (send)
```

## Comparison

- vs. [[Lemlist]]: both handle LinkedIn outreach; Lemlist adds email + WhatsApp as additional channels
- vs. Instantly: Instantly is cold email; HeyReach is LinkedIn-native

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — primary source
- [[Lemlist]] — alternative/complement for multichannel sequences
- [[Clay]] — upstream enrichment layer
- [[Signal Infrastructure]] — what feeds HeyReach
