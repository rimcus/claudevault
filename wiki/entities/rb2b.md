---
title: "RB2B"
type: entity
entity_kind: tool
tags: [tool, website-visitors, deanonymization, signals]
created: 2026-04-14
updated: 2026-04-14
sources: [salescaptain-linkedin-outbound-playbook, alexvacca-gtm-engineering-hire]
---

# RB2B

A website visitor deanonymization tool that identifies LinkedIn profiles of people visiting your website — specifically useful for capturing traffic that originated from LinkedIn content. Converts anonymous site visits into known prospects with LinkedIn identity.

## Role in This Wiki

Appears in both [[Alex Vacca]]'s signal infrastructure framework and [[SalesCaptain]]'s capture system. Closes the loop between content (someone reads your LinkedIn post, clicks to your site) and outbound (you now know who that person is).

## Position in the Capture System

```
LinkedIn content → website visit → RB2B → identify LinkedIn profile → Clay → outreach
```

## See Also

- [[sources/salescaptain-linkedin-outbound-playbook]] — part of capture system
- [[sources/alexvacca-gtm-engineering-hire]] — mentioned as signal platform
- [[Signal Infrastructure]] — the concept this tool implements
- [[Trigify]] — complementary LinkedIn signal tool
- [[Teamfluence]] — complementary profile viewer tool
