# Search traffic

Captured: **2026-07-17**

Market: **Google US-English, desktop Windows**

DataForSEO values are third-party search observations or estimates, not
ZenMail analytics. The domain appears early in its public life, and live SERP
results can update before DataForSEO Labs.

## Labs snapshot

The three Labs endpoints returned no result rows:

| Endpoint | Observed result |
| --- | --- |
| Domain Rank Overview | `items: 0`; no domain metrics |
| Ranked Keywords | `items: 0`; no keyword rows |
| Relevant Pages | `items: 0`; no landing-page rows |

This does **not** mean the domain has no Google visibility. A live SERP check
in the same pass found the homepage for a precise product-aware query.

## Live query checks

| Query | ZenMail result | Narrow conclusion |
| --- | --- | --- |
| `zenmail email client` | Homepage organic group rank 3, absolute rank 4 | Captures some product-aware demand despite brand ambiguity |
| `gmail client for mac` | Absent from returned organic top 10 | No top-10 visibility for the exact category query |
| `gmail keyboard shortcuts mac` | Absent from returned organic top 10 | The matching guide did not capture this exact high-intent guide query |
| `mimestream vs zenmail` | Absent from returned organic top 10 | The dedicated comparison page did not capture the exact comparison query |
| `best gmail client for mac` | Absent from returned organic top 10 | The “best clients” article did not capture the checked category query |

The brand/product query was noisy: results also included unrelated “Zen”
email products and older ZenMail identities. Rank 4 therefore demonstrates
indexing and brand capture, not broad category authority.

## Owned content footprint

The current [sitemap](https://usezenmail.com/sitemap.xml) contains 20 URLs:
the homepage, About, Newsroom, Privacy, Terms, and 15 articles.

| Public date | Article | Search/acquisition intent |
| --- | --- | --- |
| 2026-03-21 | [Introducing the Screener](https://usezenmail.com/blog/the-screener) | Product feature / sender control |
| 2026-03-28 | [Native vs. Electron](https://usezenmail.com/blog/native-vs-electron) | Technical differentiation |
| 2026-04-03 | [Inbox zero is a system, not a goal](https://usezenmail.com/blog/inbox-zero-is-a-system) | Productivity education |
| 2026-04-08 | [Why we built ZenMail](https://usezenmail.com/blog/why-we-built-zenmail) | Founder/product narrative |
| 2026-04-10 | [Gmail keyboard shortcuts for Mac](https://usezenmail.com/blog/gmail-keyboard-shortcuts-mac) | Non-brand guide intent |
| 2026-04-12 | [Why Gmail on the web is slow](https://usezenmail.com/blog/why-gmail-is-slow) | Problem/alternative intent |
| 2026-04-15 | [Inbox zero on Gmail](https://usezenmail.com/blog/inbox-zero-gmail) | Gmail productivity intent |
| 2026-04-18 | [Best Gmail clients for Mac](https://usezenmail.com/blog/best-gmail-clients-mac-2026) | Category comparison |
| 2026-04-21 | [Mimestream vs. ZenMail](https://usezenmail.com/blog/mimestream-vs-zenmail) | Competitor comparison |
| 2026-04-23 | [Superhuman alternatives](https://usezenmail.com/blog/superhuman-alternatives-2026) | Competitor-alternative intent |
| 2026-04-25 | [CASA Tier 2 verification](https://usezenmail.com/blog/casa-tier-2-verification) | Security trust |
| 2026-05-05 | [Manage multiple Gmail accounts](https://usezenmail.com/blog/manage-multiple-gmail-accounts-mac) | Workflow guide |
| 2026-05-10 | [Use Gmail offline on Mac](https://usezenmail.com/blog/gmail-offline-mac) | Offline/category intent |
| 2026-05-17 | [Best apps for MacBook Neo](https://usezenmail.com/blog/best-apps-macbook-neo-2026) | Adjacent listicle discovery |
| 2026-06-26 | [Notion Mail is shutting down](https://usezenmail.com/blog/notion-mail-shutting-down-alternatives) | Timely migration/alternative intent |

Dates above come from current article structured data. Some differ from sitemap
`lastmod` values or visible index labels. They establish current metadata, not
an independently archived publication date.

The content set is unusually broad relative to a gated beta: product posts,
Gmail how-tos, category lists, competitor comparisons, a security proof post,
and a timely shutdown alternative. Every article routes through the global
navigation or `/#waitlist`; no separate content upgrade or public product
trial was observed.

## Content quality risks

The current articles visibly lack outbound citations for consequential
technical, security, pricing, memory, and performance comparisons.

The public corpus also conflicts with itself:

- the homepage says Swift/AppKit; several articles say Rust/Tauri;
- the homepage says “protected” local database; legal/editorial pages say
  encrypted;
- homepage structured data claims approximately 150 MB of memory, while an
  article claims an under-15-MB binary and sub-100-ms cold start; these are
  different measurements, but neither exposes a public test method;
- the Mimestream comparison correctly describes direct Gmail API sync and
  local storage, but its broader comparative judgments are uncited.

These are acquisition liabilities because comparison pages ask the reader to
trust both the competitor description and ZenMail's own product specification.

## Indexing setup

Observed:

- unique titles, descriptions, canonicals, Open Graph, and Twitter metadata;
- BlogPosting, FAQ, breadcrumb, organization, and website structured data;
- a sitemap with all current content pages;
- index/follow directives;
- explicit permission for search and AI-assistant crawlers;
- English-only content with no hreflang;
- an RSS link in markup whose response could not be confirmed in this pass.

This is a deliberate technical SEO foundation. It does not establish crawling,
indexing, traffic, or citation by AI systems.

## Backlinks and mentions

DataForSEO returned:

| Check | Result |
| --- | ---: |
| Backlink summary | No result row |
| Detailed backlinks, one per domain | `total_count: 0`, `items: 0` |
| Exact-domain Content Analysis search | `total_count: 0`, `items: 0` |
| Brand-plus-category Content Analysis search | 19 results |

The 19 brand-plus-category results were dominated by an older 2020 ZenMail
browser extension and unrelated products. Manual search found current Reddit
pages that the backlink and exact-domain indexes missed. The correct
interpretation is **weak and ambiguous third-party coverage with clear
endpoint coverage gaps**, not “no links exist.”

## Paid-search slice

A narrow Google Ads Transparency advertiser query for `zenmail` returned “No
Search Results.” A domain-targeted ads search covering May 31, 2018 through
July 17, 2026 also returned no items.

That is no evidence of paid Google creative in the checked US slice. It does
not rule out:

- another advertiser name or domain;
- other countries or dates;
- social, sponsorship, display, or affiliate spend;
- campaigns that the endpoint does not index.

## Verdict

Observed with high confidence for the captured date:

- ZenMail has a deliberately indexable 15-article SEO program.
- The homepage captures a precise product-aware query.
- ZenMail did not appear in the returned top 10 for four representative
  non-brand, guide, and comparison queries.
- Labs had no modeled domain, keyword, or page data yet.
- Third-party backlink and mention indexes undercount demonstrably public
  pages.

Unobservable:

- Google Search Console impressions and clicks;
- actual organic sessions or waitlist entries;
- query-to-waitlist conversion;
- whether any article produced a beta invite, Gmail connection, activation, or
  retained user;
- search geography beyond the checked US-English desktop slice;
- the editorial program's production cost and payback.

For Tecotype, this supports a small, evidence-backed search test after the
release gate. It does not support publishing a large comparison library before
the product, claims, and activation funnel can be verified.

Exact requests, task IDs, and spend are in [requests.md](./requests.md).
