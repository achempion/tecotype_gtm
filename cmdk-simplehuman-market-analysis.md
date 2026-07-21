# CMDK (formerly Simplehuman) market and customer analysis

**Research date:** 21 July 2026

**Scope:** CMDK, the Gmail browser extension formerly called Simplehuman. This is not the `cmdk` React component library or the simplehuman home-goods company.

**Current product snapshot:** Chrome/Chromium extension for desktop Gmail; 15-day trial; $9 monthly, $79 yearly, or $169 lifetime; Gmail only; no CMDK mobile app.

## Research verdict

CMDK's durable value is a deliberately small replacement surface:

```text
keep Gmail as the source of truth
→ install one browser extension in seconds
→ retain Gmail search, labels, spam filtering, account state, mobile fallback,
  and compatibility with other extensions
→ learn a command bar and faster shortcut grammar
→ triage, split, defer, template, track, and clean up mail
→ reach Inbox Zero without migrating to a new client
```

That loop is commercially meaningful. The public reviews contain repeated former-Superhuman users who say CMDK preserves most of the workflow they valued at a much lower price. Other users are more precise: they do not want a full client at all; they want Gmail to become faster while remaining Gmail.

The evidence does **not** establish a large standalone market, paid retention, or willingness to migrate to a full desktop client. CMDK's public footprint is roughly 1,000–2,000 displayed Chrome users, depending on which current Store surface is observed, with about 60 ratings. Its independent review corpus is small and overwhelmingly positive. The strongest conclusion is therefore narrow:

> CMDK validates willingness among some desktop Gmail power users to pay for a low-risk interaction layer. It does not validate demand for leaving Gmail.

For Tecotype, CMDK is both a competitor and a warning. It can undercut any proposition framed merely as “keyboard shortcuts and Inbox Zero for Gmail.” Tecotype's distinct case must make the additional value of a local working copy, exact and on-device semantic retrieval, true multi-provider control, unified accounts, provider independence, and calm desktop operation legible enough to justify switching.

## Executive summary

### Practical ideal customer

The strongest CMDK fit is a desktop-first Gmail or Google Workspace user who:

- processes enough mail that repeated clicks and navigation feel expensive;
- already wants Inbox Zero, deferred follow-up, reusable replies, or read/open signals;
- likes Gmail's data model and does not want to migrate to a separate client;
- works in Chrome, Edge, Brave, Arc, Opera, or another compatible Chromium browser;
- has used, considered, or priced Superhuman and mainly wants its shortcut-driven processing loop;
- values a lightweight, non-AI-first product and responsive human support;
- may use several Google accounts or other Gmail extensions; and
- is price-sensitive relative to Superhuman, but willing to pay more than Gmail's native free feature set.

Recurring public roles include founders, executives, operators, consultants, salespeople, customer-success professionals, and high-volume personal users. The operating condition is more predictive than title: frequent desktop Gmail use, consequential follow-up, and a willingness to build keyboard muscle memory.

Fit is weak or conditional for Outlook, IMAP, iCloud, Safari, Firefox, mobile-first, true-unified-inbox, enterprise-admin, regulated-industry, delegated-mailbox, shared-inbox, or full-offline requirements.

### Market read

CMDK occupies a small but established category: **paid Gmail augmentation**. The category ranges from calm-interface overlays such as Simplify Gmail, through reminder/tracking tools such as Boomerang and Mailsuite, to CRM and team-workflow layers such as Streak and Gmelius. Public Chrome Store user proxies for adjacent products range from tens of thousands to three million. Those counts show that Gmail can sustain third-party workflow businesses; they do not reveal unique people, paid customers, revenue, retention, or direct substitutability.

The job-level search market is much larger than CMDK's brand demand. A July 2026 US-English DataForSEO snapshot found measurable demand for Gmail read receipts, templates, bulk deletion, keyboard shortcuts, tracking, bulk unsubscribe, and multiple inboxes. CMDK itself had essentially no measurable new-brand search demand; its organic footprint was led by generic Gmail how-to pages. Acquisition is therefore job-led and competitor-led, not brand-led.

### What appears to drive activation and love

1. **No migration:** Gmail remains authoritative and immediately available without the extension.
2. **Fast first value:** install, open Gmail, press Cmd/Ctrl+K.
3. **Learned control:** mouse nudges gradually teach shortcuts rather than requiring a hard workflow reset.
4. **Superhuman familiarity:** the command palette, shortcut grammar, snippets, snooze/reminders, splits, and read receipts resemble the valued part of a premium-client workflow.
5. **Low counter-price:** $79 per year and a $169 lifetime option make the comparison with $300–$396 annual premium clients easy.
6. **Founder-level support:** responsiveness and rapid feature fixes recur unusually often in reviews.
7. **Reversibility:** if CMDK fails, is removed, or is unavailable on mobile, the user's ordinary Gmail remains intact.

### Structural limits

- Gmail and Chromium only; no Outlook, IMAP, native desktop client, or mobile feature layer.
- Account switching is not a true aggregated unified inbox or native cross-account search.
- Dependence on Gmail's rendered interface creates breakage and maintenance risk when Google changes markup or behavior.
- Gmail already supplies many basic shortcuts, snooze, templates, search, labels, multiple inboxes, spam handling, mobile access, and increasingly Gemini.
- Point solutions can reproduce individual CMDK outcomes, sometimes free or at a lower price.
- Public scale, paid conversion, cohort retention, refund rate, and revenue are unknown.
- A founder-led micro-team profile creates support strength but also key-person and continuity risk.
- Privacy, pricing, and product documents conflict in ways that weaken enterprise trust.

---

## 1. Scope, method, and evidence quality

### Identity correction

[Simplehuman became CMDK on 6 April 2026](https://cmdk.email/post/simplehuman-is-now-called-cmdk/) after both the simplehuman home-goods company and Superhuman contacted the maker about the name. The vendor says the account, team, product, settings, and data were unchanged. Simplehuman and CMDK are therefore one product history, not two competitors.

The old name still appears in review archives, email addresses, Notion documentation, indexed pages, and Chrome metadata. The new name also collides with the well-known `cmdk` developer-library term. Both names create search ambiguity, so brand-query totals require manual inspection.

### Research approach

The analysis combined:

- current official product, pricing, affiliate, release, privacy, legal, and feature pages;
- direct interactive inspection of the Chrome Web Store listing and all 55 English written reviews exposed by its review drawer;
- Product Hunt, G2, LinkedIn, Chrome Store, and first-person open-web sources;
- founder-authored acquisition retrospectives, kept separate from independent demand evidence;
- current official Gmail documentation to establish the free/native substitute set;
- current competitor product, pricing, and Chrome Store pages;
- DataForSEO US-English keyword, ranked-keyword, and page visibility snapshots;
- a community-source independence audit to separate repeated promotion from independent customer accounts; and
- direct inspection of Tecotype's product, positioning, architecture, release, and implementation state.

### Source hierarchy

| Evidence tier | Best sources | Used for | Main limitation |
| --- | --- | --- | --- |
| Current primary | CMDK site, Chrome Store, disclosures, terms, release log | Product, price, permissions, current claims | Vendor-authored and internally inconsistent |
| Direct customer | Chrome written reviews, one G2 review, Product Hunt reviews | Jobs, outcomes, switching, support, objections | Small, self-selected, activation-biased |
| Vendor operational | CMDK aggregate usage post, founder acquisition posts | Usage mechanism and acquisition hypotheses | No independent audit or paid-user denominator |
| Independent ecosystem | Gmail docs, competitor stores/pricing, market documentation | Substitute set and category context | Install buckets are not customers or revenue |
| Community discussion | Reddit and similar first-person threads | Deep context only after identity/promotion checks | Anonymous and highly promotion-contaminated |
| Modeled discovery | DataForSEO | Relative query and page opportunity | Modeled estimates, not visits, people, or TAM |

### Review-surface inventory

| Surface | July 2026 snapshot | Treatment |
| --- | ---: | --- |
| [Chrome Web Store](https://chromewebstore.google.com/detail/cmdk-read-receipts-split/nipfocapamlefjhldhcagammlldbangf?hl=en-US) | 4.9/5; about 59–60 ratings; public surfaces showed 1,000–2,000 users | Primary current footprint and richest direct review corpus |
| Chrome English written-review drawer | 55 written reviews; 53 five-star, one 3-star, one 1-star | All visible entries inspected; useful for failure modes, not prevalence |
| [Product Hunt](https://www.producthunt.com/products/simplehuman) | #4 product of the day on 6 February 2025; roughly 523–528 points, 556 followers, two 5/5 reviews | Launch and founder-network context; tiny, positive-selection sample |
| [G2](https://www.g2.com/products/simplehuman/reviews) | One 5/5 review | A single validated small-business user; review was incentivized via G2 invite |
| Official homepage testimonials | “4.9/5 from 1000+” wording and a wall of love | Vendor-selected social proof, not an independent rating corpus |
| LinkedIn/company pages | Self-owned, size-one company profile; founder retrospectives | Company and acquisition context, not customer census |
| Reddit | Several apparent recommendations | Only independently attributable accounts retained; repeated seeded comments excluded |

The Chrome Store count discrepancy is real. A direct interactive 21 July view showed version 60.3.0, updated 17 July, 60 ratings, and 1,000 displayed users. Google's text/index surfaces returned v60.1.x snapshots dated 2–11 July with 59 ratings and 2,000 users during the same research session. Chrome says ratings update daily, and install counts are rounded. This report uses a **1,000–2,000 public-store range**, not a false point estimate.

Google's Chrome Enterprise documentation calls the corresponding public field “Number of active users.” It should therefore not be called cumulative downloads. It is still a platform-defined, rounded/cached measure and says nothing about Gmail usage frequency, trial status, payment, or retention.

The visible written-review distribution is exceptionally positive: 53 of 55 were five-star. That establishes love among reviewers, not the satisfaction of all installers. There were no visible two- or four-star written reviews, and users who uninstall without reviewing are absent.

### Inspection and independence corrections

- The English review drawer was expanded until all 55 written reviews loaded; dates ranged from July 2021 to July 2026.
- Repeated Reddit recommendations from one seven-year-old account were initially easy to mistake for several independent users. Its visible history contained four tightly clustered 2026 Simplehuman/CMDK recommendations among only six visible comments. Those posts were excluded as independent demand evidence and treated only as possible manual community seeding.
- Homepage testimonials that reproduce Chrome reviews were not counted again.
- Product Hunt's 2025 “launch” date does not establish product inception; Chrome reviews reach back to 2021 and the company profile says founded in 2022. The safest interpretation is public/Product Hunt launch after a longer beta history.
- Vendor comparisons claiming a percentage of Superhuman replacement, regulated-industry suitability, or savings were not treated as independently demonstrated outcomes.
- No public paid-customer count, revenue, funding round, retention cohort, churn rate, or refund rate was located.

### DataForSEO audit

Two parallel focused Google US-English passes cost approximately $0.30 combined. They overlapped, one included a duplicated overview task, and their rows were not added together. The results were used directionally. Search volume is modeled; organic ETV is modeled traffic, not analytics; CPC indicates advertiser competition, not CMDK's CAC or willingness to pay.

Confidence labels in this report mean:

- **High:** current explicit product fact or repeated across materially different evidence types.
- **Medium-high:** repeated direct-user pattern in the small corpus with a clear consequence.
- **Medium:** several accounts or one strong source, but unknown incidence.
- **Low / warning:** plausible and consequential, but tiny, conflicted, or vendor-selected evidence.

---

## 2. Current product and company snapshot

### What the product is

CMDK is a Chrome/Chromium extension that changes Gmail's interface and interaction layer. It is not a replacement mail service and does not present itself as a full native email client.

Current official surfaces describe:

- a Cmd/Ctrl+K command bar for Gmail actions;
- 25+ additional hotkeys, with broader metadata elsewhere saying 80+ or 100+;
- shortcut-learning nudges after mouse actions;
- search- or label-defined Tabs described as a split inbox;
- natural-language snooze and reminders;
- Send & Remind / follow-up reminders;
- one-click “Nuke” blocking and deletion for unwanted senders;
- invisible-pixel read receipts with open and re-open status;
- reusable rich-text snippets with variables, placeholders, CC/BCC, Send Guard, and reminder/receipt automation;
- quick switching between Google accounts;
- quick quote, instant copy, paste-as-link, appearance controls, and smart actions; and
- compatibility with other Gmail extensions.

The homepage says it is available for Mac, Windows, and Linux. That means the browser extension can run on those desktop operating systems; it is not evidence of native apps for each platform. The current pricing FAQ says there is no mobile app.

A residual [Microsoft Edge Add-ons listing](https://microsoftedge.microsoft.com/addons/detail/lpbhllollfalncekepkkdcihoadgilib) remained under the Simplehuman name with an old version and one displayed user. It is better treated as stale residue than evidence of an active second-store channel. No maintained Firefox listing or Google Workspace Marketplace product surfaced.

### Product-state contradictions

The site is actively changing, and not all pages agree:

| Topic | Current evidence | Interpretation |
| --- | --- | --- |
| Shortcut count | Homepage body says 25+; page title says 80+; one comparison says 100+ | Do not publish a precise total without a maintained inventory |
| Snippets | Homepage, Store, and dedicated page say shipped; pricing still says “Coming soon” | Pricing copy is stale |
| Starting price | Current checkout page says $9 monthly / $79 yearly; Store says plans start at $5/month | Store copy is stale or refers to an undisclosed/effective annual rate |
| Store footprint | Direct Store UI and indexed text differed on version, date, ratings, and user bucket | Counts are dynamic and surfaces are not synchronized |
| Release log | Notion log stops at v50.3.1 on 12 May; Store was already v60.x in July | Product is active, but public change documentation is incomplete |
| Local/no server | Disclosure says every feature works without server or internet; read receipts record remote opens and snippets sync between devices | The blanket statement cannot be literally correct |
| “Bulk unsubscribe” / Nuke | The [SEO page](https://www.simplehuman.email/bulk-unsubscribe-gmail/) calls the job bulk unsubscribe, but its mechanics are sender blocking plus deletion; Google says blocking does not unsubscribe from a mailing list | Treat it as instant cleanup/suppression, not standards-based list removal |
| Referral branding | The [Store](https://chromewebstore.google.com/detail/cmdk-read-receipts-split/nipfocapamlefjhldhcagammlldbangf?hl=en-US) says receipt-enabled emails get the user's referral link, while the [receipt page](https://www.simplehuman.email/read-receipts/) says no CMDK branding appears unless the sender opts in | The mechanic exists, but public sources do not establish whether it is added by default or only after sender opt-in; exposure and conversion are unknown |
| Trial | Pricing says 15 days; 2023 terms say 14 days | Legal document is stale |

These inconsistencies do not show that the product is fraudulent. They show that current public documentation is not reliable enough for procurement-sensitive or privacy-sensitive claims without direct clarification.

### Company and maturity

Public evidence points to a founder-led micro-team:

- FutureWave is the legal entity named in the 2023 privacy policy and terms, with an Indian VAT number and Mysore address.
- The current LinkedIn company profile describes CMDK as self-owned, founded in 2022, and company size one, while also associating two profiles with the company.
- Founder Phalgun Guduthur describes building the prototype on weekends, later monetizing it, and operating the Product Hunt launch with friends and newsletter support.
- In a December 2023 founder post, he said the product had reached first revenue and its best month was helping pay rent. That confirms pre-Product-Hunt monetization, but provides no amount, margin, or retention evidence.
- Product Hunt launch material describes a one-person operation and says the first version was built with a friend; current involvement by that collaborator is unclear.
- No public institutional funding announcement surfaced in this research. That is an absence of evidence, not proof of bootstrapping.
- Store reviews since 2021 and frequent 2026 releases indicate a longer-lived, actively maintained product rather than a newly launched prototype.

The founder-led model is part of the current experience. Reviewers repeatedly praise direct, fast support and feature responsiveness. The same profile creates concentration risk around Gmail breakage, support load, compliance, and product continuity.

### Public timeline

| Date | Observable event | What it means |
| --- | --- | --- |
| 2021 | Chrome listing/reviews begin | Product history predates the later formal launch |
| 2022 | LinkedIn founding year | Company self-description; not independently incorporated-date proof |
| Dec 2023 | Founder describes first revenue and best month helping pay rent | Early monetization, no scale disclosed |
| Sep–Nov 2024 | Usage analytics introduced; Google login later ties events to email | Product learning becomes account-linked telemetry |
| 6 Feb 2025 | #4 Product Hunt launch | Formal awareness/backlink event, not product inception |
| Oct 2025 | Active inbox email checked for Tabs/multiple accounts | Account metadata scope expands with product functionality |
| 6 Apr 2026 | Simplehuman renamed CMDK | Legal/brand reset; product continuity |
| May 2026 | Affiliate and referral signature added | Customer/recipient acquisition loop becomes part of product |
| Jul 2026 | Store v60.x and vendor usage dataset published | Active shipping and enough event volume to study behavior |

---

## 3. Customer segments and jobs

### Segment map

| Segment | Trigger and core job | Why CMDK fits | What breaks fit |
| --- | --- | --- | --- |
| Superhuman price refugee | Wants the learned fast-processing loop without $300+ annual spend | Familiar command/shortcut/snooze/snippet grammar inside Gmail | Needs full client polish, mobile parity, AI, CRM, or true unified accounts |
| Gmail-preserving power user | Likes Gmail and other extensions; wants less mouse work | Zero migration, reversible, native Gmail remains available | Native shortcuts or a cheaper overlay are sufficient |
| High-volume operator | Processes sales, customer, founder, or consulting mail with costly delays | Fast triage, reminders, snippets, receipts, account switching | Reliability or extension conflicts add verification work |
| Inbox-zero personal user | Wants newsletters and obligations converted into a finite queue | Tabs, Nuke, snooze, one-key archive/delete | Price exceeds personal value; mobile is primary |
| Multi-Google-account user | Repeatedly switches among work and personal Gmail identities | Hotkey account switching and unlimited inbox licensing | Expects aggregated mail or global cross-account search |
| AI-averse minimalist | Wants speed and calm without a cloud AI reading mail | Local/browser framing, human support, hide-Gemini controls | Analytics, receipt tracking, and imprecise privacy copy weaken trust |
| Sales / outreach user | Wants open status, reusable messages, automatic CC/BCC, follow-up | Receipts, snippets, reminders, referral-compatible workflow | Needs CRM depth, team admin, deliverability controls, or compliance |
| Team / regulated buyer | Needs provisioning, DPA, SSO, audit, shared state, policy assurance | Very little public evidence of fit | Current terms, no visible SOC 2/DPA, Gmail-only architecture, solo operation |

### Jobs to be done

Customers appear to hire CMDK to:

- process a long Gmail inbox without repeated pointing and clicking;
- keep Gmail's familiarity and state while borrowing Superhuman's interaction grammar;
- make the inbox feel like a deterministic work queue;
- postpone an obligation and trust it will return;
- follow up when a sent message receives no response;
- reuse polished replies without leaving compose;
- know whether an important message was opened;
- separate projects, roles, or categories into keyboard-addressable views;
- remove thousands of old marketing messages quickly;
- move among several Google accounts without tab hunting;
- learn Gmail shortcuts gradually through contextual coaching;
- avoid a premium-client subscription and migration; and
- hide Gmail/Gemini interface elements that feel noisy.

### The emotional job

The desired feeling is not raw speed alone. Reviews describe getting out of email, feeling able to reach Inbox Zero, and no longer experiencing Gmail as clunky. The command bar and nudges turn a large interface into a smaller set of predictable actions. The emotional outcome is control with low commitment: the user can rely on Gmail underneath.

This is close to Tecotype's calm-control territory, but CMDK reaches it through **preservation** rather than **replacement**.

---

## 4. What customers value

Themes are ordered by repeated direct evidence and decision impact, not estimated prevalence.

| Rank | Value | Confidence | Why it matters |
| ---: | --- | --- | --- |
| 1 | Gmail continuity and no migration | High | Removes setup, data-model, fallback, and trust barriers |
| 2 | Keyboard and command-bar processing loop | High | Makes common actions immediate and learnable |
| 3 | Price relative to Superhuman | High | Simple comparison for former or aspiring premium-client users |
| 4 | Human, founder-level support | High in review corpus | Resolves extension breakage and makes users feel heard |
| 5 | Inbox Zero and faster triage | Medium-high | Converts subjective speed into a completed-work outcome |
| 6 | Snooze, reminders, and follow-up | Medium-high | Keeps sent and received obligations from disappearing |
| 7 | Split Tabs and navigation | Medium | Creates stable project/category queues inside Gmail |
| 8 | Nuke / bulk sender cleanup | Medium | Delivers dramatic first-session relief for overloaded personal inboxes |
| 9 | Snippets and compose automation | Medium, current | Removes repeated writing and sales/support setup actions |
| 10 | Read receipts | Segment-high | Valuable to sales, vendors, recruiting, and consequential follow-up |
| 11 | Lightweight, non-AI-first framing | Medium-high | Appeals to users rejecting AI cost, opacity, or interface clutter |
| 12 | Coexistence with other extensions | Medium-high | Lets Gmail remain a modular personal stack rather than a forced suite |

Nuke deserves a narrower interpretation than its search-facing “bulk unsubscribe” label. [CMDK's own instructions](https://cmdk.email/learn-to-use/) say it blocks the chosen sender and deletes that sender's existing mail; it can also target a company domain. It does not claim to send a `List-Unsubscribe` request. [Google's documentation](https://support.google.com/mail/answer/15621070?hl=en) explicitly distinguishes the two: blocking routes future messages to Spam but does not remove the recipient from the sender's mailing list. The product still solves a real cleanup job—often more dramatically because old mail disappears—but it is suppression, not confirmed subscription cancellation. This conclusion applies specifically to Nuke; CMDK separately advertises an unsubscribe Smart Action whose mechanism was not verified, so this research does not establish that CMDK lacks every standards-based unsubscribe path.

### Gmail continuity is the strongest adoption advantage

The strongest review language is not “this is a better email client.” It is closer to:

- the user still lives in Gmail;
- their existing extensions continue to work;
- their inbox remains available on mobile;
- if CMDK fails, ordinary Gmail remains usable;
- there is no import, reindexing period, or new source of truth; and
- the user gets the speed layer without accepting a complete product worldview.

This makes switching **into** CMDK unusually cheap and switching **away** unusually safe. A full client's benefit must exceed both the subscription price and this reversibility advantage.

### Support is part of the product

Responsive support appears across old and recent reviews, language requests, bug reports, and feature suggestions. One Product Hunt reviewer reported requested shortcuts shipping during roughly six weeks of use. This is selected evidence, but the recurrence is too strong to ignore.

The retention mechanism may be relational as well as functional: users forgive an overlay bug when the maker responds immediately. That is hard to scale and easy for a larger product to lose.

### Vendor-reported usage data

A 16 July 2026 CMDK article disclosed aggregate product telemetry over a recent 30-day window:

- 221,610 shortcut actions versus 100,187 mouse actions, a 68.9% keyboard share by volume;
- about one quarter of users reportedly performing at least three quarters of Gmail actions by keyboard;
- 28.7% of normalized activity outside 09:00–18:00 local time;
- 8,574 snoozed emails over 90 days, with tomorrow and Monday common destinations.

This is stronger than a generic productivity claim because it shows repeated feature use. It remains vendor-reported, omits a unique-user and paid-user denominator, and cannot establish retention or causal time savings. The methodology says cohort sizes are stated with each statistic, but the published sections do not provide those cohort counts; event deduplication is not user deduplication. The article also confirms that account-linked usage telemetry is operationally important to CMDK.

### What the public review corpus actually establishes

The 55-review direct Store audit and a separate coding pass over 38 unique mirrored review texts overlap and are not additive. In the mirrored set, 16 of 38 explicitly named Superhuman or its price anchor, and roughly 12 praised the founder, support, or rapid feature shipping. That makes two themes unusually well supported for such a small product:

1. CMDK is bought and evaluated in a Superhuman-defined comparison frame.
2. High-touch support is part of the perceived product value, not incidental service.

The direct Store corpus adds repeated accounts of Inbox Zero, faster processing, keeping native Gmail and other extensions, and returning after a trial because ordinary Gmail felt slow. Individual reviewers describe hundreds of daily messages, thousands of messages cleaned up, or years of continued use. Those are self-reported examples, not a typical-use distribution.

The two Product Hunt reviews add one early-user endorsement and one approximately six-week account that reports more frequent Inbox Zero, easier handling of time-sensitive mail, intuitive shortcuts, and four requested shortcuts being implemented. G2 adds one validated consulting user who reports daily time savings, simple setup, a light touch, and strong support—but the review was incentivized through a G2 invite, and G2 explicitly says one review is insufficient for buying insight.

There is no corresponding public corpus of churned or refunded users. The review evidence is therefore strong for describing **why activated advocates love CMDK**, weak for estimating how often people activate, and nearly silent about retention and churn.

---

## 5. What customers reject or cannot get

| Failure or limit | Confidence | Consequence |
| --- | --- | --- |
| Gmail/Chromium-only product boundary | High | Outlook, IMAP, iCloud, Safari, Firefox, and mobile workflows remain elsewhere |
| No true unified inbox or cross-account search | High | Multi-account users still switch contexts |
| Price versus Gmail or cheaper overlays | High | Native shortcuts or Simplify's lower price may be “good enough” |
| Occasional slowness or extension breakage | Medium | A speed product loses its core promise; Gmail fallback limits damage |
| Learning curve / too many shortcuts | Medium | Users must persist long enough for muscle memory to form |
| Trial and pricing disclosure distrust | Medium-high, small corpus | A reasonable price can still lose the sale if the paywall feels hidden |
| Privacy-document precision | High as document fact | Can slow or block security-sensitive or procurement-led adoption |
| No mobile feature parity | High | Desktop behavior does not travel; Gmail mobile becomes a separate workflow |
| No team/admin/compliance package found | Medium-high | Hard to standardize in larger organizations |
| Founder-led micro-team continuity and support capacity | Medium as structural risk | High-touch advantage may become a bottleneck |
| Gmail DOM/interface dependency | High as architecture | Google changes can cause recurring breakage and urgent updates |

### Negative reviews and trust repair

The visible Chrome corpus contains one 1-star and one 3-star written review.

- A March 2025 reviewer believed the listing implied a free product or free plan, then discovered the product was paid and removed it.
- A second reviewer initially rated one star, later changed to three after the developer clarified the description, and said the price itself was reasonable but the original presentation damaged trust.

Current surfaces now prominently state a 15-day no-card trial. This looks like a repaired activation problem, not a current claim that CMDK is free. It is still strategically important: a small product asking for access inside Gmail cannot afford ambiguity at the first payment boundary.

### Performance and platform requests

One recent reviewer described CMDK as a little slow on PC. Other reviews ask for mobile, Safari, or Outlook. These are not enough to estimate defect incidence, but they align with structural limits rather than isolated feature requests.

### Read-receipt ethics

CMDK markets invisible tracking as an advantage: the recipient receives no confirmation prompt and may not know they are being tracked. That creates a privacy asymmetry. A sender can choose CMDK partly for privacy from mailbox-content processing while imposing silent engagement tracking on recipients.

This is commercially valuable to sales and outreach segments, but it is not aligned automatically with a calm, predictable, recipient-respecting product philosophy. For Tecotype, read receipts should not be treated as table-stakes for every user merely because they recur in premium email tools.

An “open” also does not prove that a person read the message. Image blocking can suppress the event, while proxies, security scanners, prefetching, and [Apple Mail Privacy Protection](https://support.apple.com/en-gb/guide/mail/mlhlp1205/16.0/mac/26) can load remote content without a human reading it. The feature is an engagement signal with known false positives and negatives, not a reliable receipt.

---

## 6. Privacy, security, and trust

### What can be claimed defensibly

CMDK says it does not read or store email content and does not request Gmail API read/write access. Its core interaction layer operates in the browser against Gmail's interface. That is materially different from a cloud client that imports and indexes the mailbox.

The defensible formulation is:

> CMDK says message content remains in Gmail/the browser, while account identifiers, product-usage events, errors, snippet data, and read-receipt events involve remote services.

It is not defensible to compress that into “no data leaves the device” or “all features work offline.”

### Current disclosed remote data flow

The [March 2026 data disclosure](https://simplehuman.notion.site/Data-Collection-Disclosures-78ef0e5a5d244312a48afb1f05cc7bb2) says:

- a CMDK account requires an email address;
- feature-use and error events are tracked;
- Tabs, read receipts, and account switching inspect which Gmail inbox is active;
- Google login stores the user's email and tags events to that email; and
- multiple inbox email addresses are checked/stored to show the correct Tabs.

The [2023 privacy policy](https://cmdk.email/privacy/) additionally describes IP, device, browser, usage, log, feature, Google-login, Mixpanel, Stripe, and possible business-transfer processing. It is broad and stale, but it prevents a zero-telemetry interpretation.

The current website cookie panel separately lists Google Analytics, Mixpanel, Affonso, Meta, Google Ads, X, and Vimeo categories. That shows a web-acquisition measurement stack, not that every service runs inside the extension or can access mail; site telemetry and extension/mailbox data flow should not be conflated.

The current Chrome listing discloses handling “User activity.” That category is broad; it does not prove CMDK records every keystroke or email action beyond the product events it describes.

The Store's [Featured badge](https://developer.chrome.com/docs/webstore/discovery) is a positive trust signal: Chrome says staff manually evaluate technical best practices, user experience, design, listing quality, and respect for user privacy. It is not a penetration test, independent security audit, SOC 2 report, or regulatory certification.

### Claims that cannot be reconciled literally

The data disclosure says all features fully work in the browser “without the need for a server or the internet.” Current feature pages say:

- [read receipts](https://cmdk.email/read-receipts/) embed a 1×1 pixel, record timestamp/count, and produce notifications even while Gmail is closed; and
- [snippets](https://cmdk.email/snippets/) are stored in the user's account and synchronized across devices.

Those functions necessarily require remote state or delivery. Message content may remain private while the feature metadata travels; the problem is overbroad documentation, not proof that message bodies are uploaded.

### Legal and procurement gaps

The current Terms and Privacy pages are dated 5 September 2023 and still use the old domain/legal framing. The terms:

- say the trial is 14 days while current pricing says 15;
- prohibit users from transmitting 1×1 pixels or similar passive collection mechanisms even though read receipts are a marketed product feature; and
- explicitly say the service is not tailored for HIPAA, FISMA, or GLBA use.

A current CMDK comparison article claims suitability for regulated industries, which conflicts with those terms. No public SOC 2 report, DPA, enterprise security page, independent audit, SSO/admin documentation, or regulated-industry package was found.

The Chrome Store also labels the developer a “non-trader” and warns EU buyers that consumer rights do not apply to contracts between them and this developer. That is a store/legal status disclosure, not a judgment about product quality, but it further limits an enterprise-grade reading of the listing.

Conclusion: CMDK has a plausible, vendor-claimed message-content privacy distinction for individual users, but the public evidence does not verify that architecture independently or support high-trust enterprise assurance.

---

## 7. Pricing and business model

### Current public price

| Plan | Price | Notes |
| --- | ---: | --- |
| Monthly | $9/month | Positioned as a longer trial path |
| Yearly | $79/year | About $6.58/month equivalent |
| Lifetime | $169 once | Currently shown discounted from $199 |

All plans are presented as including unlimited inboxes and the common feature set. The lifetime card also invokes a “generous fair usage policy” without defining its limits. The trial is 15 days with no card; the pricing FAQ promises a 30-day no-questions refund. Stripe manages payment and cancellation.

The lifetime offer is strategically important. CMDK says local/browser operation gives it negligible running cost. The offer lowers subscription resistance and anchors the product as a durable utility rather than an evolving cloud service. It also shifts sustainability risk to the buyer: long-lived Gmail maintenance, read-receipt delivery, sync, analytics, and support are not literally costless.

The 2023 terms reserve the right to modify, suspend, or discontinue the service and do not define a perpetual-service guarantee for “lifetime.” The safest interpretation is a current one-time commercial offer, not an enforceable promise that every present feature and remote dependency will operate forever.

### Competitive anchors

| Option | Current price signal | What the customer is buying |
| --- | ---: | --- |
| Gmail native | Free for consumer Gmail; bundled with Workspace | Provider-native mail, shortcuts, search, snooze, templates, multiple inboxes, mobile, Gemini depending on plan |
| [Simplify Gmail](https://simpl.fyi/plans) | $2/month billed annually for an individual | Calm Gmail redesign, bundles, saved search, pause, tracker blocking, shortcuts, privacy |
| [Boomerang Personal](https://www.boomeranggmail.com/subscriptions.html) | Free Basic; $4.98/month billed annually | Send later, reminders, response tracking, receipts, pause, scheduling |
| [Mailsuite](https://mailsuite.com/en/pricing) | Free tracking tier; €9.99/user/month Advanced on the observed page | Tracking, reminders, templates, CRM/outreach, mobile and Outlook surfaces |
| CMDK | $79/year or $169 lifetime | Superhuman-like interaction layer, reminders, receipts, snippets, cleanup |
| [Superhuman Mail Starter](https://help.superhuman.com/hc/en-us/articles/46005733349517-Pricing-Plans) | $300/year or $30 monthly | Full premium client and team/AI features |
| Superhuman Mail Business | $396/year or $40 monthly | Advanced AI, CRM integrations, opens feed, team/business features |
| Tecotype (working offer; Mac-first) | €149/year or €15 monthly | Local-first desktop client under active development; Gmail and generic IMAP sync, local search, and unified views; broader rollout and parts of sending UX remain incomplete |

CMDK's $79 annual price is low relative to full premium clients but high relative to Gmail and Simplify. It must sell the complete shortcut/reminder/snippet/receipt loop, not keyboard shortcuts alone.

A modular Simplify-plus-Boomerang-Personal stack costs roughly $84 per year before tax at current annual rates—almost the same as CMDK—and covers much of the calm-interface, shortcut, reminder, scheduling, and receipt territory. CMDK's advantage is one coherent layer and one support relationship; modular alternatives let users choose a stronger specialist or a free tier.

For Tecotype, price cannot carry a “faster Gmail” comparison. CMDK's entire lifetime price is close to one Tecotype annual term in numerical magnitude before currency conversion. The case for Tecotype must be a different, larger job.

### Revenue boundaries

No defensible revenue estimate is possible from the public data.

- Chrome “users” are a rounded active-install-style platform measure, not paid accounts.
- A 15-day trial means some visible users are unpaid.
- Lifetime, annual, monthly, discounts, refunds, churn, and historical prices create unknown mix.
- One account can use unlimited inboxes and multiple devices.
- Reviewers may remain visible after uninstalling.

Multiplying Store users by list price would create false precision and is not done here.

---

## 8. Demand and market boundaries

### Brand demand is tiny

The DataForSEO snapshot found:

- no measurable volume for “CMDK email” in the selected US-English keyword view;
- about 40 modeled monthly searches for “simplehuman email”;
- about 170 for “Simplify Gmail”;
- about 390 for “Boomerang Gmail”; and
- about 5,400 for “Superhuman email.”

The bare term “cmdk” has developer-library ambiguity and cannot be attributed to this product. The old Simplehuman name collides with home goods. Rebranding solved a legal/identity problem but did not create a clean high-intent brand query.

### Job demand is larger

Selected modeled US monthly search volumes:

| Query family | Approximate monthly volume | Interpretation |
| --- | ---: | --- |
| Gmail read receipts | 4,400 | Large outcome category, crowded and often free |
| Gmail templates | 3,600 | Reusable reply demand, native and add-on substitutes |
| Bulk delete Gmail | 3,600 | Strong pain, often episodic rather than subscription-retentive |
| Gmail keyboard shortcuts | 2,900 | Large learning demand; much is solved natively |
| Gmail tracker | 2,400 | Sales/outreach intent; privacy-sensitive |
| Bulk unsubscribe Gmail | 1,000 | Cleanup job; potentially acquisition-heavy, retention-light |
| Gmail multiple inboxes | 480 | Organization job; native terminology creates ambiguity |
| Superhuman alternative | 170; CPC about $13.35 | Small but commercially valuable competitor-displacement query |
| Gmail reminder extension | 40 | Narrow explicit add-on query |
| Gmail split inbox | 20 | Product vocabulary is not a large search category |

These terms overlap and are not unique people. They show discoverable jobs, not an 18,610-person serviceable market.

### CMDK's organic footprint

DataForSEO modeled approximately:

- 200 ranking organic keywords;
- 188.5 monthly organic ETV;
- about $692 in modeled paid-traffic value; and
- zero paid keywords.

Generic Gmail how-to posts dominated. “How to bulk delete Gmail,” “bulk delete Gmail,” and “how to create rules in Gmail” were among the strongest pages/queries. The homepage accounted for only a small share of modeled visibility. Comparison and brand pages were much smaller.

The correct conclusion is that CMDK is building an early content-acquisition surface around existing Gmail jobs. It is not evidence of meaningful brand demand or a new named category.

A separate backlink pass found roughly 1,242 indexed links from 136 domains, with substantial directory/spam noise alongside legitimate links from the Chrome Store, Product Hunt, G2, AlternativeTo, newsletters, blogs, and productivity-stack posts. The founder credits Product Hunt and newsletter backlinks with better search visibility. Backlink volume is not customer evidence; it does help explain how a tiny brand began ranking for generic Gmail jobs.

### Category-scale proxies

| Product | July 2026 Chrome Store proxy | Primary job |
| --- | ---: | --- |
| CMDK | 1,000–2,000 users; 59–60 ratings | Broad Superhuman-like Gmail speed layer |
| [Simplify Gmail](https://chromewebstore.google.com/detail/simplify-gmail/pbmlfaiicoikhdbjagjbglnbfcbcojpj?hl=en) | 40,000 users; 626 ratings | Calm interface, privacy, bundles, pause, shortcuts |
| [Boomerang for Gmail](https://chromewebstore.google.com/detail/boomerang-for-gmail/mdanidgdpmkimeiiojknlnekblgmpdll/details) | 800,000 users; about 2,100 ratings | Send later, reminders, response tracking, scheduling |
| [Streak CRM](https://chromewebstore.google.com/detail/streak-crm-for-gmail/pnnfemgpilpdaojpnkjdgfgbnnjojfik?hl=en) | 600,000 users; about 6,500 ratings | CRM and sales workflow inside Gmail |
| [Mailsuite/Mailtrack](https://chromewebstore.google.com/detail/email-tracker-by-mailtrac/ndnaehgpjlnokgebbaldlmgkapkpjkkb?hl=en-US) | 3,000,000 Store users; about 11,700 ratings | Email-open tracking |
| [Gmail Tabs by cloudHQ](https://chromewebstore.google.com/detail/gmail-tabs-by-cloudhq/ckoglchhifaedlfjhnoaebnloipiepjg?hl=en) | 30,000 users; about 152 ratings | Search/label-defined Gmail tabs |
| [Inbox Zero Tabs](https://chromewebstore.google.com/detail/inbox-zero-tabs-for-gmail/iencpoofingkkakccoknbleilcliokfk) | About 1,000 users | Free local tabs, Cmd+K, hotkeys, per-account settings |
| [Inbox Keys](https://chromewebstore.google.com/detail/inbox-keys-gmail-command/bfcdnkjplofjddlecpojhpoomdialafa) | 11 users; 6 ratings shortly after 13 July 2026 launch | Free/open-source command bar, hotkeys, split tabs, remapping |

The embedded-Gmail category is real and much larger than CMDK. The table does not mean every user would buy CMDK or Tecotype. Each product serves a different job, free tiers distort installed bases, and Store buckets are not unique paid people.

Inbox Keys is strategically useful despite its tiny launch footprint. Its free MIT-licensed extension reproduces CMDK's central command-bar, shortcut, search-tab, and account-switching wedge with local storage and no stated analytics. The public repository showed more than 20 commits but zero stars and forks, so this is evidence of technical reproducibility—not adoption or a maintained competitive business. Its own documentation also acknowledges Gmail-DOM fragility, English-label limits, Gmail/Calendar host access, local inspection of the signed-in account list, selector hardening, and test infrastructure. It lacks CMDK's reminders, receipts, snippets, and Nuke bundle. The keyboard layer is therefore commercially contestable and can be offered at zero price, but reliable Gmail automation and ongoing maintenance are not trivial. CMDK's current defensibility lies more in reputation, support, distribution, learned workflow, and the bundled extras than in proprietary interaction technology.

### Market-size conclusion

Public evidence supports three levels of claim:

1. **High confidence:** Chrome Store user proxies for Gmail workflow extensions reach three million, and some products sustain paid plans.
2. **Medium confidence:** a small price-conscious Superhuman-adjacent segment pays for a bundled shortcut/reminder/snippet/receipt layer.
3. **Not established:** CMDK has broad paid retention, a large category of its own, or a user base ready to migrate to full desktop clients.

[Google said in January 2026 that Gmail had three billion users](https://blog.google/products-and-platforms/products/gmail/gmail-is-entering-the-gemini-era/). That substrate is not a serviceable TAM. A useful bottom-up model needs paid conversion, retention, geography, browser/provider fit, email volume, and willingness-to-switch data that are not public.

---

## 9. Competitor and substitute map

### The decisive axes

The market separates along five axes:

1. **Overlay versus replacement:** keep Gmail visible or adopt a new client.
2. **Gmail-only versus multi-provider:** inherit Google's state or normalize providers.
3. **Local/minimal processing versus cloud/AI:** interaction control or mailbox intelligence.
4. **Individual processing versus team/revenue workflow:** Inbox Zero or shared/CRM outcomes.
5. **Zero migration versus full migration:** reversible enhancement or a new source of truth.

### Competitive groups

| Group | Examples | CMDK advantage | CMDK disadvantage |
| --- | --- | --- | --- |
| Native Gmail | Shortcuts, custom shortcuts, snooze, templates, multiple inboxes, Tasks, Gemini | Better command surface, coaching, receipts, bundled polish | Free, provider-native, mobile, no extension dependency |
| Calm Gmail overlays | Simplify Gmail | More Superhuman-like actions, reminders, receipts, snippets | Simplify is cheaper, more established, tracker-blocking, stronger privacy clarity |
| Point solutions | Boomerang, Right Inbox, Mailsuite, Mailbutler, Text Blaze | One subscription combines several jobs | Best-of-breed/free tools may be deeper or cheaper |
| CRM/team layers | Streak, Gmelius, Mixmax, Sortd | Lighter and more personal | No pipelines, shared inbox, admin, automation, or deep integrations |
| Gmail replacement clients | Superhuman, Shortwave, Mimestream, Kiwi | No migration, lower price, extension coexistence | Less mobile, AI, search, client polish, team capability |
| Cross-provider clients | Spark, Thunderbird, eM Client, Mailbird, Canary, Mailspring, Tecotype | Gmail state fidelity and instant activation | No Outlook/IMAP/unified/local cross-provider control |
| Browser workspaces | Wavebox, Shift, Chrome PWA | Rich Gmail-specific workflow | Wrappers consolidate more web tools/accounts |
| Cleanup/triage tools | Clean Email, SaneBox, Gmail subscriptions, Fyxer | User-controlled, visible actions | Less automation, background triage, or broad cleanup depth |

### Gmail is the strongest substitute

[Gmail's official shortcut set](https://support.google.com/mail/answer/6594?co=GENIE.Platform%3DDesktop&hl=en-EN) already covers compose, send, archive, delete, read/unread, snooze, reply, forward, navigation, labels, search, selection, and undo. Users can enable custom shortcuts. Gmail also provides:

- [multiple inboxes](https://support.google.com/mail/answer/9694882?hl=en) based on search criteria;
- [snooze](https://support.google.com/mail/answer/7622010?co=GENIE.Platform%3DDesktop&hl=en);
- [templates](https://support.google.com/mail/answer/14864208?hl=en), labels, filters, Tasks, [scheduled send](https://support.google.com/mail/answer/9214606?hl=en), spam filtering, search, and mobile apps;
- a [Manage subscriptions](https://support.google.com/mail/answer/15621070?hl=en) view that groups active mailing lists by sender and requests unsubscribe across the sender's associated lists; Google announced it for all personal and Workspace accounts in July 2025, while the current help page still warns that it may not yet be available; and
- Gemini drafting, summaries, and retrieval, with availability depending on feature, plan, language, and rollout.

Google's January 2026 product update made thread-summary AI Overviews, Help Me Write, and Suggested Replies available at no additional charge in its initial US-English rollout; asking arbitrary questions across the inbox remained a Google AI Pro/Ultra feature, while AI Inbox was still in trusted testing. The native substitute is therefore expanding into outcomes that were recently premium-client territory. CMDK can hide the Gemini interface for users who reject it, but it cannot assume that “no AI” alone is a durable feature advantage.

CMDK's value is not feature existence. It is better discoverability, a more coherent command grammar, natural-language time entry, coaching, receipts, compose automation, and lower interaction cost. Gmail's native subscription manager weakens “unsubscribe” as a durable paid wedge, although Google says the feature is still rolling out, completion may take several days, and some senders require a website handoff. Gmail does not remove existing messages, so Nuke's distinct outcome is immediate suppression plus backlog deletion—not confirmed list removal.

### Simplify is the closest strategic adjacent

Simplify shares CMDK's low-migration, Gmail-preserving, founder-led structure while emphasizing calm, privacy, bundles, saved searches, pausing, and tracker blocking. It charges $2/month annually for an individual, offers a one-month trial, has roughly 40,000 Chrome users, and explicitly describes continuous Gmail-change maintenance as the reason not to sell lifetime access.

The products can coexist. Simplify's [8 October 2024 App Store release notes](https://apps.apple.com/us/app/simplify-for-gmail/id1544668450?mt=12) explicitly added support for the Simplehuman extension. That is evidence of audience and technical adjacency, not a current distribution partnership.

The ethical contrast is notable: Simplify blocks tracking pixels while CMDK sells invisible read receipts. Tecotype's equanimity positioning is more naturally adjacent to Simplify's calm/privacy side than to silent recipient tracking.

### Positioning landscape

| Product | Primary promise | Risk removed for the buyer | Tradeoff accepted |
| --- | --- | --- | --- |
| Gmail | The provider-native default, increasingly AI-assisted | No extra vendor, migration, or payment | Generic interface and Google-defined workflow |
| CMDK | Superhuman-like speed inside Gmail without the premium bill | No client migration; low price; Gmail fallback | Browser/Gmail dependency, limited scope, receipt/telemetry ambiguity |
| Simplify | Make Gmail simpler, calmer, more private, and more capable | No migration; low price; no stated analytics; tracker blocking | Gmail/browser scope and fewer revenue-workflow features |
| Superhuman | Premium full-client speed, AI, and team workflow | High polish and a complete purpose-built system | High price, migration, broader mailbox processing |
| Tecotype | Calm local control across desktop email | Provider independence, unified accounts, local retrieval | Higher switching burden and price; public platform rollout still incomplete |

The clearest open territory for Tecotype is not “the fastest Gmail.” It is **a quiet, provider-independent local control plane for people whose email life no longer fits inside one web inbox**.

---

## 10. Acquisition, activation, and distribution

### Observed acquisition system

| Mechanism | Evidence | Role | Confidence |
| --- | --- | --- | --- |
| Chrome Web Store | Featured badge, recommended-practices status, public ratings | High-intent install and trust surface | High as current fact; attribution unknown |
| Superhuman comparison | Pricing, copy, SEO pages, review language | Captures users who want the workflow but reject price/client | High |
| Generic Gmail SEO | 200 modeled ranking keywords, job-led pages | Acquires from cleanup, shortcuts, rules, templates, reminders | Medium; modeled traffic only |
| Product Hunt | #4 day, friends/network rally, newsletter inclusion | Launch spike, backlinks, social proof | Medium; founder-reported downstream results |
| Newsletters | Founder says five newsletters covered launch; one kept sending daily users after two weeks | Borrowed-audience acquisition | Medium-low; no counts or paid conversion |
| Affiliate program | 20% of payments for life; 60-day cookie; $30 payout threshold | Creator/customer referrals | High as mechanics, unknown performance |
| Product signature | “Sent via CMDK” referral link can accompany receipt-enabled email | Recipient-driven product loop | High that the mechanic exists; default state and performance unknown |
| Founder support/word of mouth | Recurrent review praise and recommendations | Trust, reviews, retention, referrals | Medium-high |
| Community seeding | Repeated recommendations from at least one low-activity Reddit account | Manual awareness | Medium as observed pattern; not independent demand |
| Direct influencer outreach | Founder says cold outreach produced zero responses before creators approached post-launch | Tested non-working channel | Medium; vendor self-report |

### Activation design

CMDK's activation path is unusually short:

```text
Store listing / comparison page
→ install extension
→ open the Gmail already in use
→ press Cmd/Ctrl+K or receive a contextual shortcut nudge
→ perform an ordinary action faster
→ try a differentiating action such as Nuke, receipt, Tab, or reminder
→ 15-day paywall decision
```

There is no mailbox import, desktop installer, reindexing wait, or blank new-client state. According to CMDK's disclosures, activation also does not require Gmail API read/write OAuth access for message bodies. That is a distribution and product advantage that a full client cannot copy merely through better onboarding copy.

### Affiliate economics

The [affiliate program](https://cmdk.email/affiliate/) offers:

- 20% recurring commission for the life of referred payments;
- a 60-day attribution cookie;
- a 30-day holding period;
- a $30 payout threshold; and
- examples of $1.80 monthly, $15.80 annual, and $33.80 lifetime commission.

The program allows paid promotion but prohibits bidding on CMDK brand terms. Vendor claims about conversion and refund levels were not independently verified.

### Strict distribution assessment

Under this workspace's definition, distribution counts only when a partner permanently introduces Tecotype to someone with zero existing users and the first action can be attributed through paid conversion.

**CMDK has no evidenced qualifying distribution partner.** Chrome Store featuring, Product Hunt, SEO, newsletters, affiliates, Reddit, G2, and customer word of mouth are acquisition. The signature referral is an attributable product loop but not a permanent partner/pre-install introduction.

For Tecotype, the following are structurally capable of qualifying only if implemented, accepted, permanent, and joined to paid attribution:

| Candidate | Why it could qualify | What must be true |
| --- | --- | --- |
| [Setapp](https://setapp.com/developers) | Permanent catalog discovery, installation, licensing, usage and payout | Tecotype accepted; source/install/activation joined to paid economics |
| [Microsoft Store](https://learn.microsoft.com/en-us/windows/apps/publish/) | Permanent Windows search/browse/curation and acquisition analytics | Windows version shipped; store source survives into paid funnel |
| [Google Workspace Marketplace](https://developers.google.com/workspace/marketplace/how-to-publish) companion | In-Gmail discovery and possible domain installs | Companion provides real utility, hands off to desktop, attributes paid |
| [Chrome Web Store](https://developer.chrome.com/docs/webstore/about) companion | Searchable Gmail surface and managed-install potential | Not a hollow installer; useful deep link/local handoff; paid attribution |
| Simplify partnership | Highly aligned Gmail audience and prior compatibility work | Permanent in-product recommendation/integration, not a blog mention; partner source to paid |

These are research candidates, not commitments and not current distribution counts.

---

## 11. Implications for Tecotype

### Current capability boundary verified on 21 July 2026

The Tecotype source check used commit `9cfab3a337a0` plus the observed working tree. That tree already contained local changes to `architecture/logs.md` and `native/src/imap/sync_forward.rs`; this analysis did not modify them. The claims below describe source and architecture state, not acceptance of a named release artifact.

Tecotype's current repository implements substantial client functionality, including:

- Gmail and generic IMAP account paths;
- a local working copy and exact local search;
- optional on-device semantic “Better search”;
- unified/all-account navigation;
- Split Inbox and query-backed views;
- command palette and keyboard operation;
- reminders; and
- draft/sending foundations.

The release and architecture documents still describe important work before a broad public release, including sending UX completeness, onboarding, encryption, license gating, Gmail audit, and platform distribution. Current release infrastructure is macOS-oriented; Windows distribution is proposed/pending and Linux is not a current public release. The product and positioning documents describe a Mac-first phase.

The source implements an SMTP module and routes IMAP/Fastmail outbox sends through it, and the architecture index lists SMTP submit among the shipped sending core. The detailed IMAP document nevertheless still marks SMTP send pending. Until the status documents are reconciled, this report treats generic IMAP sync and an SMTP implementation as present, but SMTP-send release completeness as unverified.

Therefore this analysis does **not** claim that Tecotype is already publicly available across macOS, Windows, and Linux or that every comparison capability is shipped. The market analysis may assume a future published desktop product across those operating systems, as directed by this workspace, while public claims must remain current.

### Where CMDK is stronger

| Dimension | CMDK advantage |
| --- | --- |
| Activation | Seconds from Store to value inside an already-open Gmail |
| Migration | None; Gmail remains the interface and source of truth |
| Reversibility | Disable extension and ordinary Gmail remains |
| Mobile fallback | Gmail's mobile app continues to expose the same mailbox |
| Gmail fidelity | Search, labels, categories, spam, contacts, and provider behavior inherited |
| Price | $79 annual / $169 lifetime is a sharp counter-anchor |
| Modular stack | Coexists with Streak, Boomerang, HubSpot, Simplify, and other extensions |
| Learned Superhuman loop | Familiar shortcuts and command surface for defectors |

### Where Tecotype can be distinct

| Dimension | Tecotype advantage or intended wedge |
| --- | --- |
| Provider scope | Gmail plus generic IMAP sync; SMTP-send status requires reconciliation |
| Account control | True unified/all-account desktop operation rather than quick switching |
| Local working copy | Mail available for local processing and resilient retrieval |
| Search | Deterministic local exact search plus on-device semantic search |
| Provider independence | Workflow not tied to Gmail's rendered DOM or one browser family |
| Desktop environment | Purpose-built focused workspace rather than a modified web UI |
| Privacy architecture | Structural local processing can cover more than an overlay interaction layer |
| Long-term expansion | Published product can serve macOS, Windows, and Linux without depending on Chromium Gmail |

### The strategic category decision

Tecotype should not enter the comparison as “CMDK but native” or “Superhuman but cheaper.” Those frames invite buyers to ask why they should leave Gmail at all.

The defensible contrast is:

```text
CMDK: make one provider's familiar web inbox faster without migration

Tecotype: bring several providers into one calm, local, searchable desktop
control system when Gmail continuity is no longer enough
```

Speed is expected in both. Tecotype's reasons to switch are scope, retrieval, locality, provider independence, and a calmer cross-account operating model.

### Switching bar set by CMDK

A CMDK user considering Tecotype will expect:

1. **Immediate mailbox confidence.** Known mail, labels/folders, drafts, sent items, threads, attachments, and search results must appear predictably.
2. **Shortcut continuity.** A familiar keymap, discoverable palette, coaching, and ideally import/remap support reduce retraining.
3. **Correct account identity.** Unified views must make wrong-account replies harder, not easier.
4. **Obligation continuity.** Snooze/reminders/follow-up state must be visible and trustworthy.
5. **Compose reliability.** Signatures, aliases, CC/BCC, rich content, scheduling, undo, failures, and reply threading are fundamentals.
6. **A mobile/fallback story.** With mobile out of scope, users need clarity that provider mail remains accessible and how desktop-only local state behaves elsewhere.
7. **Reversibility.** Trial, cancellation, local data removal, and return to provider clients must feel safe.
8. **A value larger than the price delta.** Unified multi-provider search/control must be experienced quickly, not explained abstractly.

### Product hypotheses, not commitments

CMDK raises several research-worthy ideas:

| Hypothesis | Why it matters | Current treatment |
| --- | --- | --- |
| Contextual shortcut coaching | CMDK turns keyboard skill into a gradual habit | Validate with Tecotype users; do not claim shipped |
| Familiar/remappable keymaps | Reduces switching cost from Gmail, Superhuman, Spark | Validate by source cohort |
| Reusable snippets with safe placeholders | Strong revenue/support job and visible CMDK depth | Consider only after compose fundamentals are reliable |
| Natural-language reminder entry | Lowers friction in a core obligation loop | Compare with current reminder UX |
| Safe sender cleanup | Dramatic acquisition moment for overloaded inboxes | Test reversibility and provider semantics first |
| Appearance controls / quiet mode | Directly supports equanimity and AI-clutter rejection | Prefer coherent defaults over a settings explosion |
| Invisible read receipts | Segment demand exists, but recipient privacy and server needs conflict with north star | Do not assume parity; research ethics and architecture |

### Acquisition audiences worth testing

These are hypotheses for interviews or message tests, not channel commitments:

- former Superhuman users who rejected price, AI expansion, or a separate-client workflow;
- CMDK/Simplify/Gmail power users whose next pain is true multi-account or multi-provider retrieval;
- consultants, founders, and operators with Gmail plus one or more IMAP identities;
- people who keep a provider client open only to verify another email client's search; and
- privacy-conscious desktop users who want semantic retrieval without cloud mailbox processing.

The critical qualifier is **need beyond Gmail**. CMDK users satisfied by one provider and browser should not be forced into Tecotype's funnel merely because they like shortcuts.

---

## 12. Decision framework

### What CMDK validates

- People will pay for interaction quality on top of a free, capable provider UI.
- A command palette plus shortcut-learning system can create a valued habit.
- “Keep Gmail” is a strong acquisition and risk-reversal message.
- Superhuman price and product expansion create an alternative-seeking segment.
- Inbox Zero, follow-up, templates, and cleanup work together as an operating loop.
- Human support can be a retention feature in workflow software.
- Anti-bloat and no-forced-AI positioning has real customer resonance.

### What it does not validate

- A large CMDK-specific market.
- Paid conversion or annual/lifetime retention.
- Demand for a full client among satisfied Gmail-overlay users.
- True unified inbox or multi-provider demand within its current users.
- Enterprise readiness or regulated-industry trust.
- That read receipts, snippets, or any one feature cause retention.
- That public review positivity represents the installer base.
- That Store, SEO, Product Hunt, or referral traffic converts profitably.

### Tecotype decision rule

Treat CMDK as a **counter-position and source segment**, not as a blueprint.

Advance a CMDK-derived message or feature only when research shows:

1. the user has a recurring job with a concrete consequence;
2. Gmail/CMDK cannot solve it without another tool or repeated verification;
3. the job specifically benefits from Tecotype's local, unified, multi-provider architecture;
4. current product fundamentals can support the promise reliably; and
5. acquisition can reach the segment with attributable behavior, not only generic email traffic.

---

## 13. Highest-value unknowns

Public research cannot answer the following. The highest-value next evidence would be:

1. Eight to twelve active paid CMDK users split across monthly, annual, and lifetime plans.
2. Five people who completed the trial but did not pay, refunded, churned, or stopped using the extension.
3. Week-1, week-4, month-3, and month-12 active-user retention by plan.
4. Paid conversion by Chrome Store, SEO, Product Hunt, newsletter, affiliate, signature, and direct source.
5. Usage distribution by unique user—not only action volume—for command bar, shortcuts, Tabs, reminders, receipts, snippets, and Nuke.
6. How many customers previously paid for Superhuman versus only compared prices.
7. How many users co-install Simplify, Boomerang, Streak, HubSpot, or other extensions.
8. The exact behavior and failure cases of multiple-account switching.
9. What would make a CMDK customer accept migration into a full client.
10. Support burden and retention impact after Gmail interface changes.
11. Refund rate and the sustainability of lifetime pricing.
12. Exact server/data flow, retention, subprocessors, encryption, and deletion for receipts, snippets, analytics, and account metadata.

### Suggested interview screen

Screen on behavior, not title:

- Gmail/Workspace as primary desktop inbox;
- Chrome/Chromium use;
- messages processed and hours in email;
- number and type of accounts/providers;
- CMDK plan and tenure;
- previous/parallel Superhuman, Simplify, Boomerang, or other tool use;
- actual use of command bar, snippets, reminders, receipts, Nuke, and Tabs;
- last failure or fallback to native Gmail;
- mobile share of email work; and
- a recent message they could not find, defer, or act on in the desired way.

---

## 14. Strategic conclusions

1. **CMDK's category is premium-client avoidance.** It captures users who want the fast loop but prefer Gmail's interface, state, price, extensions, and fallback.
2. **Continuity is more important than the feature checklist.** Gmail inheritance removes migration risk and supplies free parity for search, spam, labels, mobile, and provider fidelity.
3. **The public footprint is small but the segment signal is real.** Repeated former-Superhuman reviews and 2026 usage telemetry show an active workflow; they do not show a large paid base.
4. **The category around it is established.** Simplify, Boomerang, Streak, and Mailsuite show Gmail extensions reaching Store user proxies from tens of thousands to three million across distinct jobs.
5. **CMDK's sharpest adoption advantage is low commitment.** A full client must earn the migration, not merely match shortcuts.
6. **The core interaction wedge is commercially contestable.** Free entrants already reproduce command palette, shortcuts, split tabs, and account switching; reliable Gmail-DOM maintenance remains real work, but those controls cannot carry differentiation alone.
7. **Pricing creates a hard Tecotype counter-anchor.** Tecotype must sell a larger cross-provider/local-control job, not “faster Gmail.”
8. **Privacy differentiation needs precise language.** CMDK plausibly avoids cloud processing of message bodies, but account analytics, receipt events, snippet sync, and stale legal pages make “everything local” indefensible.
9. **Trust documentation is the most avoidable weakness.** Trial, feature, server, compliance, and legal contradictions create disproportionate risk for a product inside email.
10. **No qualifying distribution exists today.** CMDK's Store, launch, SEO, affiliate, newsletter, signature, and community motions are acquisition, not permanent partner distribution.
11. **Tecotype should use CMDK to sharpen its boundary.** The opportunity begins where keeping Gmail is no longer enough: several providers, unified control, local exact and semantic retrieval, and calm desktop independence.

---

## Source register

### CMDK primary

- [Homepage and current features](https://cmdk.email/)
- [Pricing](https://cmdk.email/pricing/)
- [Chrome Web Store listing](https://chromewebstore.google.com/detail/cmdk-read-receipts-split/nipfocapamlefjhldhcagammlldbangf?hl=en-US)
- [Simplehuman-to-CMDK rebrand](https://cmdk.email/post/simplehuman-is-now-called-cmdk/)
- [Data collection disclosures](https://simplehuman.notion.site/Data-Collection-Disclosures-78ef0e5a5d244312a48afb1f05cc7bb2)
- [Privacy policy](https://cmdk.email/privacy/)
- [Terms of service](https://cmdk.email/terms/)
- [Release log](https://simplehuman.notion.site/Release-Log-bc25b5022d6048a99e916ce9d215bac6)
- [Snippets](https://cmdk.email/snippets/)
- [Read receipts](https://cmdk.email/read-receipts/)
- [Nuke / bulk-cleanup page](https://www.simplehuman.email/bulk-unsubscribe-gmail/)
- [CMDK usage guide](https://cmdk.email/learn-to-use/)
- [Affiliate program](https://cmdk.email/affiliate/)
- [CMDK aggregate usage data](https://cmdk.email/post/email-statistics/)

### Customer, launch, and company

- [Product Hunt product and reviews](https://www.producthunt.com/products/simplehuman)
- [G2 reviews](https://www.g2.com/products/simplehuman/reviews)
- [CMDK LinkedIn company profile](https://www.linkedin.com/company/cmdk-email)
- [Founder Product Hunt retrospective](https://www.linkedin.com/posts/guduthur_i-launched-on-product-hunt-and-it-led-to-activity-7299074104605753344-GW-E)
- [Founder early-build retrospective](https://www.linkedin.com/posts/guduthur_home-activity-7137036864993038336-cxJn)

### Native and competitor context

- [Gmail keyboard shortcuts](https://support.google.com/mail/answer/6594?co=GENIE.Platform%3DDesktop&hl=en-EN)
- [Gmail multiple inboxes](https://support.google.com/mail/answer/9694882?hl=en)
- [Gmail snooze](https://support.google.com/mail/answer/7622010?co=GENIE.Platform%3DDesktop&hl=en)
- [Gmail templates](https://support.google.com/mail/answer/14864208?hl=en)
- [Gmail scheduled send](https://support.google.com/mail/answer/9214606?hl=en)
- [Gmail Manage subscriptions](https://support.google.com/mail/answer/15621070?hl=en)
- [Google's July 2025 Manage subscriptions announcement](https://workspaceupdates.googleblog.com/2025/07/manage-email-subscriptions-in-gmail.html)
- [Gmail unsubscribe](https://support.google.com/mail/answer/15433283?hl=en)
- [Gmail sender blocking](https://support.google.com/mail/answer/8151?hl=en)
- [Google's January 2026 Gmail/Gemini update](https://blog.google/products-and-platforms/products/gmail/gmail-is-entering-the-gemini-era/)
- [Chrome Web Store discovery and Featured-badge criteria](https://developer.chrome.com/docs/webstore/discovery)
- [Chrome's definition of the extension “active users” field](https://support.google.com/chrome/a/answer/10836225?hl=en)
- [Simplify Gmail product and pricing](https://simpl.fyi/plans)
- [Simplify Chrome listing](https://chromewebstore.google.com/detail/simplify-gmail/pbmlfaiicoikhdbjagjbglnbfcbcojpj?hl=en)
- [Simplify App Store release history](https://apps.apple.com/us/app/simplify-for-gmail/id1544668450?mt=12)
- [Boomerang Chrome listing](https://chromewebstore.google.com/detail/boomerang-for-gmail/mdanidgdpmkimeiiojknlnekblgmpdll/details)
- [Streak Chrome listing](https://chromewebstore.google.com/detail/streak-crm-for-gmail/pnnfemgpilpdaojpnkjdgfgbnnjojfik?hl=en)
- [Mailsuite/Mailtrack](https://mailsuite.com/en/features/mailtrack)
- [Mailsuite/Mailtrack Chrome listing](https://chromewebstore.google.com/detail/email-tracker-by-mailtrac/ndnaehgpjlnokgebbaldlmgkapkpjkkb?hl=en-US)
- [Boomerang pricing](https://www.boomeranggmail.com/subscriptions.html)
- [Mailsuite pricing](https://mailsuite.com/en/pricing)
- [Superhuman Mail pricing](https://help.superhuman.com/hc/en-us/articles/46005733349517-Pricing-Plans)
- [Inbox Keys Chrome listing](https://chromewebstore.google.com/detail/inbox-keys-gmail-command/bfcdnkjplofjddlecpojhpoomdialafa)
- [Inbox Keys source repository](https://github.com/hadijaveed/inbox-keys)
- [Inbox Zero Tabs Chrome listing](https://chromewebstore.google.com/detail/inbox-zero-tabs-for-gmail/iencpoofingkkakccoknbleilcliokfk)

### Distribution mechanics

- [Setapp for developers](https://setapp.com/developers)
- [Microsoft Store publishing](https://learn.microsoft.com/en-us/windows/apps/publish/)
- [Google Workspace Marketplace publishing](https://developers.google.com/workspace/marketplace/how-to-publish)
- [Chrome Web Store overview](https://developer.chrome.com/docs/webstore/about)

### Tecotype verification basis

- [Tecotype product definition](product.md)
- [Tecotype positioning](positioning.md)
- [Architecture status and release boundary](../tecotype/architecture/README.md)
- [Current macOS release/update infrastructure](../tecotype/architecture/distribution-updates-analytics.md)
- [Windows distribution proposal](../tecotype/architecture/windows-distribution.md)
- [Generic IMAP implementation/status notes](../tecotype/architecture/imap.md)
- [SMTP implementation](../tecotype/native/src/smtp/mod.rs)
- [Outbox provider routing](../tecotype/native/src/outbox/submit.rs)
- [Local search architecture](../tecotype/architecture/search.md)
- [Split Inbox architecture](../tecotype/architecture/split-inbox.md)
- [Reminders architecture](../tecotype/architecture/reminders.md)
