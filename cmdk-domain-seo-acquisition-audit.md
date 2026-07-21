# CMDK / Simplehuman domain, SEO, backlink, and acquisition audit

**Audit date:** 21 July 2026

**Domains:** `cmdk.email`, `simplehuman.email`, and `www.simplehuman.email`

**Search market:** Google, United States, English

**Purpose:** determine whether the April 2026 rebrand transferred search and link equity cleanly, identify the pages and referrals that create discoverability, and separate observable acquisition evidence from traffic estimates.

## Verdict

Yes, auditing both domains was necessary. The result changes the priority order:

1. **Fix the migration before producing more content or pursuing backlinks.** The old apex redirects correctly, but sampled deep URLs on `www.simplehuman.email` still return indexable `200` pages. That leaves duplicate legacy pages live and prevents the cleanest possible transfer of signals to CMDK.
2. **The new domain owns most modeled organic visibility, but current visibility is small and fragile.** In the deduplicated DataForSEO snapshot, `cmdk.email` held 200 ranking keywords and 188.529 modeled monthly organic visits, versus 11 keywords and 24.549 for `simplehuman.email`. That is 94.8% of combined keyword rows and 88.5% of combined modeled traffic on the new domain—not 88.5% of actual company traffic.
3. **Search demand is almost entirely job-led, not brand-led.** Of CMDK's 200 ranked keywords, 199 were non-brand. Informational queries produced 88.7% of modeled traffic, while commercial and transactional queries together produced only 4.4%.
4. **A small set of pages carries the channel.** The top two articles produced 50.5% of modeled organic traffic; the top eight produced 87.5%. Only about 40 URLs had any modeled ranking visibility despite a 189-URL sitemap footprint.
5. **Raw backlink totals exaggerate authority.** CMDK had 1,242 observed backlinks from 136 referring domains; the old domain view had 1,966 from 141. Much of the legacy count is sitewide/spam noise, and 82% of referring-domain rows sampled for CMDK reached it through redirects rather than a direct CMDK link.
6. **Public data cannot establish which channel sends “most traffic.”** Organic search is the largest channel that can be modeled publicly. Product Hunt is the clearest launch event, Andrew Yeung is the strongest documented sustained creator referral, Nick Lafferty is the clearest evergreen bottom-funnel referral, and the Chrome Web Store is probably central to product discovery and installation. Their relative shares require CMDK's private analytics.

The immediate growth job is therefore not “get more backlinks.” It is: **complete the migration, recover existing authority, protect the eight pages already working, strengthen a few high-intent pages, and instrument the path from landing page or Store discovery to paid use.**

---

## 1. What this audit can and cannot reveal

### What is observable

- server responses, redirects, canonical tags, sitemaps, indexability, and internal legacy URLs;
- modeled organic rankings and traffic potential;
- crawled backlink and referring-domain graphs;
- public launch, newsletter, review, affiliate, directory, and community links;
- current live search-result positions for a small validation set; and
- public Chrome Web Store footprint and metadata.

### What is not observable publicly

- sessions or unique visitors by source;
- Chrome Web Store impressions, listing conversion, installs by source, or retained users;
- direct and dark-social traffic;
- referral clicks from a particular article or newsletter;
- affiliate clicks, trials, approved conversions, or payouts;
- trial-to-paid conversion, retention, refunds, or revenue by source; and
- whether an organic landing page visitor later installed the extension on another device or session.

DataForSEO's estimated traffic volume (ETV) is a ranking-and-click-through model, not CMDK's analytics. Backlink crawlers report discovered links, not clicks or customers. Chrome's displayed user figure is rounded and does not expose acquisition source. Any public claim that one channel produces a particular percentage of CMDK's total traffic would therefore be invented.

[CMDK's current cookie controls](https://cmdk.email/) list GA4, Mixpanel, Affonso affiliate cookies, Google Ads, Facebook, and X measurement. The owner likely has substantially better website attribution than the public can see, although the presence of these tools does not prove complete or correctly joined data. The unresolved gap is connecting consented website/store acquisition to extension activation and payment.

The right answer to “where do they get most of their traffic?” is:

> **We can rank plausible sources and quantify modeled search visibility, but we cannot determine the actual source mix without CMDK's GA4, Google Search Console, Chrome Web Store, affiliate, and payment data.**

---

## 2. Domain migration audit

[Simplehuman became CMDK on 6 April 2026](https://cmdk.email/post/simplehuman-is-now-called-cmdk/). The migration is partially correct, but it is not complete.

### What works

- `http://simplehuman.email/` and `https://simplehuman.email/` resolve to the CMDK homepage with a permanent redirect.
- Representative old-apex deep paths preserve their path and query string when redirected to CMDK.
- A controlled nonexistent old-apex URL redirects to the equivalent CMDK path, which then returns a true `404`; it does not become a soft-404 homepage.
- All 18 URLs sampled from CMDK's page sitemap returned `200` and self-canonicalized.
- The first 50 URLs sampled from the post sitemap returned `200`.
- CMDK's XML sitemap is discoverable from [`robots.txt`](https://cmdk.email/robots.txt).

### P0 defect: the old `www` host still serves pages

The old apex and old `www` host behave differently:

| Request pattern | Observed behavior | Assessment |
| --- | --- | --- |
| `https://simplehuman.email/{path}` | Path-preserving `301` to `https://cmdk.email/{path}` | Correct foundation |
| `https://www.simplehuman.email/` | Redirects to CMDK | Correct at homepage only |
| `https://www.simplehuman.email/{deep-path}` | Sampled pricing, legal, learn, blog, snippet, read-receipt, and post URLs returned indexable `200` pages with a CMDK canonical | Migration defect |

The legacy `www` host's own [`robots.txt`](https://www.simplehuman.email/robots.txt) and [`sitemap.xml`](https://www.simplehuman.email/sitemap.xml) also return `200` rather than redirecting, although their contents point crawlers toward CMDK. Exact-title and site-restricted searches exposed legacy `www` URLs crawled within the previous 5–14 days. One exact-title Shortwave check returned both the CMDK URL and its old-`www` duplicate. The scale of duplicate indexing is unknown without Search Console, but the issue is active rather than merely historical.

The canonical tags are useful, but they are not a substitute for retiring the old hostname. Google describes redirects and `rel="canonical"` as strong consolidation signals and sitemaps as weaker signals; it recommends permanent server-side redirects when retiring duplicate URLs. See [Google's duplicate-URL consolidation guidance](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

This defect has four consequences:

- Google can continue crawling and sometimes displaying old `www` URLs.
- crawlers and people can keep linking to pages on the old hostname;
- migration signals are split across a redirecting apex and a live duplicate `www` host; and
- clean before/after measurement is harder because the old property has not actually disappeared.

Apply redirect rules before WordPress, caching, or application routing. **Evaluate exact legacy-path mappings first**, then use this host-wide path-preserving rule as the fallback:

```text
https?://(www.)?simplehuman.email/{path}?{query}
    → 301 https://cmdk.email/{path}?{query}
```

The fallback must preserve path and query string and should resolve in one hop. Exact mappings must precede it; otherwise renamed URLs still take two hops and `/privacy.html` still reaches the wrong CMDK path. Keep the redirects indefinitely while the old domain remains controlled.

### Broken and chained legacy URLs

Several indexed or discoverable old URLs do not arrive at a useful final page:

| Legacy URL | Observed result | Required disposition |
| --- | --- | --- |
| `www.simplehuman.email/post/what-is-the-best-follow-up-reminder-tool-for-gmail/` | Direct `404`; the CMDK version of the old slug has a redirect to a current reminder article | Send the legacy URL directly to that current canonical reminder article |
| `www.simplehuman.email/post/how-to-set-up-gmail-reminders-that-actually-work-stop-forgetting-to-follow-up/` | Redirects through `cmdk.email/?p=27621`, then `404` | Map directly to the current reminder guide |
| `www.simplehuman.email/post/how-simplehuman-teaches-you-gmail-keyboard-shortcuts-while-you-work-2/` | Redirects through `cmdk.email/?p=27769`, then `404` | Map directly to the canonical keyboard-shortcut guide or its closest surviving section |
| `simplehuman.email/privacy.html` | Generic path-preserving redirect to `cmdk.email/privacy.html`, then `404` | One-hop `301` to [`cmdk.email/privacy/`](https://cmdk.email/privacy/) |

Other renamed posts sometimes take two redirects: old host → same slug on CMDK → renamed final slug. Collapse chains for URLs with links, impressions, or clicks. A one-hop redirect reduces failure modes and makes the intended target unambiguous. In implementation order, exact legacy-path mappings come first and the host-wide rule catches everything else.

### Search Console migration controls

Google's Change of Address procedure requires ownership of every relevant source and destination property. The old apex and old `www` variant should both be verified and checked; a move submitted only for the apex does not retire a live `www` host. Follow [Google's Change of Address instructions](https://support.google.com/webmasters/answer/9370220?hl=en).

After the host-wide redirects are deployed:

1. verify `simplehuman.email`, `www.simplehuman.email`, and `cmdk.email` in Search Console;
2. submit or confirm Change of Address for each old property that Google recognizes separately;
3. submit only the canonical CMDK XML sitemap;
4. inspect the broken URLs above and a sample of high-link/high-impression legacy URLs;
5. monitor indexed old URLs, redirect errors, not-found pages, and canonical selection weekly; and
6. keep the old domain, TLS certificates, and redirect service operational.

### Sitemap and indexation cleanup

CMDK exposes two overlapping XML systems plus an HTML sitemap:

- [`sitemap.xml`](https://cmdk.email/sitemap.xml), a valid sitemap index with misc, post, and page children;
- [`sitemap_index.xml`](https://cmdk.email/sitemap_index.xml), a second Rank Math index with overlapping URLs and empty Elementor/category children; and
- [`sitemap.html`](https://cmdk.email/sitemap.html), an indexable HTML page that is itself included in XML and also declared as a `Sitemap:` in `robots.txt`.

Recommended cleanup:

- choose one XML sitemap system and expose only canonical, indexable `200` URLs;
- remove the `Sitemap:` directive pointing to the HTML page;
- remove the HTML sitemap from XML, and either make it a genuinely useful navigational page or remove/noindex it;
- remove empty sitemap children; and
- review utility/preview URLs such as `/installed/` and `/wall-of-love-preview/` for intentional indexability.

Google expects sitemap files to identify canonical URLs and documents the supported formats in its [sitemap guidance](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview).

### Stale internal content

The public WordPress API exposed three stored records with old-domain references:

- `/india/`: 26 image references on `http://simplehuman.email/wp-content/...` and one old-domain self-link;
- `/learn-to-use/`: one legacy HTTP GIF; and
- `/terms/`: old-domain wording plus a broken plain-text `/privacy.html` URL reference.

Replace these in the stored content, not only at the rendering/cache layer. The legal page should also use the current company/product identity consistently.

No `hreflang` was found. That is not inherently a defect. Add regional annotations only if `/india/` is a true locale-specific alternative to another page; otherwise a single canonical English page is simpler.

### Performance was not verified

The PageSpeed Insights API returned a quota response during the audit, and no reliable field-data source was available. This report makes no Core Web Vitals or performance claim. Use Search Console's Core Web Vitals report and CrUX/PSI when available rather than inferring performance from one synthetic request.

---

## 3. Organic search footprint

### Old versus new domain

The deduplicated US-English Google snapshot was:

| Domain | Ranked keywords | Modeled organic ETV/month | Modeled traffic value | Paid keywords |
| --- | ---: | ---: | ---: | ---: |
| `cmdk.email` | 200 | 188.529 | $691.89 | 0 |
| `simplehuman.email` | 11 | 24.549 | $28.72 | 0 |
| Directional combined total | 211 | 213.078 | $720.61 | 0 |
| New-domain share | 94.8% | 88.5% | 96.0% | — |

Do not treat the combined row as a traffic total. Search datasets can retain stale or overlapping URLs during a migration, and this audit found only two intersecting keyword rows between the domains. The split is best used as a migration trend: the new domain is dominant, while the old domain has not disappeared.

CMDK's position distribution also shows how early the footprint remains:

| Position band | Keywords |
| --- | ---: |
| 1–3 | 0 |
| 4–10 | 6 |
| 11–20 | 24 |
| 21–50 | 114 |
| 51–100 | 56 |

There were 158 newly detected keywords and 34 improved keywords in the snapshot. That is consistent with crawler recognition after the rebrand, not proof of an equivalent increase in visits.

### Search-model validation

Live SERP checks were weaker than the weekly ranking model on several queries:

| Query | Snapshot model / live check | Interpretation |
| --- | --- | --- |
| `how to bulk delete gmail` | Modeled as visible; absent from first 21 live results | Model likely stale or volatile |
| `gmail mass unsubscribe` | Modeled as visible; absent from first 22 | Model likely stale or volatile |
| `email reminders in gmail` | Model #7; live #18 | Material overstatement |
| `gmail keyboard shortcuts` | Modeled as visible; absent from first 22 | Weak current head-term visibility |
| `where is remove formatting button in gmail` | Live #12; old domain absent from first 30 | One confirmed useful ranking |
| `superhuman alternative` | Live #19 | Commercial page has improvement room |
| `superhuman chrome extension` | Live #13 | Relevant, but below first-page traffic concentration |

The small head-query set did not show simultaneous old/new results, but exact-title and site-restricted checks did. Duplicate-index scale is unknown without Search Console; it should not be dismissed as either isolated or widespread from this sample alone.

### Brand demand and naming collision

CMDK has almost no measurable qualified brand-search demand:

- only one of the 200 ranked rows was branded-ish: `simplehuman email sign up`, with 3.283 ETV;
- no ranked query beginning with `cmdk` appeared in the domain dataset;
- `cmdk email`, `cmdk gmail`, and `cmdk extension` had no measurable database volume;
- bare `cmdk` had roughly 590 average monthly searches in the keyword model, but live results were dominated by the `cmdk` React component/library ecosystem and shortcut tools; and
- `simplehuman email` demand was tiny and contaminated by the much larger housewares brand.

The product can rank first for a highly qualified query such as `cmdk email` without receiving meaningful traffic if almost nobody searches for it. It is unlikely to displace the developer-library entity for bare `cmdk` efficiently.

Use one explicit entity label across page titles, H1s, organization/software schema, profiles, Store metadata, and editorial anchors: **“CMDK for Gmail”** or **“CMDK Email.”** The goal is to grow a qualified entity, not to win the ambiguous three-letter head term.

### Intent mix

| Search intent | Keywords | ETV | Share of CMDK ETV |
| --- | ---: | ---: | ---: |
| Informational | 175 | 167.263 | 88.7% |
| Navigational | 10 | 12.994 | 6.9% |
| Transactional | 11 | 6.529 | 3.5% |
| Commercial | 4 | 1.743 | 0.9% |

The site is being discovered as a Gmail help publication. It is not yet being discovered primarily as a product or purchase option. The homepage ranked for only one term and 3.283 ETV—1.7% of the domain total.

This can still create customers, but only if useful articles move readers into an honest, relevant product action. The current dataset cannot show that conversion.

### Pages that carry the channel

| Rank | CMDK page/topic | Keywords | ETV | Modeled value |
| ---: | --- | ---: | ---: | ---: |
| 1 | Use the Delete key to delete Gmail messages | 27 | 59.801 | $296.55 |
| 2 | Gmail rules | 24 | 35.355 | $198.56 |
| 3 | Bulk unsubscribe / sender cleanup | 16 | 15.502 | $115.08 |
| 4 | Instant Copy | 4 | 14.336 | — |
| 5 | Gmail font size | 24 | 12.235 | — |
| 6 | Gmail reminders | 13 | 12.140 | — |
| 7 | Gmail archive | 6 | 8.100 | — |
| 8 | Gmail attachments | 28 | 7.434 | — |

The top two pages account for 95.156 ETV, or 50.5% of the domain total. The top eight account for 164.903 ETV, or 87.5%. The next notable product/commercial pages were the homepage (3.283), Superhuman Chrome extension page (2.780), keyboard guide (2.429), snippets (1.017), and pricing (0.882).

This is a fragile portfolio. A ranking change to two articles can move the whole modeled channel materially.

### Publishing footprint versus yield

The canonical sitemap footprint contained 169 posts, 18 pages, the homepage, and the HTML sitemap: 189 URLs. Only about 40 pages had any modeled ranking visibility, a directional yield of roughly 21%.

Publication timing was unusually concentrated:

| Publication month | Posts |
| --- | ---: |
| Jul–Dec 2025 | 15 |
| Jan 2026 | 99 |
| Feb–May 2026 | 13 |
| Jun 2026 | 13 |
| Jul 2026 to audit date | 29 |

The 99 January pages are largely templated individual keyboard-shortcut pages. This creates coverage, but also risks thin intent overlap with the main shortcut guide. The right response is not a blind mass deletion. Use Search Console clicks, impressions, query overlap, inbound links, and content uniqueness to decide which pages should remain, merge, redirect, or canonicalize into a stronger hub.

### Competitive context

The competitor data is directional because each domain has a different content breadth:

- Simplify Gmail's raw `simpl.fyi` data is polluted by the generic word “simplify.” Excluding that obvious ambiguity left about 22 qualified keywords and 67.112 ETV, with strong rankings for phrases such as `simplify gmail`.
- Boomerang's domain footprint was much larger: 1,896 keywords and 36,627.894 ETV, including 36 #1 rankings and 790 more keywords in positions 2–10.
- Superhuman's current domain footprint was much broader again, but the site now spans Grammarly, Coda, Go, and related products, so its 17,302 keywords and 91,731 ETV are not an apples-to-apples email benchmark.

CMDK has achieved more generic Gmail how-to coverage than its tiny brand demand would imply. It has not yet built the qualified brand demand or first-page commercial visibility of the established products.

---

## 4. Backlink audit

### Headline counts

DataForSEO's current target views were:

| Target | Backlinks | Referring pages | Referring domains | Main domains | Nofollow pages | Broken backlinks | Crawler rank | Spam score |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `cmdk.email` | 1,242 | 1,061 | 136 | 131 | 552 | 1 | 225 | 18 |
| `simplehuman.email` including subdomains | 1,966 | 1,746 | 141 | 139 | 379 | 3 | 325 | 12 |

These target views overlap through redirects and must not be added. The old-domain total also conceals very different hosts:

| Legacy host | Backlinks | Referring domains | Referring pages | Notable issue |
| --- | ---: | ---: | ---: | --- |
| old apex only | 744 | 35 | 543 | 427 `.io` links; crawler spam score 30 |
| old `www` only | 1,222 | 108 | 1,203 | 812 `.in` links; large sitewide/noise cluster |

The legacy host counts sum at link level, but referring domains can overlap. The large `.in` and `.io` clusters show why “1,966 backlinks” is not equivalent to 1,966 editorial endorsements.

### Link transfer and anchor state

In a one-row-per-referring-domain sample for the new domain:

- 23 of 131 rows linked directly to CMDK;
- 108 of 131, or 82%, reached CMDK through redirects from a legacy URL;
- 36 were dofollow and 95 nofollow; and
- the most common source-domain anchors remained exact old URLs or the Simplehuman name.

Top sampled anchor groups by number of source domains were:

| Anchor group | Referring domains in sample |
| --- | ---: |
| Exact old URL | 20 |
| `simplehuman.email` | 14 |
| `superhuman email alternative` | 6 |
| `cmdk email` | 4 |
| `Simplehuman` | 4 |
| `cmdk.email` | 3 |
| `cmdk` | 3 |

The redirect graph is doing most of the work, which makes the live old `www` host particularly costly. Directly updating controllable and high-value editorial links would reduce dependence on that graph and establish the new entity faster.

The top destination distribution in the same sample was also concentrated:

| CMDK destination | Referring domains | Dofollow |
| --- | ---: | ---: |
| Homepage | 89 | 20 |
| Superhuman alternative | 14 | 4 |
| Inbox Zero | 13 | 1 |
| Pricing | 2 | 2 |
| Bulk unsubscribe | 2 | 1 |

These listed destinations account for 120 of the 131 referring domains and 28 of the 36 dofollow domains. The remaining 11 domains, including 8 dofollow, were distributed across other destinations.

### Link-history interpretation

Crawler history shows recognition of the move:

| Month end / current | CMDK backlinks / domains | Simplehuman backlinks / domains |
| --- | ---: | ---: |
| 30 Apr 2026 | 579 / 12 | 2,745 / 129 |
| 31 May 2026 | 1,145 / 99 | 2,302 / 140 |
| 30 Jun 2026 | 1,190 / 122 | 2,111 / 140 |
| 21 Jul 2026 | 1,242 / 136 | 1,966 / 141 |

That pattern is consistent with crawler recognition and redirect inheritance after the rebrand. It is not evidence of 1,000 new independent endorsements. The new/lost backlink feeds contain many link instances from repeating templates and crawler recrawls; they should not be treated as users, traffic, or commercial momentum.

### Backlink decision

Do not launch a broad link-building campaign yet, and do not disavow domains solely because a third-party crawler labels them spammy.

Priorities are:

1. make every old host redirect consistently;
2. update links the company controls;
3. request updates from the handful of editorial/referral sources that plausibly send qualified users;
4. earn product-relevant evidence links, not bulk directory links; and
5. use Google Search Console's manual-actions and link reports before considering a disavow file.

DataForSEO documents that its [backlink endpoint](https://docs.dataforseo.com/v3/backlinks-backlinks-live/) reports crawled link records and its [history endpoint](https://docs.dataforseo.com/v3/backlinks-history-live/) reports historical crawler counts. Neither is a clickstream or attribution system.

---

## 5. Likely acquisition sources

This is an evidence ranking, not a traffic-share ranking.

| Source | Observable evidence | Likely role | Confidence / limitation |
| --- | --- | --- | --- |
| [Chrome Web Store](https://chromewebstore.google.com/detail/cmdk-read-receipts-split/nipfocapamlefjhldhcagammlldbangf?hl=en-US) | Featured listing; about 59–60 ratings; public surfaces showed a rounded 1,000–2,000-user range during research | Always-on product search, trust, installation, and possibly direct discovery that bypasses the website | Structurally central; no public impressions, source mix, listing conversion, or paid conversion |
| Google organic | 188.529 new-domain plus 24.549 residual old-domain modeled ETV in the snapshot | Largest publicly quantifiable website-discovery channel; mostly generic Gmail help | Modeled and partly stale; not sessions or customers |
| [Product Hunt](https://www.producthunt.com/products/simplehuman) | #4 product of the day; launch backlinks and social proof | Clearest documented launch burst | Founder says it brought “a lot of users” and eventual customers, but supplied no counts; one-time event |
| [Andrew Yeung newsletter](https://www.andrew.today/p/my-ai-productivity-stack) | Personal-use endorsement in a productivity-stack issue; old-root link redirects | Strong creator recommendation with relevant audience and residual tail | Founder said it still sent daily users two weeks later; self-reported and unquantified |
| [Nick Lafferty's Superhuman alternatives](https://nicklafferty.com/reviews/superhuman-alternatives/) | Ranks Gmail + CMDK first and links directly with an attribution parameter | Highest-intent evergreen comparison referral found | Clicks/conversions unknown; commercial relationship or affiliate status not established publicly |
| Community discussion | A real advocate in a [Growthhacking.fr email-client thread](https://www.growthhacking.fr/t/meilleur-client-mail-pour-macos-pour-utiliser-gmail/36950); some Reddit discussion | Trust and evaluation at point of need | Tiny corpus; repeated recommendations often trace to one account; not independent scale evidence |
| Niche publications | [IndianVC stack page](https://www.indianvcs.com/vc-stack/product/simplehuman-mail), Amit Sarda productivity-tool list, 80/20 AI mention | Long-tail awareness and backlinks | Unknown clicks; mixed editorial/commercial context |
| Founder-seeded directories | AlternativeTo, Startup Listing, SaaSHub, one G2 review, portfolio pages | Search-result occupancy and credibility fragments | Mostly low-engagement, maker-added, derivative, or tiny review surfaces |

No paid-search keywords were detected for either domain in the snapshot. That is evidence against a visible Google Ads search program at that moment, not proof that CMDK never uses paid social, display, retargeting, or short campaigns.

### Product Hunt is the clearest launch channel

The maker's [Product Hunt retrospective](https://www.linkedin.com/posts/guduthur_i-launched-on-product-hunt-and-it-led-to-activity-7299074104605753344-GW-E) says the launch produced many users, eventual customers, five newsletter features, and a ranking lift. That is the best first-person source about a discrete acquisition event. It remains vendor-reported and lacks session, install, conversion, or revenue numbers.

### Andrew Yeung is the clearest sustained creator referral

Andrew's article is a first-person “my stack” endorsement rather than a generic directory entry. The founder separately said the newsletter continued to send daily users two weeks later. Its current link still points to the old `www` root, so asking for a direct CMDK update is a small, high-confidence migration win.

### Nick Lafferty is the clearest evergreen bottom-funnel referral

The comparison meets users already evaluating a costly incumbent and gives a concrete Gmail-plus-CMDK recommendation. Its `?atp=nicklafferty` parameter makes intentional attribution plausible. The public page does not prove an affiliate or sponsorship arrangement, and no click/conversion data is available.

### The Store may matter more than website traffic reports show

The product is installed from Chrome Web Store. A person can discover it there, from browser search, or through a direct Store link without first becoming a session on `cmdk.email`. Store listing views and installs must therefore be analyzed alongside website traffic. Organic website ETV cannot answer product-acquisition share on its own.

### Affiliate channel is live but commercially inconsistent

The [official affiliate page](https://cmdk.email/affiliate/) advertises 20% lifetime commission, a 60-day cookie, and a 30-day hold. An [OpenPartner marketplace listing](https://openpartner.dev/marketplace/off_01KRNWBAKEKN4G91CCKPW6ER1X) advertises 40% for 36 months with the same 60-day cookie and 30-day hold. These may be concurrent offers or one may be stale, but public prospects cannot tell.

Resolve the terms before recruiting partners. Affiliate availability is an acquisition/referral tactic, not evidence that the channel currently sends meaningful traffic or revenue.

### What does not qualify as Tecotype distribution

None of these channels meets this workspace's strict definition of distribution: introduction to zero-existing-user audiences through permanent pre-install discovery with an attributable first-action-to-paid funnel. They are acquisition, referral, or marketplace discovery. The Chrome Web Store is the closest persistent install surface, but public evidence does not establish an attributable paid funnel.

---

## 6. Recommended action plan

### P0 — recover and consolidate existing authority

| Action | Owner type | Completion test |
| --- | --- | --- |
| Add explicit one-hop mappings for broken/renamed legacy URLs, evaluated first | Web/SEO | Every old URL with links, impressions, or prior clicks reaches a relevant canonical `200` in one redirect |
| Deploy a host-wide, path/query-preserving fallback `301` from both old hosts | DNS/edge/web | After exact mappings, representative `http`, `https`, apex, `www`, slash/no-slash, deep path, query, and nonexistent cases behave correctly |
| Complete Search Console migration controls for apex and `www` | SEO/admin | All properties verified; Change of Address status known; canonical sitemap submitted; old indexed count trends down |
| Update controllable public links and brand metadata | Marketing/product | Chrome Store, Product Hunt, AlternativeTo, SaaSHub, Startup Listing, G2, DesignCrew/portfolio, LinkedIn, legal pages, and emails use CMDK URLs/name |
| Request updates from high-value third parties | Founder/marketing | Andrew, Nick if needed, Growthhacking advocate/thread owner where appropriate, IndianVC, Amit Sarda, and 80/20 AI link directly to CMDK |
| Repair stale content URLs and sitemap duplication | Web/content | No old-domain strings in stored public content; one XML sitemap system; no HTML sitemap directive |

Do these before evaluating whether rankings “recovered.” Otherwise the baseline continues changing underneath the measurement.

### P1 — protect and convert the visibility that exists

1. **Refresh the top eight pages first.** Add answer-first structure, current Gmail screenshots, tested steps, dates, author/reviewer ownership, and precise distinctions between native Gmail behavior and CMDK behavior.
2. **Correct the “bulk unsubscribe” claim.** If CMDK's Nuke action blocks and deletes mail but does not send standards-based unsubscribe requests, describe it as sender suppression/cleanup. A high-traffic page must not win by promising a different action.
3. **Build contextual product bridges.** The Delete, rules, unsubscribe, font, reminder, archive, and attachment articles should each demonstrate one directly relevant CMDK outcome and offer a measured Store/install action—not a generic banner alone.
4. **Improve the commercial pages already near reach.** The Superhuman alternative page (#19 live) and Superhuman Chrome-extension page (#13) are closer to paid intent than most informational posts. Strengthen them with explicit fit/non-fit, current prices, verifiable workflow demonstrations, migration/reversibility, and transparent limitations.
5. **Turn shortcut sprawl into a navigable hub.** Keep unique shortcut pages that satisfy a distinct query; merge thin overlaps into the canonical guide; add breadcrumbs and strong hub/spoke internal links; avoid creating another 99-page burst without evidence of differentiated intent.
6. **Connect authority to conversion pages.** The homepage and pricing page together receive little modeled search visibility. Link to relevant feature and decision pages from ranking articles with descriptive anchors.

### P2 — build qualified demand, not vanity volume

- standardize the entity as “CMDK for Gmail” or “CMDK Email”;
- publish original, citable evidence: Gmail workflow measurements, failure/recovery testing, extension architecture boundaries, and transparent comparisons;
- pursue a small number of independent Gmail/productivity reviewers whose audiences match the desktop Gmail power-user job;
- reconcile affiliate terms and give partners attributable direct links;
- monitor rather than chase low-quality directory links;
- review preview, installation, author, tag, category, and utility pages for indexation value; and
- run a field-data performance audit when Search Console/CrUX data is available.

### What not to do

- Do not spend against the ambiguous bare `cmdk` term.
- Do not add old- and new-domain backlink totals together.
- Do not call modeled ETV “traffic” without a qualifier.
- Do not treat a crawler's spam score as a reason to submit a disavow file.
- Do not publish more templated shortcut pages merely because the sitemap can hold them.
- Do not infer channel success from backlinks, Product Hunt points, Store users, or review count without a paid conversion join.

---

## 7. Measurement design needed to answer the traffic question

### Funnel

```text
source / campaign / query
→ canonical landing page or Chrome Store listing
→ Store click or install
→ first useful Gmail action
→ trial start
→ paid conversion
→ retained paid use
```

The join should use privacy-preserving campaign and product events—not mailbox contents. Chrome Web Store does not ordinarily pass an arbitrary campaign token into the installed extension, so website-assisted installs need an explicit, consented handoff such as a website-to-extension handshake or authenticated account join. Store-first installs that never touch the website generally cannot be deterministically joined to an external source; measure those in aggregate. Campaign detail should expire or aggregate once attribution no longer requires it.

### Minimum data sources

| System | Required data | Decision it enables |
| --- | --- | --- |
| Google Search Console | query, page, clicks, impressions, position, canonical/indexing split by old/new property | Migration recovery and organic landing-page demand |
| Website analytics | landing page, referrer, campaign, Store outbound click | Which public sources and articles create install intent |
| Chrome Web Store dashboard | listing impressions, installs/uninstalls where exposed, geography, listing conversion | Store discovery versus website-assisted installation |
| Extension telemetry | consented website/account handoff where available, aggregate Store cohort, first useful action, trial start | Which measurable sources activate—not merely click |
| Billing/subscription | privacy-safe customer key, plan, payment, refund, retention | Source-to-paid and source-to-retained value |
| Affiliate platform | partner, click, trial, approved paid conversion, reversal | Whether the program produces attributable paid and retained customers |

### Weekly migration dashboard for 90 days

- GSC clicks and impressions to `cmdk.email` versus both old properties;
- indexed and submitted URLs by host;
- old URLs selected as canonical or shown in search;
- redirect errors, loops, chains, and old-host `200` responses;
- not-found URLs with prior clicks, impressions, or backlinks;
- direct CMDK referring domains versus redirected legacy sources;
- top-eight page clicks, positions, Store clicks, activations, and paid conversions;
- branded queries for `cmdk email`, `cmdk gmail`, and `cmdk for gmail`; and
- source-to-first-action, source-to-paid, refund, and 30/60/90-day retention.

### Decision thresholds

Use trends, not arbitrary backlink counts:

- **Migration healthy:** no old-host `200` pages; old indexed URLs fall steadily; new-domain clicks rise without persistent split canonicals; high-value legacy links resolve in one hop.
- **Content healthy:** top-page clicks are not merely impressions; Store-click and first-action rates hold after refresh; the portfolio becomes less dependent on two articles.
- **Referral healthy:** a partner creates attributable first actions and paid retention, not just a link.
- **Brand healthy:** qualified CMDK-for-Gmail queries grow and land on the intended entity, even if the product never wins bare `cmdk`.

---

## 8. Implications for Tecotype

CMDK validates one useful acquisition thesis: generic email jobs can create discovery before a new brand has search demand. It does not validate a high-volume content mill or prove that informational readers become paid users.

For Tecotype, the transferable approach is:

- lead with jobs that expose the product's actual structural advantage, such as local retrieval of already-synchronized mail during unreliable connectivity, provider-independent search, multi-account finding, multilingual retrieval, and evidence-based switching from expensive clients;
- publish fewer, stronger pages with original demonstrations and an attributable first-action path;
- preserve one consistent brand entity and canonical domain from launch;
- treat extension stores, directories, and editorial mentions as acquisition unless a pre-install and paid-conversion funnel proves distribution; and
- keep privacy structural: source attribution never requires mailbox credentials or message content to reach Tecotype infrastructure.

This is research guidance, not a product or channel commitment. The detailed competitive/product context remains in [the CMDK market analysis](./cmdk-simplehuman-market-analysis.md).

---

## 9. Method and reproducibility

### Collection

The audit combined:

- direct HTTP inspection of redirects, status codes, canonical tags, sitemap files, `robots.txt`, and representative URLs;
- WordPress API inspection for publication timing and stored legacy URLs;
- DataForSEO Labs ranked-keyword, relevant-page, keyword-overview, SERP, backlink summary, backlink detail, referring-domain, new/lost, and history endpoints;
- live Google-result validation for a small query set;
- manual inspection of identified editorial, launch, community, directory, affiliate, and Store sources;
- comparison with the prior CMDK market/customer report;
- a current Tecotype source-tree spot check for synchronized local mail, search, account, and provider boundaries; architecture drafts were not treated as shipped behavior.

DataForSEO usage followed the repository's [setup and cost
controls](./tools/dataforseo.md). The audit cost approximately **$1.04**,
including validation calls and competitor context. This excludes the roughly
$0.30 of search work already recorded in the earlier market analysis.

Where parallel calls overlapped, rows were deduplicated and totals were not
added.

### Evidence cautions

- Rankings, snippets, and indexed URLs can change after the audit date.
- ETV and traffic value are modeled estimates.
- The live SERP set was deliberately small and validates volatility, not every keyword.
- Referring-domain samples are crawler samples, not a full editorial-quality review of every link.
- Backlink host views overlap through redirects.
- Founder statements about users or traffic are clearly labeled as self-reported.
- The audit did not access private analytics, Search Console, Store dashboards, billing, or affiliate conversions.
- Performance and Core Web Vitals remain unverified.

## Primary reference links

- [CMDK rebrand announcement](https://cmdk.email/post/simplehuman-is-now-called-cmdk/)
- [CMDK Chrome Web Store listing](https://chromewebstore.google.com/detail/cmdk-read-receipts-split/nipfocapamlefjhldhcagammlldbangf?hl=en-US)
- [CMDK robots.txt](https://cmdk.email/robots.txt)
- [CMDK canonical sitemap](https://cmdk.email/sitemap.xml)
- [CMDK secondary sitemap index](https://cmdk.email/sitemap_index.xml)
- [CMDK HTML sitemap](https://cmdk.email/sitemap.html)
- [Google: consolidate duplicate URLs](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)
- [Google: site moves and Change of Address](https://support.google.com/webmasters/answer/9370220?hl=en)
- [Google: sitemap guidance](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview)
- [DataForSEO Backlinks API](https://docs.dataforseo.com/v3/backlinks-backlinks-live/)
- [DataForSEO backlink history](https://docs.dataforseo.com/v3/backlinks-history-live/)
- [Product Hunt listing](https://www.producthunt.com/products/simplehuman)
- [Founder Product Hunt retrospective](https://www.linkedin.com/posts/guduthur_i-launched-on-product-hunt-and-it-led-to-activity-7299074104605753344-GW-E)
- [Andrew Yeung productivity-stack mention](https://www.andrew.today/p/my-ai-productivity-stack)
- [Nick Lafferty Superhuman alternatives](https://nicklafferty.com/reviews/superhuman-alternatives/)
- [CMDK affiliate terms](https://cmdk.email/affiliate/)
- [OpenPartner CMDK listing](https://openpartner.dev/marketplace/off_01KRNWBAKEKN4G91CCKPW6ER1X)
