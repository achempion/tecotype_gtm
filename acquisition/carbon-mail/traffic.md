# Search traffic

Captured: **2026-07-17**

Market: **Google US-English, desktop**

DataForSEO values are modeled estimates, not Carbon Mail analytics. This is a
small current-domain snapshot. It does not reconstruct launch traffic or prove
that a returned result produced a visit, Gmail connection, or retained user.

## Domain snapshot

The three DataForSEO Labs calls returned no search-visibility items:

| Endpoint | Returned result |
| --- | ---: |
| `dataforseo_labs/google/domain_rank_overview/live` | 0 items |
| `dataforseo_labs/google/ranked_keywords/live` | 0 organic or paid keywords |
| `dataforseo_labs/google/relevant_pages/live` | 0 pages |

The empty Labs responses reported `items_count: 0` and `total_count: null`.
They therefore support “no returned items,” not a claim that Carbon Mail has
never ranked or received search traffic.

## Live top-10 checks

| Query | Carbon Mail result on 2026-07-17 | Narrow conclusion |
| --- | --- | --- |
| `carbon mail email client` | [Homepage](https://www.carbonmail.app/) at organic group rank 1, absolute rank 2; [login page](https://www.carbonmail.app/login) at organic group rank 9, absolute rank 11 | Carbon Mail captures an explicit product-aware brand query |
| `on-device AI email client` | Carbon's domain was absent; a [founder Reddit post](https://www.reddit.com/r/NoCodeSaaS/comments/1qoph6j/building_email_client_with_ondevice_ai_looking/) appeared at organic group rank 2, absolute rank 5 | Founder-created community content has category-query visibility that the domain does not |
| `privacy-first email client` | No Carbon domain or identified founder post in the returned organic results | No top-result visibility for this exact privacy wording on the captured date |

The branded result used the current homepage metadata:

> **Title:** Carbon Mail – Email Client with Local AI | Zero Tracking
>
> **Description:** Turn 200 emails into 12 that matter. Local AI filters noise
> in your browser. 100% private, zero tracking. Works with Gmail.

A direct public homepage request independently returned the same title and
description, with `https://www.carbonmail.app/` as the canonical URL.

The live brand result does not conflict with the empty Labs snapshot. A precise
brand query can resolve correctly before a small domain develops enough
category visibility to appear in the Labs dataset.

## Landing pages

Labs returned no relevant pages. The branded live SERP exposed only:

| Landing page | Live evidence |
| --- | --- |
| `https://www.carbonmail.app/` | First organic result for `carbon mail email client` |
| `https://www.carbonmail.app/login` | Ninth organic result for the same query |

No category, comparison, integration, or editorial page appeared in the
captured search data. This does not prove that such pages do not exist; it means
they were not visible in these calls.

## Community result

The ranking Reddit result is a founder-authored beta post. It describes Carbon
Mail as a privacy-first client using on-device AI and links to the homepage.
The author also says users liked demonstrations but returned to Gmail the next
morning, that the project was bootstrapped with `$0` spent, and that the team
was seeking growth advice without paid ads.

Public search found several near-identical posts in small startup communities,
including [r/microsaas](https://www.reddit.com/r/microsaas/comments/1qopfpp/building_email_client_with_ondevice_ai_looking/),
[r/startupideas](https://www.reddit.com/r/startupideas/comments/1qophwp/building_email_client_with_ondevice_ai_looking/),
and [r/indie_startups](https://www.reddit.com/r/indie_startups/comments/1qo61yr/building_email_client_with_ondevice_ai_looking/).
Visible engagement was in the low single digits. The search ranking proves
discoverability for one wording, not material referral traffic or acquisition.

## Verdict

Observed with high confidence for the captured date:

- Carbon Mail captures the explicit `carbon mail email client` query.
- Labs returned no organic keywords, paid keywords, or relevant pages.
- Carbon's domain did not appear for either tested non-brand positioning query.
- A founder Reddit post, rather than the product domain, ranked for
  `on-device AI email client`.
- The search-visible landing-page footprint returned by these calls is limited
  to the homepage and login route.

Unknown:

- Actual impressions, search visits, Gmail connections, activation, or
  retention.
- Search performance outside Google US-English desktop.
- Whether Labs will add the live branded ranking in a later index update.
- Whether other category wording exposes Carbon Mail.
- Whether community-post impressions or votes produced users.
- Whether SEO was intentionally deprioritized or is simply too early to
  measure.

For Tecotype, the narrow evidence supports testing an honest, demonstrable
community story that can also answer a specific search query. It does not
support duplicating one post across many communities or treating a ranking,
vote, or signup as activation. Any test should preserve source tags and measure
account connection, meaningful first-session use, and next-day return.

Request bodies, costs, task identifiers, and limitations are in
[requests.md](./requests.md).
