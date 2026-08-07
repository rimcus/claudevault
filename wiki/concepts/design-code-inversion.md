---
title: "Design/Code Source-of-Truth Inversion"
type: concept
tags: [design, figma, ai-coding, product-design, design-systems]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Design/Code Source-of-Truth Inversion

*Code has become the source of truth ahead of design files, not the other way around — inverting roughly a decade of standard practice and pushing the designer's role downstream in the production line.*

## Overview

Observed by [[entities/maxime-champoux|Maxime Champoux]] at [[entities/well|Well]] as a direct consequence of the team's AI-coding velocity increase (see [[concepts/ai-native-engineering-team]]). For roughly the last ten years, the standard workflow put Figma upstream: a designer specifies the intended experience in Figma, engineers build code to match it, and the next iteration starts again from an updated Figma file. Once code can be produced and iterated on faster than a human can update a design file to track it, that relationship breaks down.

## Key Properties / Characteristics

- Figma-as-source-of-truth assumed a slower code-production cadence than design iteration; that assumption no longer holds at Well's shipping velocity.
- Code is now the source of truth; Figma has become what Champoux calls a "slave" artifact — descriptive of what was built, not prescriptive of what to build.
- The designer's position in the production sequence moved from upstream (defining the spec before engineering starts) to downstream (polishing what engineering already shipped).

## How It Works

Where a designer previously produced the up-front visual spec for a feature, they now receive a functionally complete but raw ("brute") feature from engineering, and their job is to reconcile it with the existing design system, ensure UI components are properly created/reused rather than duplicated, and polish the overall UX — closer to a quality-and-consistency pass than an original-spec role. This mirrors the same "black-box briefing, downstream polish" pattern described in [[concepts/roadmap-abstraction-shift]] for the product-manager role: both roles are moving from defining-the-what-in-advance toward refining-the-what-after-the-fact, as the actual construction step (code) becomes near-instant.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | Well's design workflow has inverted: code leads, Figma follows | high (direct, first-person practitioner claim, consistent with the rest of the source's velocity narrative) |

## Contradictions & Open Questions

- No detail on whether Figma is maintained at all going forward (e.g., regenerated periodically from code, or effectively abandoned) — the source states the team "can't keep up" maintaining it but doesn't describe a replacement documentation/handoff artifact for design intent beyond the design-system component library itself.
- Open question: does this inversion generalize to companies with larger, cross-functional design orgs (where Figma also serves stakeholder communication, not just engineering handoff), or is it specific to a small, highly-integrated team like Well's 12 people?

## See Also

- [[concepts/ai-native-engineering-team]] — the velocity shift that caused this inversion
- [[concepts/roadmap-abstraction-shift]] — the parallel shift in the product manager's role (spec-writer → concept-definer + downstream reviewer)
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
