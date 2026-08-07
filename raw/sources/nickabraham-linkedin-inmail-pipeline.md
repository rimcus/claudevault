---
title: "Nick Abraham on X: \"We send 250,000+ LinkedIn InMails a month.If we get the list wrong, we burn through paid credits in days and LinkedIn freezes all our sending.This is the 4-step list pipeline that protects the whole operation: https://t.co/2sE16S5XDx\""
source: "https://x.com/NickAbraham12/status/2074915461750284796"
author:
published: 2026-07-08
created: 2026-07-09
description:
tags:
  - "clippings"
---
## Post

## Conversation[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

We send 250,000+ LinkedIn InMails a month. If we get the list wrong, we burn through paid credits in days and LinkedIn freezes all our sending. This is the 4-step list pipeline that protects the whole operation:

[![Image](https://pbs.twimg.com/media/HMuUnbMW0AElvfs?format=jpg&name=small)](https://x.com/NickAbraham12/status/2074915461750284796/photo/1)

[View quotes](https://x.com/NickAbraham12/status/2074915461750284796/quotes)

Post your reply[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915466921816498)

LinkedIn gives you 50 paid InMail credits per Sales Navigator license per month. On top of that, you get 400-800 free sends to Open Profiles. But if your paid credits hit zero, LinkedIn freezes everything. Including the free ones.[1.1K](https://x.com/NickAbraham12/status/2074915466921816498/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915473439789559)

That one rule changes how you build every list. If a single non-open profile sneaks into your send queue, the sequencer burns a paid credit on it. Get 3-5 of those a day and within a week your paid balance is gone. So we built a pipeline to prevent it.[1.1K](https://x.com/NickAbraham12/status/2074915473439789559/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915476497412514)

Step 1: Pull the raw list. We use GetLeads to build the initial list. For InMail, you only need one field: the LinkedIn profile URL. You don't need email, phone, or company domain. Just the LinkedIn URL and you can run the whole system from there.[559](https://x.com/NickAbraham12/status/2074915476497412514/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915480293233081)

Step 2: Enrich for open-profile status. Run every LinkedIn URL through the NetNut API. It flags which contacts have Open Profile turned on so you know who you can message for free. Then split the list: open profiles in one bucket, non-open in another.[537](https://x.com/NickAbraham12/status/2074915480293233081/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915486085644479)

This segmentation step is not optional. If you dump everyone into a sequencer together and start sending, you will hit non-open profiles and burn paid credits. That's how people silently drain their balance and wake up frozen.[415](https://x.com/NickAbraham12/status/2074915486085644479/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915489332036011)

Step 3: Filter for active users. We use Apify to identify which contacts have posted or commented on LinkedIn in the last 30-60 days. Active users are far more likely to see and respond to your message. This gives campaigns a significant lift across every outbound channel.[381](https://x.com/NickAbraham12/status/2074915489332036011/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915493673148760)

Step 4: Validate ICP fit. Your total sends are capped, so every send needs to go to a great-fit prospect. We run an AI qualification agent across every contact to confirm industry, profile, and role. Credit conservation and quality at the same time.[339](https://x.com/NickAbraham12/status/2074915493673148760/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915496772632614)

One thing worth knowing: the source of your list changes your open-profile density. A standard lead database pull runs about 5-8% open profiles. A list scraped from Sales Navigator runs 30-40%. Sales Nav appears to sort open profiles toward the front of search results.[318](https://x.com/NickAbraham12/status/2074915496772632614/analytics)[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915499624792386)

Even after all this, there's still a trap. NetNut might flag a profile as open today, and the person flips it closed tomorrow. If your sequencer can't check open status at send time, it sends anyway and burns a paid credit. That's why sequencer choice matters for InMail.[Nick Abraham](https://x.com/NickAbraham12)[@NickAbraham12](https://x.com/NickAbraham12)

[19h](https://x.com/NickAbraham12/status/2074915502699192815)

The full pipeline: 1. Pull raw list (GetLeads) 2. Enrich for open-profile status (NetNut) 3. Filter for active users (Apify) 4. Validate ICP fit (AI agent) 5. Segment open vs. non-open before loading into sequencer Do all 5 before a single InMail goes out.