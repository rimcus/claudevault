---
title: "PDL (People Data Labs)"
type: entity
entity_kind: tool
tags: [tool, data-provider, enrichment, b2b-data, firmographics, contacts]
created: 2026-06-24
updated: 2026-06-24
sources: [codyschneider-tam-mapping]
---

# PDL (People Data Labs)

A large-scale B2B data provider offering firmographic and contact data at scale. Named in [[Cody Schneider]]'s TAM mapping waterfall stack (alongside [[LeadMagic]], [[Findymail]], and [[Prospeo]]) for resolving firmographics and contacts across a full TAM universe.

## Role in This Wiki

A data enrichment provider in the [[TAM Mapping]] and [[Enrichment Waterfall]] stacks. PDL is particularly suited for high-volume data pulls — building the initial enriched universe of thousands of accounts before tiering and qualification.

## Position in Stack

```
Universe pull (Crunchbase, BuiltWith, Apollo, scrapers)
    → PDL / LeadMagic / Findymail / Prospeo waterfall (enrich contacts + firmographics)
    → AI research (soft qualifier extraction)
    → Tiering
```

## See Also

- [[TAM Mapping]] — the primary use case; building the enriched account universe
- [[Enrichment Waterfall]] — the contact enrichment pattern
- [[entities/leadmagic]] — co-listed enrichment provider
- [[entities/prospeo]] — co-listed enrichment provider
- [[entities/findymail]] — co-listed enrichment provider
- [[sources/codyschneider-tam-mapping]] — primary source
