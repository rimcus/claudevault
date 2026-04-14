---
title: "Fibbler"
type: entity
entity_kind: tool
tags: [tool, linkedin, ads, signals]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-linkedin-outbound-playbook]
---

# Fibbler

A LinkedIn ad engager tracking tool. Detects prospects who engaged with your LinkedIn ads but never clicked through — people in the consideration phase who showed interest without converting.

## Role in This Wiki

Triggers Workflow 01 in [[SalesCaptain]]'s 7 LinkedIn workflows: someone sees your LinkedIn ad, engages (likes, comments, or views past a threshold), but never clicks. Fibbler surfaces these engaged non-converters for follow-up outreach.

## Position in Stack

```
LinkedIn Ad → Fibbler (detect engagement, no click) → Clay → HeyReach/Lemlist
```

An alternative tool for this workflow is ZenABM.

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — primary source
- [[Signal Infrastructure]] — the broader concept
- [[Clay]] — downstream enrichment
