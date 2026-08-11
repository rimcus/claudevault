---
title: "LeadMagic"
type: entity
entity_kind: tool
tags: [tool, enrichment, b2b-data, contacts, firmographics]
created: 2026-06-24
updated: 2026-08-11
sources: [codyschneider-tam-mapping, codyschneider-two-agents-podcast]
---

# LeadMagic

A B2B enrichment provider. Appears in [[Cody Schneider]]'s TAM mapping waterfall stack alongside [[Findymail]], [[Prospeo]], and [[PDL]] for resolving firmographics and contacts at scale. Also appears in [[SalesCaptain]]'s enrichment waterfall as a 2nd-pass provider (filling gaps after Findymail's initial ~50–60% coverage).

[[sources/codyschneider-two-agents-podcast]] (August 2026) names it in a narrower role: **mobile phone number enrichment specifically**, run alongside [[entities/origami|Origami]]'s aggregated waterfall rather than as a general firmographic pass.

## Role in This Wiki

The **2nd-pass enrichment provider** in the SalesCaptain waterfall, and one of four providers in Schneider's TAM enrichment stack. Used for both contact email resolution and firmographic data.

## Position in Stack

```
Findymail (1st pass, ~50-60%) → LeadMagic (2nd pass, fills gaps to ~70-80%) → Apollo (final gaps → 85%+) → ZeroBounce (validation)
```

## See Also

- [[Enrichment Waterfall]] — the waterfall concept; LeadMagic is 2nd-pass
- [[TAM Mapping]] — the broader process this feeds into
- [[entities/findymail]] — 1st-pass provider
- [[entities/prospeo]] — alternative enrichment provider in same stack
- [[entities/pdl]] — People Data Labs; another provider in Schneider's TAM stack
- [[sources/codyschneider-tam-mapping]] — primary source
- [[sources/codyschneider-two-agents-podcast]] — mobile-phone-specific enrichment role
- [[entities/origami|Origami]] — aggregated waterfall used alongside LeadMagic in the newer pipeline
