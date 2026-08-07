---
title: "1% Marginal Gains (Applied to AI-Coding Tooling)"
type: concept
tags: [productivity, tooling, continuous-improvement, ai-coding]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# 1% Marginal Gains (Applied to AI-Coding Tooling)

*A daily discipline of shipping small (~1%) improvements to the team's AI-coding tooling, shared immediately with the whole team, compounding into a large aggregate velocity gain.*

## Overview

[[entities/maxime-champoux|Maxime Champoux]] at [[entities/well|Well]] explicitly borrows this from cycling — Dave Brailsford's marginal-gains methodology at British Cycling/Team Sky, which improved sleep, nutrition, and equipment by small increments each, compounding into outsized aggregate athletic performance. Applied here to the team's Claude Code/agent tooling stack rather than physical performance.

## Key Properties / Characteristics

- Explicit daily target: find a ~1% improvement to the tooling, not a big redesign.
- Improvements take the form of small automations or reusable "skills."
- Distribution mechanism: shared with the whole team immediately via pull request, the moment anyone believes a change produces even a marginal gain — not batched or held back.
- The gains compound: individually small, but stacked daily across a team, they produced a measurable jump in shipped-features-per-month.

## How It Works

From January onward, Well ran this as a standing team rule rather than a one-off initiative. Anyone who noticed a way to shave friction off the coding/agent workflow — a small automation, a new reusable skill — built it and opened a PR immediately, on the logic that even a ~1% individual improvement is worth propagating to the whole team right away rather than waiting to batch bigger changes. Champoux credits this discipline specifically for the climb from the initial post-adoption 2x jump (November→December) up to the 40s-features/month range by February — i.e., it's the mechanism that kept compounding gains after the one-time "everyone starts coding" jump had already happened (see [[concepts/ai-native-engineering-team]]).

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | Daily 1%-improvement discipline, starting in January, drove velocity from ~14 to the 40s features/month by February | medium (specific figures given, but the causal link between this specific practice and the velocity numbers is the founder's own attribution, not independently isolated from other concurrent changes) |

## Contradictions & Open Questions

- No mechanism described for preventing tooling sprawl or duplicate/conflicting "1% improvements" as the number of accumulated skills grows — worth flagging as a plausible failure mode at larger team scale, though not observed or discussed in-source.
- Open question: is this discipline distinct in practice from the later, more structured "named specialized agents" system in [[concepts/agent-specialization-context-window]], or did the marginal-gains skills eventually get folded into that more formal structure? The source implies a progression (informal marginal gains → later formal agent specialization) but doesn't describe the transition explicitly.

## See Also

- [[concepts/ai-native-engineering-team]] — the velocity narrative this practice fits inside
- [[concepts/agent-specialization-context-window]] — the more structured system this informal practice appears to have fed into
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
