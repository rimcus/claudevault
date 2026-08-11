---
title: "Origami"
type: entity
entity_kind: tool
tags: [tool, enrichment, b2b-data, waterfall, aggregator]
created: 2026-08-11
updated: 2026-08-11
sources: [codyschneider-two-agents-podcast]
---

# Origami

An enrichment aggregator that sits in front of a full [[concepts/enrichment-waterfall|enrichment waterfall]] and exposes it behind a single API call.

## Role in This Wiki

Named by [[entities/cody-schneider|Cody Schneider]] in [[sources/codyschneider-two-agents-podcast]] as the way his cold-outbound agent handles enrichment: instead of manually chaining individual providers ([[entities/findymail|Findymail]] → [[entities/leadmagic|LeadMagic]] → [[entities/apollo|Apollo]], as in the SalesCaptain waterfall), the agent calls Origami once and Origami internally routes through the cheapest-to-most-expensive provider cascade.

## Pipeline Position

Prospect record → **Origami** (internally waterfalls across providers) → [[entities/leadmagic|LeadMagic]] (mobile-specific pass) → [[entities/millionverifier|MillionVerifier]] (validate) → [[entities/instantly|Instantly]] (send)

## See Also

- [[concepts/enrichment-waterfall]] — the pattern Origami aggregates
- [[sources/codyschneider-two-agents-podcast]] — primary source
- [[entities/leadmagic|LeadMagic]] — used alongside Origami for mobile enrichment specifically
- [[entities/millionverifier|MillionVerifier]] — downstream validation step
