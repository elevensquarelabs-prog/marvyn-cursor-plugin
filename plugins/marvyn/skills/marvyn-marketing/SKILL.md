---
name: marvyn-marketing
description: Build and manage the user's ad campaigns (Meta, Google, Reddit) and answer questions about their marketing results using the Marvyn tools. Use when the user wants to launch, change, pause or resume ads, or asks how their ads, campaigns, traffic, SEO or conversions are doing.
---

# Marvyn marketing

## When to use

- "Launch a campaign for…", "Pause the ads that are wasting money", "Turn that campaign back on"
- "How are my ads doing?", "Why did traffic drop?", "What should I fix first?"
- Checking tracking before shipping a landing page or a pixel change

## Building a campaign

1. Read the account first with the facts tool for the platform (`campaign_facts`, `google_campaign_facts`, `reddit_campaign_facts`): ad accounts, pages, pixels, audiences.
2. Use `campaign_search` for interests, locations and languages. Never invent ids.
3. Save the campaign with the draft tool (`campaign_draft`, `google_campaign_draft`, `reddit_campaign_draft`). Only use budgets, locations and audiences the user actually gave; leave anything else for them to fill in.
4. Tell the user the campaign is ready to review and that it goes live when they approve it in Marvyn. Never say it is live.

## Changing ads

- Use `propose_pause` / `propose_resume` for campaigns or ads, and `propose_recommendations` for Marvyn's suggested fixes. Each saves a card the user approves in Marvyn.

## Reading results

1. Start with `get_marketing_summary`; use `get_campaign_performance`, `get_creative_performance`, `get_search_visibility`, `get_conversion_funnel` or `get_tracking_health` when the question names an area.
2. Check `get_marvyn_alerts` when the user asks what is wrong or what changed.
3. Quote numbers with their period and source exactly as returned. Do not estimate missing figures.
4. If a tool says an account is not connected or needs reconnecting, tell the user to fix it in Marvyn under Integrations.
