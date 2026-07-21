# CMDK / Simplehuman SEO strategy and traffic-source analysis

- **Analysis date:** 21 July 2026
- **Search market:** Google, United States, English
- **Domains:** `cmdk.email`, with residual visibility from `simplehuman.email`
- **Purpose:** understand CMDK's SEO system, the demand it does and does not capture, the sources that plausibly introduce users, and the parts Tecotype can reuse.

## Executive interpretation

CMDK is building a **Gmail-help publication around a Chrome extension**. Its search strategy is not primarily to rank as an email client. It targets a concrete job inside Gmail, answers the native-Gmail question, introduces the nearest CMDK capability, and sends the reader to the Chrome Web Store. Recent articles use an article-specific campaign link; older pages rely more heavily on generic Store CTAs.

```text
specific Gmail problem
        ↓
native answer or free utility
        ↓
point where Gmail becomes awkward
        ↓
contextual CMDK feature
        ↓
campaign-tagged Chrome Store CTA
        ↓
install and trial inside Gmail
```

The public ranking footprint confirms the first half of that system but not the commercial outcome:

- CMDK has **200 modeled US ranking keywords and 188.529 modeled monthly organic estimated traffic volume (ETV)**. The old domain separately retains 11 keyword rows and 24.549 residual ETV; migration records may overlap, so the two are only a directional combined view. ETV is a ranking model, not sessions.
- **88.7% of CMDK's modeled ETV is informational.** The homepage contributes only 1.7%. Searchers mostly meet CMDK as a Gmail tutorial, not as a named product or email-client choice.
- The live rankings that held up were narrow jobs such as `archive shortcut gmail` at #6 and `how to set reminder in gmail` at #9. CMDK was outside the first 30 for larger, more product-qualified searches including `email client for gmail`, `gmail read receipts`, `gmail templates`, `gmail keyboard shortcuts`, and `chrome extensions for gmail`.
- The DataForSEO model says the top eight articles contribute 87.5% of ETV, but same-day SERPs were materially weaker for several supposed head-term wins. The likely real traffic is modest and even more long-tail-heavy than the model suggests.
- The 90 shortcut posts published in one January batch produced only 17.647 ETV, 9.4% of the domain total, and just eight had modeled visibility. A small number of older, broader job pages carry the channel.

It is therefore not defensible to describe CMDK as “mostly word of mouth.” The more accurate public-evidence description is:

> **Launch-and-creator seeded, Chrome-Store-routed, content-supported, and referral-amplified.**

Product Hunt and a founder network supplied the launch burst; newsletters and comparison pages supplied trusted referrals; the Chrome Web Store is the persistent install surface; SEO is now being industrialized; and a 20% recurring affiliate program plus an optional referral signature turns recommendation into an incentivized channel. Private analytics would be required to rank those sources by actual sessions, installs, or paid customers.

For Tecotype, the reusable idea is **the job-to-product bridge**, not the publishing volume. Tecotype should own the moment when literal email search fails: help the reader retrieve the message natively, demonstrate the limit of exact-word search, then show—in a synthetic mailbox—how local Better search can find what the reader remembers. Start with four strong pages and one embedded demonstration, not a shortcut content mill.

## 1. The acquisition system behind the SEO

CMDK's discoverability has developed in layers rather than through one channel.

### Layer 1: founder network and launch

The February 2025 [Product Hunt launch](https://www.producthunt.com/products/simplehuman) finished #4 with 523 points and now shows 556 followers. In the founder's [launch retrospective](https://www.linkedin.com/posts/guduthur_i-launched-on-product-hunt-and-it-led-to-activity-7299074104605753344-GW-E), he says friends and his Twitter network rallied the early votes; the launch produced users and eventual customers; five newsletters then featured the product; and the Product Hunt backlink lifted rankings. Those are first-person claims without counts, but they show the sequence he believes mattered:

```text
founder network → Product Hunt → newsletters/creators → users/customers → links/search lift
```

This is network-seeded acquisition, not passive word of mouth.

### Layer 2: trusted creator and comparison referrals

[Andrew Yeung's productivity-stack article](https://www.andrew.today/p/my-ai-productivity-stack) describes personal use: Simplehuman helped him process email faster “like Superhuman, but for Gmail.” The founder said it was still sending new users every day two weeks after publication. The claim is unquantified, but it is the strongest documented sustained creator referral.

[Nick Lafferty's Superhuman alternatives page](https://nicklafferty.com/reviews/superhuman-alternatives/) puts Gmail plus CMDK first and explains its fit, features, price, and limitations. Its CMDK link carries an attribution parameter. This is the clearest evergreen bottom-funnel referral found because it meets a reader already comparing paid email products. Public data does not expose clicks or conversions.

### Layer 3: Chrome Web Store discovery and conversion

The [Chrome Web Store listing](https://chromewebstore.google.com/detail/cmdk-read-receipts-split/nipfocapamlefjhldhcagammlldbangf?hl=en-US) is **Featured**, shows **2,000 users**, a **4.9 rating from 59 ratings**, and a keyword-rich title: “Read Receipts, Split Inbox, Hotkeys & Reminders for Gmail.” It is both the install endpoint and a possible discovery surface in its own right.

This distinction matters. A person can discover CMDK in the Store, through Google, or from a creator's direct Store link without ever becoming a `cmdk.email` session. Website traffic estimates cannot reveal the installation mix.

### Layer 4: publication SEO

CMDK's [blog proposition](https://cmdk.email/blog/) is explicit: “Gmail tips, keyboard shortcuts, and honest takes on the email tools worth your time.” The content does three acquisition jobs:

1. capture non-brand Gmail problems;
2. intercept people comparing Superhuman and adjacent tools; and
3. create useful or citeable assets that can earn search visibility and links.

### Layer 5: structured referrals

The [affiliate program](https://cmdk.email/affiliate/) offers 20% recurring commission for the customer's lifetime, a 60-day attribution window, and a 30-day hold. The Store listing also promotes an optional “Sent via CMDK” signature with a unique referral link and 20% commission.

That productizes recommendation. It may amplify genuine advocacy, but it should not be counted as organic word of mouth, and its current contribution is not public.

## 2. CMDK's publication strategy

### The content inventory is deliberately broad and heavily modified

The public WordPress API exposed 169 posts. Title classifications overlap, but they show the editorial center of gravity:

| Title signal | Posts |
| --- | ---: |
| Mentions Gmail | 139 |
| Mentions a shortcut, keyboard action, or hotkey | 95 |
| Competitor or email-client/category topic | 13 |
| Calculator, generator, tester, builder, or cheat sheet | 6 |
| Writing/template topic | 12 |

Publishing was concentrated in three production bursts:

| Burst | Posts | Strategic purpose |
| --- | ---: | --- |
| 7 January 2026 | 90 | Exact-action and shortcut coverage |
| 30 June 2026 | 13 | Product-feature pages mapped to Gmail jobs |
| 11–16 July 2026 | 29 | Broader how-tos, comparisons, writing assets, tools, and original data |
| **Three-burst total** | **132 / 169** | **78.1% of the whole post inventory** |

CMS metadata records 97 posts modified in June and 66 in July—163 of 169, or 96.4%, touched across seven weeks. This shows a bulk maintenance pass, but not whether every edit was substantive.

### The strategy has evolved through four stages

1. **Job-led foothold, 2025.** Reminders, unsubscribe, archive, keyboard use, and Superhuman-adjacent topics established a handful of broad Gmail pages.
2. **Exact-action expansion, January 2026.** Ninety shortcut pages attempted to cover individual commands and variants such as action, Gmail, shortcut, Mac/Windows, and tutorial.
3. **Feature-to-query mapping, February–June.** Product releases became search pages for snippets, read receipts, command bar, auto-archive, RSVP, snooze, and other Gmail workflows.
4. **Utility and authority expansion, July.** CMDK added reviews, cost calculators, generators, a search-operator builder, a downloadable shortcut sheet, writing templates, and a proprietary email-statistics page.

The latest phase is the most strategically interesting. CMDK is moving from brute-force topical coverage toward assets with a reason to be chosen or cited.

### Three page types form the current system

#### A. Native-job tutorials

These pages answer a task people already try to perform in Gmail: delete, archive, filter, unsubscribe, enlarge text, find attachments, or set a reminder. The product bridge is adjacent rather than forced:

```text
how Gmail does it → friction or limitation → CMDK shortcut/feature → install
```

This is where almost all current modeled traffic lives.

#### B. Commercial interception

The Superhuman cluster includes alternatives, pricing, reviews, shortcuts, a Chrome-extension query, migration, and a [cost calculator](https://cmdk.email/post/superhuman-cost-calculator/). The calculator turns price comparison into an interactive result and then frames CMDK as the in-Gmail alternative.

This traffic is much more qualified, but the cluster is still small: ten posts produced about 5.318 modeled ETV, 2.8% of CMDK's total. The [`best-gmail-alternatives-superhuman-alternative` comparison](https://cmdk.email/post/best-gmail-alternatives-superhuman-alternative/) contributed only 0.240 ETV in the fresh relevant-pages task, and a same-day live check placed CMDK #27 for `superhuman alternative`.

#### C. Utility and evidence assets

The sitewide footer now groups six “Free Tools”:

- Subject Line Tester;
- Superhuman Cost Calculator;
- Out-of-Office Generator;
- Signature Generator;
- Gmail Search Operators Builder; and
- Shortcuts Cheat Sheet PDF.

The [Gmail search-operator page](https://cmdk.email/post/gmail-search-operators/) contains an in-browser query builder and reference guide. The [email-statistics page](https://cmdk.email/post/email-statistics/) combines cited industry figures with CMDK's aggregate usage data, including 221,610 keyboard actions versus 100,187 mouse actions, 28.7% of activity outside 9–6, and 8,574 snoozes over 90 days. It explains that message content, subjects, and recipients were not analyzed and commits to quarterly refreshes.

These new pages were crawled quickly, but most are days old. They demonstrate a strategy, not established traffic.

## 3. The search-to-install mechanics

CMDK does more than place a generic banner under blog posts.

Across the 169-post corpus:

- 52 posts contain a body-level Chrome Web Store link;
- 45 use a Store URL with `utm_source=blog`;
- 89 contain a related-content block; and
- every page also exposes a global Store install CTA in the header or footer.

The recent pages use article-specific campaigns such as:

```text
utm_source=blog
utm_medium=post
utm_campaign=gmail-search-operators
```

Equivalent campaigns exist for `email-statistics`, `subject-line-tester`, `superhuman-review`, and the mass-delete article. They create a mechanism to attribute **landing page → Store visit** by content intent if the relevant Store analytics are enabled; the tagged URLs alone do not prove CMDK measures the clicks or resulting installs.

The limitation is after the click. Public evidence does not show a reliable join from a Store-first install to activation and payment. UTM links prove attribution design, not conversion performance.

Internal links also favor product-adjacent destinations. In the recent corpus, frequently promoted body destinations include snippets, reminders, cleanup, read receipts, mass delete, archive, command bar, bulk unsubscribe, and Split Inbox. The publication is organized to move a generic Gmail reader toward a capability cluster, not merely to maximize page views.

## 4. Where CMDK has modeled visibility

### Domain footprint

Fresh DataForSEO Labs results for `cmdk.email` were:

| Metric | Result |
| --- | ---: |
| Ranking keywords | 200 |
| Modeled organic ETV/month | 188.529 |
| Modeled traffic value | $691.89 |
| Paid keywords | 0 |
| Positions 1–3 | 0 |
| Positions 4–10 | 6 |
| Positions 11–20 | 24 |
| Positions 21–50 | 114 |
| Positions 51–100 | 56 |

The old `simplehuman.email` domain retained 11 modeled keyword rows and 24.549 ETV. A directional combined view is about 213 ETV/month, but it is not a traffic total: ranking datasets can retain stale and overlapping URLs during a rebrand.

Intent is almost entirely informational:

| Intent | Keywords | Modeled ETV | Share of CMDK ETV |
| --- | ---: | ---: | ---: |
| Informational | 175 | 167.263 | 88.7% |
| Navigational | 10 | 12.994 | 6.9% |
| Transactional | 11 | 6.529 | 3.5% |
| Commercial | 4 | 1.743 | 0.9% |

Of the 200 keyword rows, 199 were non-brand. No ranked query beginning with `cmdk` appeared in the dataset. The homepage had one keyword and 3.283 ETV, only 1.7% of the total. Bare `cmdk` is also polluted by the unrelated React command-menu ecosystem.

### Pages carrying the modeled footprint

| Page/topic | Ranking keywords | Modeled ETV | Relation to the product |
| --- | ---: | ---: | --- |
| [Delete Gmail messages with a key](https://cmdk.email/post/using-delete-key-to-delete-emails-in-gmail/) | 27 | 59.801 | Shortcut-adjacent, broad task |
| [Gmail filters and rules](https://cmdk.email/post/the-complete-guide-to-gmail-filters-and-rules-for-beginners/) | 24 | 35.355 | Native Gmail organization |
| [Bulk unsubscribe](https://cmdk.email/post/bulk-unsubscribe-gmail-the-easy-way/) | 16 | 15.502 | Cleanup feature bridge |
| [Instant Copy](https://cmdk.email/post/introducing-instant-copy-for-gmail-copy-your-emails-in-1-keystroke-to-paste-into-other-tools/) | 4 | 14.336 | Direct feature page |
| [Gmail font size](https://cmdk.email/post/increase-font-size-shortcut-for-gmail-on-mac-windows-tutorial-simplehuman/) | 24 | 12.235 | Generic shortcut/help intent |
| [Gmail reminders](https://cmdk.email/post/gmail-reminders-that-actually-work/) | 13 | 12.140 | Exact CMDK capability |
| [Archive shortcut](https://cmdk.email/post/how-to-archive-in-gmail-using-keyboard/) | 6 | 8.100 | Direct keyboard-speed bridge |
| [Large Gmail attachments](https://cmdk.email/post/how-to-find-and-delete-large-gmail-attachments-in-seconds/) | 28 | 7.434 | Broad cleanup intent |

The top two account for 50.5% of modeled ETV; the top eight account for 87.5%. This is a concentrated article portfolio, not broad category authority.

### Same-day rankings that held up

Live Google US checks are more useful for interpreting the DataForSEO snapshot:

| Query | US monthly volume | Live CMDK position |
| --- | ---: | ---: |
| `archive shortcut gmail` | 170 | #6 |
| `how to set reminder in gmail` | 90 | #9 |
| `where is the remove formatting button in gmail` | 40 | #13 |
| `gmail reminders` | 140 | #14 |
| `superhuman chrome extension` | 110 | #14 |
| `superhuman alternative` | 170 | #27 |
| `cmdk email` | No measurable volume | #1 |

The pattern is consistent: CMDK can surface for an exact, low-volume Gmail action or a narrow competitor phrase. It has not yet earned broad product/category visibility.

## 5. Where CMDK does not rank

CMDK was absent from the first 30 live US results for the following queries:

| Query | US monthly volume | Strategic meaning |
| --- | ---: | --- |
| `how to bulk delete gmail` | 18,100 | Apparent modeled leader did not hold live |
| `email client for gmail` | 6,600 | Large category and purchase demand |
| `gmail read receipts` | 4,400 | Exact CMDK feature |
| `gmail templates` | 3,600 | Exact snippets feature |
| `gmail keyboard shortcuts` | 2,900 | Core positioning |
| `gmail filters` | 2,400 | Head term behind its second-largest page cluster |
| `gmail search` | 1,600 | Broad Gmail job |
| `bulk unsubscribe gmail` | 1,000 | Promoted use case |
| `mass unsubscribe gmail` | 1,000 | Promoted use case |
| `gmail extension` | 480 | Product-category discovery |
| `chrome extensions for gmail` | 390 | Product-category discovery |
| `best email client for gmail` | 170 | Commercial evaluation |
| `gmail unsubscribe extension` | 170 | High product fit |
| `inbox zero gmail` | 170 | Positioning fit |
| `gmail snippets` | 90 | Exact feature |

The result is not simply “low authority.” These SERPs reward different entities:

- Google Help dominates native Gmail functions;
- Chrome Web Store listings dominate extension searches;
- Reddit frequently occupies unresolved-problem and product-selection results;
- established products such as Boomerang, Streak, Missive, Shortwave, Clean Email, Mailbird, and Mimestream rank with focused feature or comparison pages; and
- established editorial domains hold “best” and “alternative” queries.

CMDK's current domain can beat generic publishers on small exact questions, but not yet Google, the Store, strong products, Reddit, and established reviewers on the valuable heads.

### Publishing volume versus visibility

The relevant-page model exposed about 35 ranking posts from a corpus of 169; approximately 134 posts had no modeled visibility.

The January shortcut cohort is the cleanest test of CMDK's high-volume tactic:

- 90 posts published on one day;
- 8 with modeled visibility;
- 17.647 combined ETV, 9.4% of the domain total; and
- two pages—font size and indent more—contributed 92.5% of that cohort's ETV.

The June feature cohort had four visible pages and 1.857 ETV. Five of the 29 July posts had 1.743 ETV, but they are too new for a performance judgment.

The economic signal is nevertheless clear: **mature, broad job pages produce the footprint; page count does not.** Tecotype should not infer that 90 atomized pages are required to build topical relevance.

## 6. Where CMDK likely gains discovery

Public evidence supports a source map, not a source-share estimate.

| Source | Observable evidence | Likely role | What remains unknown |
| --- | --- | --- | --- |
| Chrome Web Store | Featured; 2,000 displayed users; 59 ratings; 4.9 | Persistent discovery, trust, and installation | Impressions, Store search terms, install source, activation, paid conversion |
| Google organic | About 213 combined modeled ETV across old/new domains | The only ongoing website-discovery source found with a public directional estimate; mostly Gmail help | Actual sessions, source share, and downstream conversion |
| Product Hunt | #4 launch; 523 points; 556 followers | Launch burst, social proof, backlinks, newsletter trigger | Users and paid customers by count |
| Andrew Yeung | Personal-use newsletter endorsement | Trusted creator traffic with a documented tail | Clicks, installs, and revenue |
| Nick Lafferty | #1 recommendation in a Superhuman alternatives article; attributed link | Evergreen, high-intent evaluation referral | Commercial relationship and conversions |
| Affiliate/referral | 20% recurring program; 60-day window; optional signature referral | Incentivized creator and user referrals | Active affiliates, clicks, approved sales, retention |
| Community/direct | Small community mentions and likely dark sharing | Trust and incremental discovery | Scale and independence of advocates |

The backlink graph does not prove a large referral engine. DataForSEO observed 1,242 CMDK backlinks from 136 referring domains. Of 131 one-per-domain representative rows, 23 sampled links pointed directly to CMDK and 108 resolved through old-domain redirects. Most sampled destinations were the homepage, the Superhuman-alternative page, and the Inbox Zero page. Raw backlink count is therefore inflated by migration inheritance and sitewide/noisy links.

No paid-search keywords appeared in the snapshot. CMDK exposes Google Ads, Meta, and X measurement cookies, but tag presence does not establish campaign spend or traffic.

### Direct answer to the word-of-mouth question

There is evidence of advocacy and founder-network effects, but not enough to call the business mostly word of mouth. The founder's own account identifies an orchestrated launch, newsletters, backlinks, and ranking lift. The current product adds affiliate tracking and paid recurring commissions. Organic recommendation is one input inside a deliberately amplified system.

## 7. The part Tecotype should reuse

Tecotype's strongest current product-level line is [“Find mail the way you remember it”](./positioning.md). The implemented product includes local full-text search, optional on-device Better search, Gmail and generic IMAP connection, reminders, Split Inboxes, drafts, and sending at varying levels of completeness; the release remains Mac-first and public claims must remain gated by [current product status](./product.md) and the client source.

The SEO wedge should therefore be retrieval, not generic email productivity and not “cheap Superhuman.”

### Reusable page architecture

Each acquisition page should use the same four-part contract:

1. **Solve the searched job honestly.** Give the best provider-native method first.
2. **Name the exact boundary.** Explain when operators or literal words stop helping without exaggerating Gmail's limitations.
3. **Demonstrate Tecotype's distinct resolution.** Use a synthetic inbox to show the remembered description finding a differently worded or differently translated message.
4. **Offer one attributable action.** Send the reader to the normal download path with the content cluster and intent preserved into first useful action and paid conversion.

This copies CMDK's funnel logic while fitting Tecotype's calm, specific voice.

### Initial demand clusters

Fresh US keyword data suggests the following order:

| Cluster/query | Volume | Difficulty | Tecotype role |
| --- | ---: | ---: | --- |
| `gmail search operators` | 720 | 8 | Supporting retrieval hub and interactive comparison |
| `how to find old emails in gmail` | 590 | 0 | Broad, concrete retrieval pain |
| `gmail search not working` | 260 | 0 | Acute failure state and strongest Better-search bridge |
| `gmail advanced search` | 140 | 20 | Supporting operator/reference intent |
| `privacy focused email client` | 390 | 23 | Commercial trust page; distinguish client from provider |
| `email client multiple accounts` | 90 | 11 | Multi-provider workflow page |
| `best email client multiple accounts` | 50 | 22 | Supporting commercial variant |
| `unified inbox` | 170 | 0 | Demand exists but intent is ambiguous; qualify personal desktop use |
| `superhuman alternative` | 170 | 0 | Evidence-led comparison after release facts are stable |
| `best email client for gmail` | 170 | 13 | Later category page |
| `email client for gmail` | 6,600 | 57 | Valuable but too broad and difficult for the first bet |

No measurable volume appeared for `keyboard first email client`, `semantic email search`, `multilingual email search`, `natural language email search`, `search email by meaning`, or `local email search`. Those phrases are useful proof and positioning language, but not evidence for separate acquisition pages.

CMDK did not appear in the first 20 for the tested retrieval cluster. Its search-operator builder was published only on 12 July, so that is an open competitive window rather than evidence the new page has failed.

### First four pages and one asset

#### 1. Retrieval-pain pillar

**Working title:** “Gmail search not finding emails? Find an old message when you only remember part of it.”

Combine the search-failure, old-email, and literal-operator intents in one definitive page. Use decision branches for sender/date/attachment, Spam and Trash, exact operators, and the case where the remembered words differ from the message.

#### 2. Search-operator experience

Do not publish another static cheat sheet. CMDK and many established sites already do that. Build an embedded, synthetic “find this message” comparison:

```text
literal Gmail query: exact operators and remembered words
Tecotype Better search: the description the person naturally remembers
```

The demonstration should connect to no mailbox and send no query or content to Tecotype infrastructure.

#### 3. Multiple-account desktop client page

Address people managing several Gmail and IMAP accounts. Demonstrate unified search and account/provider context only when the current release supports the exact screenshots and flow being claimed.

#### 4. Privacy-focused email-client page

Explain the difference between an email provider and a client, what remains at Gmail/IMAP providers, what Tecotype stores locally, what Better search processes on-device, and which claims Tecotype intentionally does not make. Precision is the differentiator.

#### 5. Shared embedded asset: Better Search playground

Reuse the same small synthetic mailbox across the retrieval pages. Let readers try a literal query, a vague remembered phrase, and a cross-language example. This is an embedded product demonstration, not the separate free search utility rejected in the current [acquisition decision](./next-acquisition-funnel.md).

A second evidence asset can follow: a reproducible retrieval-quality and latency benchmark over a public or synthetic corpus. Publish only verified measurements and methodology. Proprietary aggregate usage data should wait until Tecotype has enough real telemetry and an explicit privacy-safe aggregation method.

### Content topology

```text
retrieval-pain pillar
  ├── search operators / interactive playground
  ├── local search and privacy explanation
  ├── multiple-account search workflow
  └── evidence-led comparison page
             ↓
       normal download path
             ↓
       first successful search
             ↓
            paid
```

One definitive page should own each intent family. Close variants belong as headings and examples, not as dozens of thin URLs.

## 8. Capacity and measurement for Tecotype

CMDK's modeled scale is useful as a reality check. Even if the directional 213 monthly ETV were actual, entirely relevant Tecotype visits—which it is not—then:

- at the current 0.2% generic visitor-to-paid planning rate, it would imply **0.43 paid customers per month**;
- at 0.36%, it would imply **0.77 paid customers per month**; and
- one paid customer per week at 0.2% requires about **2,167 relevant visits per month**.

SEO can support qualified discovery and evidence, but CMDK-sized organic visibility would not solve Tecotype's customer-zero target. It also does not meet this workspace's strict definition of distribution: a partner introducing Tecotype permanently to zero-existing-user audiences with an attributable first-action-to-paid funnel.

### Minimum funnel instrumentation

| Stage | Minimum evidence |
| --- | --- |
| Search | Query, landing page, country, device, impressions, clicks, live rank |
| Page | Entry page, content cluster, CTA impression and click |
| Download | Source/campaign carried through a privacy-safe website-to-app handoff where possible |
| Activation | First useful action, preferably a successful native or Better search—not the query text |
| Commercial | Trial start, first payment, refund, and retention by aggregate source cohort |

Never send mailbox contents, search strings, credentials, or message identifiers into acquisition analytics.

### Suggested experiment boundary

Publish the four-page cluster and embedded playground only after the public site, normal download path, source join, and relevant release claims are ready. Review at 30, 60, and 90 days.

Expand toward 8–12 high-quality pages only when the first set demonstrates both parts of the funnel:

1. qualified non-brand impressions and improving live rankings; and
2. downstream download or activation intent attributable to the cluster.

Do not expand merely because a page earns impressions. As a **proposed internal decision rule**, continue after 90 days only if at least two target families have entered the top 20 and organic visitors have produced attributable download actions. This threshold is a planning choice, not an evidence-derived SEO benchmark; paid conversion is the stronger signal whenever volume is sufficient.

## 9. Strategic boundaries

The CMDK pattern should not pull Tecotype away from its own position.

- Do not pursue broad sales-email templates, subject-line tools, read-receipt demand, or generic Gmail formatting unless a Tecotype capability creates a distinct and honest bridge.
- Do not make low price the category. Tecotype's comparison is calm control, local operation, search, providers, and workflow—not a cheaper imitation.
- Do not auto-append referral text to outgoing mail. If a referral program is ever tested, make it quiet, explicit, and user-initiated.
- Do not manufacture 90 shortcut pages. Consolidate related demand and invest in original demonstrations, screenshots, benchmarks, and refreshes.
- Do not treat Product Hunt, rankings, backlinks, Store users, or affiliate signups as customer evidence without a paid-conversion join.
- Do not describe planned Windows/Linux availability or partially complete workflows as the current release. Verify each public page against the shipping build immediately before publication.

## 10. Method and evidence boundary

This refresh used:

- the public CMDK WordPress corpus and metadata for 169 posts;
- page-level inspection of tutorials, comparisons, tools, CTAs, internal links, and aggregate-data methodology;
- fresh DataForSEO Labs ranked-keyword and relevant-page results for both domains;
- fresh US keyword demand for Tecotype-relevant clusters;
- 33 same-day Google US SERP validations;
- the Chrome Web Store, Product Hunt, founder retrospective, creator article, comparison referral, and affiliate program;
- the prior backlink dataset for direct versus redirected referring domains; and
- Tecotype's [product](./product.md), [positioning](./positioning.md), [current acquisition decision](./next-acquisition-funnel.md), implementation source under `../tecotype`, and the repository's [DataForSEO method](./tools/dataforseo.md).

Fresh DataForSEO work for this strategy refresh cost no more than approximately
**$0.48**. Overlapping calls and rows were deduplicated.

DataForSEO ETV is a model based on ranking, volume, and expected click-through; it is not CMDK analytics. A backlink is not a click, a Store user is not a paid subscriber, an affiliate program is not affiliate performance, and a founder account is not independently audited. Actual traffic share requires CMDK's GA4/Search Console, Chrome Web Store dashboard, affiliate dashboard, product analytics, and payment data.

## Bottom line

CMDK's SEO strategy is **publication SEO for Gmail jobs**, with a product CTA attached to the point where native Gmail becomes inconvenient. The current search footprint is real but small, concentrated, informational, and long-tail. Its most valuable feature and category terms remain weak or invisible. The business's discovery is broader than SEO and broader than word of mouth: launch, creators, Store, search, comparisons, and paid referrals reinforce one another.

Tecotype should reuse the funnel logic around a more defensible wedge:

> **Help someone find the missing message; show why remembered meaning can beat remembered wording; demonstrate it locally; then offer the calm desktop client that does it.**

Four definitive pages, one synthetic Better Search demonstration, and a complete search-to-paid measurement join are a better first move than CMDK's 169-page footprint.
