---
title: "Findymail"
type: entity
entity_kind: tool
tags: [tool, enrichment, email-finding]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-linkedin-outbound-playbook]
---

# Findymail

An email enrichment provider used as the first pass in [[SalesCaptain]]'s enrichment waterfall. Positioned as the cheapest-per-credit option, covering approximately 50–60% of prospects. Subsequent passes fill in gaps.

## Role in This Wiki

Represents the "cheapest-first" principle of [[Enrichment Waterfall]] design: start with the most cost-effective provider, cascade to more expensive ones only for contacts the first provider couldn't find.

## Coverage Stats (SalesCaptain)

| Pass | Provider | Coverage |
|------|---------|---------|
| 1st | Findymail or Prospeo | ~50–60% |
| 2nd | LeadMagic or FullEnrich | fills gaps |
| 3rd | Hunter or Apollo | final gaps |
| Validate | ZeroBounce | clean before send |

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — primary source
- [[Enrichment Waterfall]] — the concept this tool implements
- [[Apollo]] — 3rd-pass enrichment provider in the same waterfall
