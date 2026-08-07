---
title: "Roadmap Abstraction Shift (Concept-Level PM in an AI-Coding World)"
type: concept
tags: [product-management, roadmap, double-diamond, ai-coding, spec-writing]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Roadmap Abstraction Shift

*Once a "4–6 week" engineering scope can be executed in about 2 hours, detailed feature specs stop making sense — product work moves back up one level of abstraction, from spec-writing to concept-level vision plus black-box feature briefs.*

## Overview

Documented by [[entities/maxime-champoux|Maxime Champoux]] at [[entities/well|Well]] as the direct product-management consequence of the team's AI-coding velocity increase (see [[concepts/ai-native-engineering-team]]). With shipping velocity scaling into the hundreds of features/month and a single person (Champoux) doing all product definition, product work itself became the bottleneck — forcing a rethink of the classic Double Diamond framework rather than just working the same process faster.

## Key Properties / Characteristics

- The old Double Diamond: diverge/converge to a concept, then diverge/converge again with engineering into a 4–6-week feasibility-scoped spec — with scope deliberately cut to fit that 4–6-week time-box.
- Once the 4–6-week scope executes in ~2 hours, the artificial scope-cutting step has no remaining purpose.
- Response: move back one level of abstraction — work from concept/vision (6–12 month horizon), not detailed specs.
- The engineer, not the PM, now produces the (more technical) implementation plan, typically in 1–3 days, against a "brute"/raw version of the product.
- Product briefs are deliberately black-box: inputs, outputs, and desired experience are specified; internal implementation ("how") is explicitly delegated.
- The concept-diverging research phase (competitor analysis, pattern identification, market intelligence) is now itself heavily automated.

## How It Works

**Feature briefing as a black box.** Champoux describes his own briefing style directly: for a given feature, he defines the desired inputs, the desired outputs, and the desired experience — and deliberately does not specify the internal "how," delegating that entirely to the engineer and their agents (who, per [[concepts/agent-specialization-context-window]], have the codebase-level context to make good implementation decisions that a PM-level brief shouldn't need to dictate).

**Automating the research phase.** What used to be roughly two weeks of manual concept-diverging work — competitor analysis, identifying which patterns exist in the market and in Well's own codebase (to reason about how a new pattern should be assimilated, not just bolted on), and light market/pricing intelligence — is now run as a chain of automated skills taking about one hour, at what Champoux describes as *better* quality than the old manual process, not merely faster.

**Deliverable format evolution.** Wireframes moved from low-fidelity ASCII sketches to high-fidelity HTML wireframes rendered live using Well's actual Storybook design-system components (built from real UI building blocks, not approximations), specified in a Gherkin/BDD-style Given-When-Then format — effectively a TDD-style spec for precisely identifying dependencies and edge cases in a feature that hasn't been built yet, handed to engineering in place of a traditional written spec.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | Concept-diverging research (competitor analysis, pattern ID, market intel) dropped from ~2 weeks to ~1 hour, at improved quality | medium (specific practitioner claim; "quality improved" is subjectively assessed by the same person making the claim) |
| [[sources/maximechampoux-well-ai-native-engineering]] | Engineers now produce their own implementation plan (1–3 days) from a concept-level brief, rather than executing a pre-cut PM spec | high (direct, specific process description) |

## Contradictions & Open Questions

- This shift assumes engineers (augmented by specialized agents) can reliably fill the gap left by detailed specs — no discussion of what happens when an engineer's own implementation plan misreads the concept-level intent, or how/whether that gets caught before shipping.
- Open question: does the black-box briefing style scale to a multi-PM organization, or does it depend on the tight, single-PM, 12-person context Well currently operates in? The source only describes it at that scale.

## See Also

- [[concepts/ai-native-engineering-team]] — the velocity shift that forced this abstraction change
- [[concepts/design-code-inversion]] — the parallel shift in the designer's role (also moving downstream, from spec to polish)
- [[concepts/agent-specialization-context-window]] — why engineers can be trusted with implementation-level decisions the PM no longer specifies
- [[concepts/product-engineers-no-pms]] — the ElevenLabs source's more extreme version of the same underlying trend (no PM function at all)
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
