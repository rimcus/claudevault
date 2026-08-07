---
title: "AI-Native Engineering Team (Everyone Codes)"
type: concept
tags: [ai-coding, engineering-culture, org-design, claude-code, velocity]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# AI-Native Engineering Team (Everyone Codes)

*A 12-person team went from ~7 shipped features/month to 100+/month over roughly 6 months by moving the entire team — including designers, brand designers, and the CEO — onto direct AI-coding tools, under two explicit conditions: bounded permissions and full team buy-in.*

## Overview

Documented by [[entities/maxime-champoux|Maxime Champoux]] at [[entities/well|Well]], dated specifically from November 2025 (associated with the release of Claude Opus 4.5), which he frames as the point where coding shifted from "AI-augmented engineer" (still meaningfully bottlenecked by human-typed code) to a world where **intent is what gets coded**. This is the most granular, dated, month-by-month account of an AI-coding velocity transition currently in this wiki.

## Key Properties / Characteristics

- Not an engineering-only initiative — designers, a brand designer, and the founder himself started directly using Claude Code.
- Velocity roughly doubled in month one (Nov→Dec 2025: ~7 → ~14 features/month), then compounded through marginal-gains tooling work (see [[concepts/marginal-gains-1-percent]]) into the 40s/month by February.
- Hit an explicit plateau at 40–50 features/month through March–April, later broken via agent specialization (see [[concepts/agent-specialization-context-window]]).
- Reached 100+ features/month by the recording date, with the same 12-person headcount throughout.

## How It Works

**Two non-negotiable conditions**, per Champoux, for "everyone codes" to actually work rather than degrade quality:
1. **Bounded permissions, expressed as skills.** Non-engineers are explicitly barred from touching backend or system architecture — they can touch frontend only, and only under the relevant domain owner's validation.
2. **Full commitment, not a partial pilot.** The month-one doubling only happened because the entire team moved to "100%" at once — Champoux frames this as a change-management problem as much as a technical one.

**Where the freed capacity went.** With non-engineers able to handle small UI/UX improvements and routine bug-fixing directly, engineers were freed from the "improvement + bug-run" tail that normally follows a 4–6-week feature build, letting them chain into the next feature build sooner — this reallocation, not raw new capability, is what Champoux credits for the initial capacity doubling.

**Corroborating ratio data.** A parallel Qonto-era data point: PM-to-engineer ratio there was roughly 1:8 in the pre-AI, headcount-driven world. A secondhand anecdote from an OpenAI podcast guest heard as "Romain" (possibly Romain Huet [low confidence]) reports his own ratio shifting from 1:6 to 1:2 using Codex, with speculation it could eventually invert entirely (more PMs needed than engineers) — directionally consistent with Champoux's own experience, though from a different company and tool.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | Well went from 7 to 14 features/month in the first month of full-team Claude Code adoption | high (specific, dated, first-person account) |
| [[sources/maximechampoux-well-ai-native-engineering]] | Well reached 100+ features/month with the same 12-person team by the recording date | high (specific, first-person, though not independently audited) |
| [[sources/maximechampoux-well-ai-native-engineering]] | A PM:engineer ratio could eventually invert (more PMs than engineers) as AI coding capability increases | low (secondhand anecdote relayed from another podcast, unverifiable from this transcript alone) |

## Contradictions & Open Questions

- The initial 2x velocity gain is attributed largely to redistributing bug-fix/polish work to non-engineers, not to raw agent capability — worth distinguishing from the later, much larger jump to 100+/month, which Champoux attributes to the agent-specialization fix in [[concepts/agent-specialization-context-window]] instead.
- No headcount growth is reported across the entire 7→100+ features/month arc — worth treating this as an unusually clean natural experiment (fixed team size, measured output) relative to most public AI-coding-productivity claims, which typically don't control for headcount changes.

## See Also

- [[concepts/marginal-gains-1-percent]] — the tooling-improvement discipline that compounded month-one gains further
- [[concepts/agent-specialization-context-window]] — the fix for the plateau this team hit at 40–50 features/month
- [[concepts/design-code-inversion]] — how the designer's role changed once code, not Figma, became the source of truth
- [[concepts/product-engineers-no-pms]] — parallel concept from the ElevenLabs source: PM work compressing into engineering as AI coding capability rises
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
