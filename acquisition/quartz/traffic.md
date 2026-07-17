# Search traffic

Captured: **2026-07-17**

Market: **Google US-English, desktop**

DataForSEO values are modeled estimates, not Quartz analytics. Quartz launched
only one month before this capture, so the snapshot mostly measures early
indexing.

## Domain snapshot

`dataforseo_labs/google/domain_rank_overview/live` returned:

| Metric | Result |
| --- | ---: |
| Ranked organic keywords | 3 |
| Modeled organic ETV | 1.008 |
| Positions 21–30 | 1 |
| Positions 51–60 | 1 |
| Positions 61–70 | 1 |
| Paid keywords | 0 |
| Paid ETV | 0 |

## Ranked keywords

| Keyword | US volume | Organic group rank | Absolute rank | Landing page | Modeled ETV | Relevance |
| --- | ---: | ---: | ---: | --- | ---: | --- |
| `quartz newsletter` | 390 | 30 | 33 | Homepage | 0.819 | Ambiguous; likely Quartz media/newsletter intent |
| `quartz ai` | 50 | 51 | 60 | Homepage | 0.105 | Ambiguous name plus AI |
| `quartz chatbot` | 40 | 63 | 67 | Homepage | 0.084 | Wrong category; Quartz does not present as a chatbot |

The dataset does not show a meaningful non-brand email-client query. The
largest modeled contribution, `quartz newsletter`, is likely contaminated by
the unrelated Quartz publication.

## Live top-10 checks

| Query | Quartz result on 2026-07-17 | Narrow conclusion |
| --- | --- | --- |
| `quartz mail` | Organic group rank 1, absolute rank 2 after an AI overview; also cited by the overview | Quartz captures a precise brand query despite name ambiguity |
| `quartz email client` | Organic and absolute rank 1 | Quartz captures explicit product-aware demand |
| `local AI email client` | Absent from the returned organic top 10 | No top-10 visibility for this exact non-brand category wording |
| `private AI email client` | DataForSEO returned an internal search-engine error | Unverified; no conclusion |

The live brand checks are more current than the Labs ranked-keyword index.
Their presence does not contradict the weak modeled footprint: exact brand
capture can exist before a domain develops category visibility or material
estimated traffic.

## Landing pages

`dataforseo_labs/google/relevant_pages/live` found only:

| Landing page | Ranked keywords | Modeled ETV |
| --- | ---: | ---: |
| `https://quartzmail.ai/` | 3 | 1.008 |

The live sitemap contains only the homepage, privacy, terms, and contact pages.
There is no observable category-page, comparison-page, integration-page, or
editorial program on the Quartz domain.

## Verdict

Observed with high confidence for the captured date:

- Quartz captures `quartz mail` and `quartz email client`.
- Its modeled domain footprint is three weak, ambiguous keywords.
- The homepage is the only ranked page in the snapshot.
- The exact category query `local AI email client` did not return Quartz in the
  top 10.
- No paid keywords appeared in the Labs snapshot.

Unknown:

- Actual search visits or downloads.
- Search performance outside Google US-English.
- Whether the one-month-old domain will gain category visibility later.
- Whether the makers intentionally deprioritized SEO in favor of launch and
  owned-network distribution.
- Historical or current advertising outside the Labs paid-keyword snapshot.

For Tecotype, Quartz supports preserving a descriptive category/platform title
and building only a small number of claim-specific pages. It does not support a
broad content program, and it does not show that “local AI” is itself a
discoverable category.

Request provenance and task identifiers are in [requests.md](./requests.md).
