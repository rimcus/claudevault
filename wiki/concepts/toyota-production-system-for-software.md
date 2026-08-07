---
title: "Toyota Production System for Software"
type: concept
tags: [engineering-culture, quality, process, qonto, org-design]
created: 2026-07-22
updated: 2026-07-22
sources: [maximechampoux-well-ai-native-engineering]
---

# Toyota Production System for Software

*Treating software development as an assembly line — each contributor owns a specific task in a specific order, defects halt the line immediately, and root causes get fixed, not patched.*

## Overview

Documented by [[entities/maxime-champoux|Maxime Champoux]] as the internal engineering culture at [[entities/qonto|Qonto]] (internally nicknamed "the Qontoway"), explicitly modeled on the Toyota Production System (TPS) rather than invented from scratch. The analogy is deliberately literal: building a feature is treated like assembling a Toyota Yaris. Each station on the line — backend engineer setting the chassis, frontend engineer doing the bodywork — performs a specific task, in a specific order, and the product manager's role is to define the vehicle concept, specify each station's task, and keep the line accelerating without letting quality slip.

Champoux frames this as valuable independent of the current AI-coding shift — a durable culture-and-process concept, not a tool-specific tactic.

## Key Properties / Characteristics

- Software-as-assembly-line: fixed task order, one contributor per station, specified upstream by the PM.
- Zero-bugs-in-production as the explicit quality standard, not an aspiration.
- An Andon-cord-style stop-the-line mechanism for defects.
- Root-cause discipline: fix the specific bug, but also fix why the bug-class can recur.
- "Fix it now" — don't keep shipping around a known, unresolved defect.

## How It Works

**The Andon cord.** Borrowed directly from TPS jargon (Champoux uses the Japanese-inflected term "andon"): on the physical assembly line, a worker who spots a defect (e.g., a scratch in the bodywork) pulls a red cord. The line manager comes running, the entire assembly line halts immediately, and manager and worker investigate the defect together until they find and fix the root cause — only then does the line restart. Applied to software: any team member who spots a quality problem is expected to "pull the cord" — stop, investigate together, fix the root cause — rather than let production continue around an unresolved defect.

**Continuous improvement loop on every bug.** Each production bug triggers: (1) identify the root cause, not just the symptom; (2) fix the specific instance; (3) fix the underlying cause so the same bug-class can't recur. The standard is zero bugs in production, maintained through constant vigilance rather than periodic bug-bash cycles.

## Evidence & Examples

| Source | Claim | Confidence |
|--------|-------|------------|
| [[sources/maximechampoux-well-ai-native-engineering]] | Qonto's internal culture ("the Qontoway") is explicitly modeled on Toyota's assembly-line and Andon-cord practices | high (direct, detailed practitioner account) |
| [[sources/maximechampoux-well-ai-native-engineering]] | Zero-bugs-in-production is Qonto's stated quality standard | medium (stated as policy; no data on actual defect rates in-source) |

## Contradictions & Open Questions

- No detail on how the "stop the line" practice scales once a company has many parallel feature teams working on unrelated parts of the codebase simultaneously — the physical assembly-line metaphor assumes a single line.
- Open question: does this culture survive the AI-coding shift described in [[concepts/ai-native-engineering-team]] intact, or does it need to be re-expressed (e.g., the Andon cord becoming an automated CI gate) once the "workers" pulling the cord are partly AI agents rather than only humans?

## See Also

- [[concepts/ai-native-engineering-team]] — how this same practitioner rebuilt a much smaller team's velocity under AI coding, a different context than Qonto's human-scale assembly line
- [[concepts/agent-specialization-context-window]] — the AI-era analog of "each station owns a specific task": named, specialized agents instead of specialized humans
- [[entities/qonto]] — the company this culture was built at
- [[sources/maximechampoux-well-ai-native-engineering]] — primary source
