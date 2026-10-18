---
name: marvyn-marketing
description: Use the Marvyn tools for anything about the user's own marketing - ads, SEO, AI search visibility, Shopify store, Google Analytics, social, site behaviour, tracking - whether reading results, investigating a change, or preparing a campaign, article, audience, pause or tracking change for approval.
---

# Marvyn marketing

## When to use

- Results: "How are my ads doing?", "What did the store sell last week?", "Which pages lost traffic?"
- Why: "Why did sales drop?", "Why is CPA up?" - use `analyse_marketing_data`, it compares every source at once
- SEO and AI search: queries, rankings, indexing, competitors, backlinks, AI visibility
- Doing: launch or change campaigns, build audiences, pause or resume ads, draft an SEO article, switch on conversion sending

## Reading

1. For a broad or "why" question, call `get_marvyn_context` first (dates, connected sources, readable subjects), then start with `analyse_marketing_data` or `get_intelligence_snapshot` (`describe_marketing_metrics` explains a subject's metrics and splits). For a named area use the matching tool: `get_ads_intelligence`, `get_store_intelligence`, `get_seo_overview`, `get_seo_competitors`, `get_ai_visibility`, `get_gsc_index_coverage`, `get_gsc_sitemap_health`, `get_gsc_branded_split`, `get_ga4_property_context`, `landing_pages`, `tracking_status`.
2. Use `query_marketing_data` for exact figures the summaries do not show (orders, products, queries, pages, social posts, Clarity, pixel). Call `list_marketing_tables` first, then copy table ids and metric names exactly from it.
3. For a methodology question (audit, creative testing, CRO, attribution), find a playbook with `search_skills` and read it with `load_skill`.
4. Quote numbers with their period and source exactly as returned. Do not estimate missing figures. If a source is not connected or not on the user's plan, say so in one sentence.

## Doing

1. Read first: `campaign_facts` / `google_campaign_facts` / `reddit_campaign_facts` for accounts, pages, pixels and audiences; `campaign_search` for interests, locations and languages. Never invent ids.
2. Prepare the change with the matching tool: `campaign_draft`, `google_campaign_draft`, `reddit_campaign_draft`, `campaign_create_audience`, `propose_pause`, `propose_resume`, `propose_recommendations`, `prepare_conversion_sending`, `save_content_draft`.
3. Only use budgets, locations, web addresses and launch intent the user actually gave, and put them on the draft with provenance "assumption"; never invent values.
4. Each tool saves a card and returns its id and link. To approve in the chat: call `review_marvyn_change` with the card id, show the user EVERYTHING it returns (budget total, audience, every ad's text and links, whether it goes live, the values you filled in), and ask. Only after a clear yes, call `approve_marvyn_change` with the code. Otherwise give them the link to approve in Marvyn.
5. Never approve on your own initiative, and never say a change is live before `approve_marvyn_change` succeeds. Switching a campaign back on is approved in Marvyn, not in chat.
