---
title: "ZeroBounce"
type: entity
entity_kind: tool
tags: [tool, enrichment, email-validation]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-linkedin-outbound-playbook]
---

# ZeroBounce

An email validation service. Used as the final step in [[SalesCaptain]]'s enrichment waterfall to clean the list before sending — removes invalid, catch-all, and risky addresses that would hurt deliverability.

## Role in This Wiki

Represents the validation layer in [[Enrichment Waterfall]] design. Enrichment finds emails; validation removes the ones that would bounce or damage sender reputation. Both steps are necessary.

## Position in Stack

```
1st pass (Findymail) → 2nd pass (FullEnrich) → 3rd pass (Apollo) → ZeroBounce (validate) → Outreach
```

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — primary source
- [[Enrichment Waterfall]] — the waterfall this tool finalizes
- [[Findymail]] — upstream enrichment provider
