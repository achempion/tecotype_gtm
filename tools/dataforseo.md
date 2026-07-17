# DataForSEO

## Credentials

`dataforseo-base64` is a macOS Keychain item containing the Base64-encoded DataForSEO `login:password` credential. Read it with:

```sh
security find-generic-password -s dataforseo-base64 -w
```

Send the returned value as the Basic authorization token. The credential was verified against DataForSEO’s user-data endpoint on 2026-07-17.

Do not copy the resolved credential into repository files, API request logs, saved shell commands, or competitor reports.

## Acquisition-research workflow

Use DataForSEO after the competitor’s landing page has produced specific channel hypotheses. See the [acquisition workflow](../acquisition/readme.md).

Start with one target market, such as Google US-English.

| Research question | Endpoint | Evidence |
| --- | --- | --- |
| Does the competitor have search visibility? | `dataforseo_labs/google/domain_rank_overview/live` | Estimated organic and paid traffic and ranking distribution |
| Which queries and landing pages perform? | `dataforseo_labs/google/ranked_keywords/live` | Keywords, positions, intent, volume, CPC, estimated traffic, and landing URLs |
| Which pages attract search visibility? | `dataforseo_labs/google/relevant_pages/live` | Landing pages aggregated by rankings and estimated traffic |
| Which sites link to the competitor? | `backlinks/summary/live` and `backlinks/backlinks/live` | Referring page and domain, anchor, target URL, and first and last seen dates |
| Where is the brand discussed? | `content_analysis/search/live` | Brand mentions in blogs, news, forums, and organization pages |
| Are important results still live? | `serp/google/organic/task_post` followed by `serp/google/organic/task_get/advanced`, or `serp/google/organic/live/advanced` | Current search results for promising queries |
| Has the competitor advertised? | `serp/google/ads_advertisers/live/advanced` followed by `serp/google/ads_search/live/advanced` | Advertiser identity, creatives, formats, and first and last shown dates |

### Recommended first pass

1. Run Domain Rank Overview for a directional domain snapshot.
2. Request organic and paid Ranked Keywords together, ignore close synonyms, and start with a limit of 250.
3. Use Relevant Pages to connect visibility to landing-page strategy.
4. Request up to 200 live backlinks with `mode: one_per_domain`, include subdomains, and exclude internal links.
5. Verify only the most promising discovered queries with current SERPs.
6. Use mentions, advertising, and trend endpoints only when the landing page or initial evidence creates a concrete hypothesis.

The Standard SERP queue is suitable when immediate results are unnecessary. Post the task, wait for readiness or a postback, and retrieve it with `task_get/advanced`. Use Live only when the result is needed immediately.

Do not collect every available metric. Prioritize results that connect a traffic source or referring site to a landing page, customer promise, and CTA.

## Pricing

Pricing snapshot recorded on **2026-07-17**. Verify the linked pricing pages before a new research batch because DataForSEO can change prices.

- [DataForSEO Labs](https://dataforseo.com/pricing/dataforseo-labs/dataforseo-google-api): $0.012 per task plus $0.00012 per returned item.
- [Backlinks](https://dataforseo.com/pricing/backlinks/backlinks) and [Content Analysis](https://dataforseo.com/pricing/content-analysis-api/content-analysis): $0.024 per request plus $0.000036 per returned row.
- [Google organic SERP](https://dataforseo.com/pricing/google-serp/google-organic-serp-api): $0.0006 per Standard top-10 page or $0.002 per Live top-10 page.
- [DataForSEO Trends](https://dataforseo.com/pricing/keywords-data/dataforseo-trends-api-pricing): $0.0012 per request for up to five keywords.

DataForSEO requires a $50 minimum account payment, while API usage is pay-as-you-go.

### Planning estimate

Budget **$0.25 per competitor**. A useful first pass in one market should usually cost approximately **$0.12–$0.20**, depending on returned rows and Standard versus Live SERPs.

| Call | Assumption | Maximum cost |
| --- | ---: | ---: |
| Domain Rank Overview | 1 item | $0.0121 |
| Ranked Keywords | 250 keywords | $0.0420 |
| Relevant Pages | 50 pages | $0.0180 |
| Backlinks Summary | 1 row | $0.0240 |
| Backlinks | 200 referring pages | $0.0312 |
| Content mentions | 100 citations | $0.0276 |
| Current SERP verification | 20 queries, top 10 results each, Standard | $0.0120 |
| Advertising checks | 2 Live requests | $0.0040 |
| Trends | 1 request | $0.0012 |
| **Total** | | **$0.1721** |

An emerging competitor may return fewer rows and cost less. Each additional search market should add approximately $0.08–$0.09.

Avoid historical Labs endpoints and clickstream data during the first pass. Historical endpoints have a higher base cost, while enabling clickstream data doubles the Labs request cost and may add little for an emerging competitor.

## Additional endpoints

After researching several competitors:

- Use `serp_competitors/live` to discover emerging competitors from category queries.
- Use `domain_intersection/live` to find queries shared by several emerging competitors.
- Use `related_keywords/live`, `keyword_ideas/live`, and `keyword_overview/live` to turn observed queries into experiments and prioritize them by demand, intent, CPC, and difficulty.
- Use `content_analysis/phrase_trends/live` and `backlinks/history/live` to identify launch or coverage spikes.
- Use DataForSEO Trends to compare brand and category interest.
- Use App Data API when a competitor distributes through the App Store or Google Play.

## Evidence boundary

DataForSEO exposes potential acquisition channels, not actual attribution:

- Search traffic is modeled rather than competitor analytics.
- A backlink does not prove referral clicks.
- A mention does not prove that it produced a signup.
- Ads archive absence does not prove that advertising never ran.
- Trend scores are relative rather than search volumes.

Offer, message, CTA, signup, onboarding, activation, payment, retention, and source-level conversion must be inspected or measured elsewhere.
