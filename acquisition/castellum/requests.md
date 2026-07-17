# Castellum research request ledger

Requests were made on **2026-07-17**.

DataForSEO search requests used Google, United States (`2840`), English, and
desktop/Windows where device fields were applicable. Endpoint and credential
setup belongs in the central [DataForSEO documentation](../../tools/dataforseo.md).

No client binary, Ollama component, or AI model was requested. No client was
installed or launched. No account, mailbox authorization, form submission,
trial, checkout, or purchase was attempted.

## Credential and redaction boundary

The HTTP authorization header was:

```text
Authorization: Basic [configured credential redacted]
```

The credential was read from the configured system credential store. It was
not placed in a repository file, request body, report, or retained command
output.

Every posted body is reproduced exactly below. The bodies contained no secret,
so no body field required redaction. Standard `Content-Type:
application/json` was used.

## Cost summary

| Request group | Task IDs | Billed tasks | Cost (USD) |
| --- | ---: | ---: | ---: |
| Labs domain overview | 1 | 1 | 0.012120 |
| Labs ranked keywords | 1 | 1 | 0.012120 |
| Labs relevant pages | 1 | 1 | 0.012120 |
| Backlink summary | 1 | 1 | 0.024036 |
| Backlink detail | 1 | 1 | 0.024072 |
| Exact-domain Content Analysis | 1 | 1 | 0.024036 |
| Organic live SERPs | 10 | 7 | 0.016000 |
| Ads advertiser lookup | 1 | 1 | 0.002000 |
| Ads creative lookup | 1 | 1 | 0.002000 |
| **Total** | **18** | **15** | **0.128504** |

The total is below the **$0.25** cap.

Three live-SERP tasks were rejected at zero cost because four tasks were
mistakenly posted together to a live endpoint that accepts only one. The
queries were then posted separately. The first separate
`private AI email client Mac` task returned a billed provider-internal error,
so one corrective duplicate was posted and succeeded. Both billed attempts are
included in the total.

## Complete task ledger

| # | Request | Task ID | Task status | Cost | Extracted result |
| ---: | --- | --- | --- | ---: | --- |
| 1 | Ads advertisers: `castellum mail` | `07171734-2101-0139-0000-4868b3e6aa40` | `40102` No Search Results | 0.002000 | No advertisers returned |
| 2 | Ads creatives: domain | `07171734-2101-0139-0000-07df63f91428` | `40102` No Search Results | 0.002000 | No creatives returned |
| 3 | Backlink summary | `07171734-2101-0265-0000-be5c3ae0e89c` | `20000` Ok | 0.024036 | 2 backlinks / 2 referring domains |
| 4 | Backlink detail | `07171734-2101-0269-0000-65eea80a7d1e` | `20000` Ok | 0.024072 | 2 rows; both nofollow SEO spam |
| 5 | Exact-domain content | `07171734-2101-0463-0000-5decb37256b0` | `20000` Ok | 0.024036 | 0 items |
| 6 | Domain overview | `07171734-2101-0388-0000-840d9f98189e` | `20000` Ok | 0.012120 | 1 organic keyword; 0.672 ETV |
| 7 | Ranked keywords | `07171734-2101-0381-0000-100bdf0ca0ca` | `20000` Ok | 0.012120 | 1 row: `castellum ai` |
| 8 | Relevant pages | `07171734-2101-0385-0000-67dfcc63fbbf` | `20000` Ok | 0.012120 | Homepage only |
| 9 | SERP batch item 1: `castellum mail` | `07171734-2101-0139-0000-7ee797196799` | `20000` Ok | 0.002000 | Product absent from returned top 10 |
| 10 | SERP batch item 2: private AI | `07171734-2101-0139-0000-8bbd1bba060a` | `40000` Only one task allowed | 0 | No result |
| 11 | SERP batch item 3: keyboard-first | `07171734-2101-0139-0000-8d897d074da3` | `40000` Only one task allowed | 0 | No result |
| 12 | SERP batch item 4: managers | `07171734-2101-0139-0000-9d1dd339b8e1` | `40000` Only one task allowed | 0 | No result |
| 13 | Private-AI separate retry 1 | `07171735-2101-0139-0000-d2414eaad7c2` | `40101` Internal SE Server Error | 0.002000 | Billed; no result |
| 14 | Private-AI corrective duplicate | `07171736-2101-0139-0000-a0a6fd9fe19c` | `20000` Ok | 0.002000 | Product absent from returned top 10 |
| 15 | Keyboard-first separate retry | `07171735-2101-0139-0000-32a064e741ba` | `20000` Ok | 0.002000 | Product absent from returned top 10 |
| 16 | Managers separate retry | `07171736-2101-0139-0000-9193c919c48a` | `20000` Ok | 0.002000 | Product absent from returned top 10 |
| 17 | Validation SERP: `castellum ai` | `07171737-2101-0139-0000-185e7a1a7eed` | `20000` Ok | 0.004000 | Product absent from returned depth-40 organic set |
| 18 | Validation SERP: `castellum email client` | `07171737-2101-0139-0000-b8f3c4f59cf2` | `20000` Ok | 0.002000 | Product absent from returned top 10 |

Task statuses are provider task-envelope statuses. The two advertising tasks
were successfully billed envelopes whose inner task status was `40102`.
Likewise, task 13 was billed even though the provider returned no search
result because of its internal error.

## Exact DataForSEO bodies

### Domain overview

Endpoint:
`dataforseo_labs/google/domain_rank_overview/live`

```json
[{"target":"castellummail.com","location_code":2840,"language_code":"en","ignore_synonyms":true}]
```

### Ranked keywords

Endpoint:
`dataforseo_labs/google/ranked_keywords/live`

```json
[{"target":"castellummail.com","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

### Relevant pages

Endpoint:
`dataforseo_labs/google/relevant_pages/live`

```json
[{"target":"castellummail.com","location_code":2840,"language_code":"en","ignore_synonyms":true,"limit":50,"order_by":["metrics.organic.etv,desc"]}]
```

### Backlink summary

Endpoint: `backlinks/summary/live`

```json
[{"target":"castellummail.com","include_subdomains":true,"exclude_internal_backlinks":true}]
```

### Backlink detail

Endpoint: `backlinks/backlinks/live`

```json
[{"target":"castellummail.com","include_subdomains":true,"exclude_internal_backlinks":true,"mode":"one_per_domain","limit":200,"order_by":["rank,desc"]}]
```

### Content Analysis

Endpoint: `content_analysis/search/live`

```json
[{"keyword":"castellummail.com","search_mode":"as_is","limit":100}]
```

### Original malformed organic-SERP batch

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"castellum mail","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10},{"keyword":"private AI email client Mac","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10},{"keyword":"keyboard first email client Mac","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10},{"keyword":"email client for managers","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

The provider executed the first object and assigned zero-cost rejection task
IDs to the remaining three. The four IDs are tasks 9–12 in the ledger.

### Corrective organic SERP: private AI, first separate attempt

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"private AI email client Mac","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

This was task 13 and returned the billed `40101` internal error.

### Corrective organic SERP: private AI, duplicate

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"private AI email client Mac","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

This was task 14. It is intentionally duplicated in this ledger.

### Corrective organic SERP: keyboard-first

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"keyboard first email client Mac","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### Corrective organic SERP: managers

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"email client for managers","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### Validation organic SERP: `castellum ai`

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"castellum ai","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":40}]
```

### Validation organic SERP: `castellum email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[{"keyword":"castellum email client","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### Google Ads advertiser lookup

Endpoint: `serp/google/ads_advertisers/live/advanced`

```json
[{"keyword":"castellum mail","location_code":2840}]
```

### Google Ads creative lookup

Endpoint: `serp/google/ads_search/live/advanced`

```json
[{"target":"castellummail.com","location_code":2840,"platform":"all","format":"all","date_from":"2018-05-31","date_to":"2026-07-17","depth":40}]
```

## DataForSEO output record

At handoff, the raw provider envelopes remained in the ephemeral,
non-repository directory:

```text
/tmp/castellum-dataforseo/
```

It contains:

```text
ads-advertisers.json
ads-creatives.json
backlink-summary.json
backlinks.json
content-analysis.json
domain-overview.json
organic-serps.json
ranked-keywords.json
relevant-pages.json
serp-castellum-ai.json
serp-castellum-email-client.json
serp-keyboard-first.json
serp-managers.json
serp-private-ai-retry.json
serp-private-ai.json
```

Temporary storage is not durable evidence and is not part of this dossier.
The repository retains the exact posted bodies, all task IDs, task statuses,
costs, and the extracted metrics used in the report.

Extraction boundaries:

- the domain overview returned one domain result;
- ranked keywords returned its complete one-row set;
- relevant pages returned its complete one-page set;
- backlink detail returned both available one-per-domain rows;
- Content Analysis returned zero items;
- live SERPs are time-, location-, device-, and provider-method snapshots;
- advertising `No Search Results` is limited to the posted identity, market,
  platform/format range, and dates.

## Public site and metadata inspection

Public GET/HTML inspection covered:

- [homepage](https://castellummail.com/);
- [privacy](https://castellummail.com/privacy);
- [terms](https://castellummail.com/terms);
- [Google Limited Use](https://castellummail.com/google-limited-use);
- `https://castellummail.com/robots.txt`;
- `https://castellummail.com/sitemap.xml`.

The latter two returned the GitHub Pages 404 page. The homepage response and
rendered document were used to inspect:

- title, description, Open Graph, and Twitter metadata;
- canonical/robots/JSON-LD/`hreflang` absence;
- public links and visible source parameters;
- loaded scripts and recognizable analytics/advertising integrations;
- presence of a consent surface;
- CTA hierarchy and final asset destination.

A current desktop capture rendered at **1280 × 720 CSS pixels, device-pixel
ratio 2**. It did not follow or fetch the disk-image link.

No analytics or consent system observed in one response should be read as
proof that GitHub/CDN logs, conditional code, historical measurement, or
client-side telemetry do not exist.

## GitHub inspection

Unauthenticated public repository, API metadata, release pages, asset metadata,
commits, and workflow content were inspected for:

- [repository metadata](https://github.com/joanmarcriera/castellum-releases);
- [all releases](https://github.com/joanmarcriera/castellum-releases/releases);
- v0.1.0 through v0.2.2 release notes and asset counters;
- disk-image sizes and public SHA-256 metadata;
- update-manifest presence and counters;
- site/content commit history;
- the July 17 legal-page commit;
- public issue-triage workflow behavior;
- stars, forks, watchers, and open issues.

The direct `latest/download/Castellum-arm64.dmg` URL was identified from
public HTML but was deliberately not requested. Manifest presence and counters
were read from public release metadata. Public GitHub counters are dynamic and
were captured only once.

## Archive and public-search inspection

A Wayback CDX wildcard lookup for successful HTML captures of
`castellummail.com` returned:

```json
[]
```

That means no matching successful capture was returned by that request. It
does not prove that no crawl was ever attempted or that no deleted page
existed.

Narrow public searches covered the exact domain/product name with:

- Hacker News;
- Product Hunt;
- Reddit;
- LinkedIn posts;
- X;
- Bluesky;
- Mastodon;
- press/review terms;
- founder name/profile terms;
- partnership and affiliate terms.

The report records only results tied to this email product. Unrelated property,
defense, Latin-reference, and `castellum.ai` compliance results were excluded.
Search-engine and site indexing gaps prevent a universal negative conclusion.

Public founder-profile and Proton/Google documentation inspection did not
involve sign-in, messaging, following, form submission, or any account change.

## Prohibited actions and resulting limits

The following actions were deliberately not performed:

- request, download, mount, install, or launch the Castellum client;
- request Ollama or a model;
- verify the disk image’s local bytes, code signature, notarization ticket, or
  quarantine launch;
- create a Castellum, GitHub, Google, provider, or payment account;
- connect a Gmail or IMAP mailbox;
- submit an OAuth consent flow;
- open a support issue or transmit diagnostics;
- submit a contact, waitlist, newsletter, or feedback form;
- start a trial, invoke checkout, purchase, or test future licensing.

Therefore this dossier cannot validate installation, onboarding, provider
connection, feature operation, AI behavior, update behavior, activation,
retention, payment, or satisfaction. Those are explicitly unknown rather than
negative results.

## Reliability rules

- Provider search volume, rank, difficulty, CPC, ETV, and traffic value are
  estimates.
- The Labs `castellum ai` position and same-day live absence are preserved as
  method/timing variance, not averaged.
- An asset request is not a unique download, install, launch, or user.
- An update-manifest request is not retained use.
- A backlink is not a referral visit.
- Spam links are not qualified distribution.
- No indexed mention or ad is not proof of no historical/private activity.
- A release claim is not an independent signing, notarization, provider, or
  feature test.
- Public policy text is a first-party commitment, not an audit.
- Repository history shows changes, not motivation or conversion.
- No internal source, activation, retention, cost-of-acquisition, payment, or
  revenue analytics was available.
