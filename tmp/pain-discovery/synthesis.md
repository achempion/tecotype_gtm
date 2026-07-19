# Sequential synthesis worksheet

Working state, not a final report. Updated 2026-07-19.

## Classification decision

### Qualified

**Outlook Classic known-message body-index omission**

Narrow evidence unit:

- actor: self-managed Classic Outlook user on Windows with data demonstrably
  local in an OST/PST;
- trigger: they search a remembered body term, sender, or subject for a message
  they can independently show exists;
- job: retrieve the intended message;
- mechanism: the local search index omits body content or otherwise returns a
  demonstrably incomplete set after the documented scope/index checks;
- consequence: repeated rebuilds/reinstalls, slow chronological search, old
  machine use, second-client use, or attempted full switch.

Confirmation IDs:

- O1: Microsoft Tech Community OP, 2025-11-02, Classic Outlook, Windows 11
  25H2, sender/subject searchable but body omitted.
- O2: distinct author on O1 page, 2026-05-30, three failed index rebuilds plus
  Windows reinstall/new disk; fourth rebuild took 24–48 hours for 1.7M items.
- O3: Microsoft Q&A, 2025-11-11, Classic Outlook for home, HTML and rich-text
  message bodies are omitted while text bodies and subjects remain searchable;
  multiple rebuilds and every documented check fail, while Safe Mode finds all
  formats.
- O4: Reddit, 2025-09, Classic Outlook on Windows 11 24H2, `deposit` yields 11
  versus 103 results elsewhere after 12 rebuilds, multiple profiles/accounts,
  and reinstall; disabling Windows Search yields 80/103.
- O5: Reddit, 2026-04, corrupt 20 GB OST plus PSTs, two months and 10+ evening
  hours of repairs; Outlook indexes headers but not bodies; eM Client imports
  and indexes the same stores, creating an attempted full switch.

All pages were opened. Counts: five independent authors, four pages, two
independently operated domains, official-support-community + Q&A + independent
forum source types, five observations within 24 months, and at least four
behavioral responses.

Independent prevalence/discovery: DataForSEO returned 90 modeled US monthly
searches, USD 0.75 CPC, 0.01/Low paid competition, keyword difficulty 0, and
Informational intent for the narrow `outlook search not finding emails` phrase.
The current SERP contained Microsoft support/Q&A, Reddit, and repair pages.
These are discoverability and ranking-model inputs, not market size, traffic,
willingness to pay, CAC, or payment.

Hard gates:

| Gate | Result | Basis |
| --- | --- | --- |
| useful free outcome | Pass | Complete read-only diagnosis/search indexes every parseable message in the user-selected local corpus, exposes any unparseable or out-of-scope store, and never paywalls retrieval; it does not overclaim that a non-result proves absence |
| private boundary | Pass as design | Proposed processing remains on device; mailbox contents, search terms, metadata, credentials, and files are not sent to Tecotype |
| desktop | Pass | Exact incident is Windows desktop; user instruction permits future Mac/Windows/Linux readiness as a planning assumption |
| zero-user source | Pass | Current exact-problem query and SERP are observed; route is Tecotype-owned acquisition |
| recommendation | Pass for validation, not confirmed Tecotype demand | Current exact Outlook search thread independently recommends eM Client or Thunderbird; current adjacent Outlook threads recommend and report switching to eM Client on the same surface |
| paid adjacency | Pass at minimum experiment gate | O5 imports into another full client and then encounters formatting, Zoom scheduling, and recurring live-mail jobs; a separate six-account user searches in another client then returns to Outlook for reply/organization; broader-client payment exists in independent eM Client-switch accounts but Tecotype conversion is Unknown |
| attribution | Pass as feasible design, not end-to-end shipped | The live release Worker records coarse UTM fields at an install redirect without an install ID; an opaque first-party token could extend the chain through local activation while only content-free stages leave device |
| testability | Pass | One segment, 100 successful-result denominator, explicit retrieval/activation/payment stops |

Channel verdict: **combination of Tecotype-owned exact-intent acquisition and
independent comparable recommendation**. Not distribution; no partner controls
a permanent pre-install Tecotype placement with an attributable paid funnel.

Score:

| Dimension | Weight | Evidence score | Weighted |
| --- | ---: | ---: | ---: |
| pain/consequence | 20 | 4 | 16 |
| addressable demand | 10 | 2 | 4 |
| zero-user discovery | 15 | 3 | 9 |
| recommendation | 10 | 3 | 6 |
| free-to-paid adjacency | 20 | 3 | 12 |
| attribution/testability | 10 | 3 | 6 |
| economics/burden | 10 | 2 | 4 |
| calm/privacy/fit | 5 | 4 | 4 |
| **total** | **100** |  | **61** |

Free offer:

- input: user-selected local PST/OST or a read-only connection to the locally
  present Classic Outlook store;
- setup: local corpus inventory and documented official-check checklist;
- output: explicit indexed scope, completeness limitations, chronological and
  literal results, matching-message anchors, and a user-confirmed intended
  message;
- complete result: search is never degraded; if the bytes are not local or
  cannot be parsed, say so before claiming success;
- delivery: current local lexical/semantic search and MIME parsing are
  **Current foundations**; PST/OST ingestion is **Net-new**; the diagnostic,
  corpus inventory, and intended-result confirmation are **Extensions**.

Funnel labels and content-free events:

| Stage | Claim | Event |
| --- | --- | --- |
| exact current query/SERP | Observed | no event until Tecotype owns a page |
| dedicated page | Proposed | `landing_viewed` with coarse `source_cluster=outlook_known_message` |
| utility start | Proposed | `utility_started` |
| local corpus ready | Proposed | `local_store_ready` |
| first useful result | Unknown until cohort | `intended_result_confirmed` boolean only |
| same-person live-mail need | Observed in individual accounts; Inferred for acquired cohort | `live_mail_connect_started` |
| Tecotype activation | Unknown | `account_sync_completed` |
| purchase | Unknown | `purchase` |
| retained milestone | Unknown | `retained_paid_milestone` |

Never transmit the query, sender, subject, mailbox/domain/provider hostname,
file name/path, match count, message/category, content, or credentials.
The browser-to-desktop handoff is the attribution breakpoint. **Observed in
current source:** the live release Worker accepts `utm_source`, `utm_medium`,
and `utm_campaign` on the stable install route, records version/OS/architecture
plus an edge-computed IP HMAC, and explicitly has no install ID. This measures
download intent, not install or activation. **Proposed:** generate a random
signed campaign token on the first-party landing, carry it through the
installer/browser-to-app handoff, redeem it for a consented, experiment-scoped
random funnel token, and expire that token after the retained milestone. Pass
a one-time derivative to checkout so payment can be attributed without joining
on billing identity. Do not use the IP HMAC to join stages. The current
implementation does not preserve the source from the redirect into app
activation or payment.

Economics:

```text
monthly paid users
= qualified zero-user opportunities
x source-to-landing rate
x landing-to-free-activation rate
x activation-to-expansion-trigger rate
x trigger-to-paid rate

monthly acquisition cost
= amortized build cost
+ maintenance
+ free-user support
+ channel cost
+ attribution infrastructure

CAC = monthly acquisition cost / new paid users
```

Known gross prices: EUR 15 monthly or EUR 149 annual, annual primary. Margin,
payment mix, LTV, retention, and support cost are Unknown.

The traffic model's one-purchase-per-1,000, 500, and 300 visitor sensitivities
imply 100 paid users require 100,000, 50,000, or 30,000 relevant visitors.
The narrow query's 90 modeled monthly searches is therefore a learning source,
not a scale plan. Even an impossible 100% click capture modeled through those
sensitivities yields only 0.09, 0.18, or 0.30 paid users/month.

Gross revenue threshold formulas:

- annual-first gross cash break-even purchases = monthly acquisition cost /
  EUR 149;
- monthly-first gross cash break-even purchases = monthly acquisition cost /
  EUR 15;
- maximum support cost per successful free result = Unknown until expansion
  and paid rates are measured.

Experiment:

- Recruit exact-intent users through one narrow page, initially using exact-
  match paid search to avoid waiting for SEO; screen out New Outlook,
  admin-controlled environments, server-only/online archives, missing local
  bytes, and cases fixed by official settings.
- Compare the local utility against Outlook's final result on the same
  user-known target.
- Complete the free result for everyone.
- Quietly offer live-mail connection only after success.
- Proposed maximum cash cost: **Unknown**, because PST/OST corpus licensing,
  security work, support, and build time are not priced.
- Proposed success after 100 qualified utility starts: at least 60 user-
  confirmed intended results; among confirmed results, at least 10% start
  live-mail connection; at least 3 distinct people reach paid purchase within
  30 days.
- Proposed failure: fewer than 30 confirmed results, or fewer than 5% start
  live-mail connection, or zero paid purchases after 100 confirmed results.
- Stop immediately if the utility uploads content/credentials, cannot
  establish a local-only corpus boundary, or most cases are resolved by one
  Microsoft setting/provider update.
- No product-native sharing loop is proposed; `K` is not applicable. Current
  third-party recommendation behavior supports acquisition testing, not a
  measured referral loop.

## Below confirmation after audit

### Google Takeout MBOX

Status: **Rejected/blocked as one confirmed pain and as a paid-client
opportunity.** Five direct authors show a durable format-access problem, but
the independent audit found distinct jobs: read one archive, restore into a
new account, quit Gmail, offload storage, and hand off records. The main exact
view/search job also has a complete current free viewer with Gmail-label,
search, attachment, large-file, and export support. Recommendations point to
Thunderbird, Betterbird, or the viewer. No source shows the same person moving
from completed archive success to paid live-mail-client use.

### Standalone MSG

Status: **Rejected/blocked as one confirmed pain and as a paid-client
opportunity.** The evidence spans accountless reading, Mac client/legal
evidence, CRM history, bulk FOIA review, Windows ARM preview, and conversion.
These have one file trigger but different completeness and failure mechanisms.
A current long-running Office365 thread independently validates an excellent
free browser-local/open-source viewer. Microsoft now documents `.msg` opening
in new Outlook for Windows for qualifying subscribers. Paid App Store behavior
is for the terminal viewer/converter, not a broader client.

## Final claim-audit checklist

- [x] One confirmed pain has five independent authors, four pages, two
  independently operated domains, three source types, all current within 24
  months, and four or more behavioral responses.
- [x] The confirmation unit is body-text indexing omission in Classic Outlook,
  not generic Outlook search, New Outlook, multi-account search, online
  archives, shared mailboxes, or forensic multi-PST review.
- [x] Search volume, CPC, competition, difficulty, and SERP positions remain
  modeled discovery evidence; none is treated as pain, traffic, CAC, payment,
  or willingness to pay.
- [x] The comparable recommendation is identified as current third-party
  behavior on `r/Outlook`, not a Tecotype recommendation, partnership, or
  distribution relationship.
- [x] The paid bridge is observed behavior into a broader client plus recurring
  live-mail jobs; Tecotype conversion, retention, and profitability remain
  Unknown.
- [x] The free result is complete and never artificially degraded. It exposes
  unreadable/out-of-scope stores rather than claiming a non-result proves
  absence.
- [x] Mail, files, credentials, queries, senders, subjects, domains, provider
  hostnames, and derived categories never enter attribution.
- [x] Current UTM/download-intent analytics are separated from the Proposed
  experiment token and end-to-end funnel.
- [x] Current source foundation is separated from a public release. Source
  claims are pinned to commit `b71a81a50e9b7251b60ce55f6b9d5f2477b0df82`;
  later uncommitted changes in the adjacent repository are excluded.
- [x] User-provided future macOS/Windows/Linux readiness is a GTM planning
  assumption, not a public-release claim.
- [x] Whole-database encryption, PST/OST ingestion, attribution continuity,
  licensing/payment, recommendations, and partnerships are not described as
  shipped.
- [x] No partner counts as distribution. No sharing loop or `K` is claimed.
- [x] Prices are gross; VAT, fees, refunds, support, margin, LTV, payment mix,
  retention, and profit are not invented.
- [x] Independent audits demoted MBOX and MSG rather than allowing scores to
  compensate for failed confirmation or hard gates.

## Key source index for final report

Pain confirmation:

- O1/O2 — <https://techcommunity.microsoft.com/discussions/outlookgeneral/outlook-search-not-returning-results-from-body-of-email/4466377>
- O3 — <https://learn.microsoft.com/en-us/answers/questions/5616891/classic-outlook-search-not-working-for-html-format>
- O4 — <https://www.reddit.com/r/Outlook/comments/1na53vy/outlook_search_completely_broken_on_current/>
- O5 — <https://www.reddit.com/r/Outlook/comments/1sodkzh/should_i_just_give_up_on_outlook/>

Recommendation and paid adjacency:

- current comparable recommendation —
  <https://www.reddit.com/r/Outlook/comments/1u88r5k/how_do_i_get_office_outlook_classic_outlooks/>
- current small-business switch recommendations —
  <https://www.reddit.com/r/Outlook/comments/1tkpczw/new_crappy_outlook_is_what_happens_when_microsoft/>
- paid/lifetime broader-client behavior and return-to-Outlook counterevidence —
  <https://www.reddit.com/r/Outlook/comments/1bduamy/switched_from_outlook_to_em_client_and_i_love_it/>
- current eM Client licensing boundary —
  <https://www.emclient.com/licensing?lang=en>

Provider and incumbent counterevidence:

- Microsoft search troubleshooting —
  <https://support.microsoft.com/en-US/Outlook/troubleshooting-outlook-search-issues>
- Microsoft current PST behavior —
  <https://support.microsoft.com/en-US/Outlook/open-and-find-items-in-an-outlook-data-file-pst>
- Microsoft current new-Outlook release notes —
  <https://learn.microsoft.com/en-us/officeupdates/release-notes-outlook-new>
- MailStore Home —
  <https://www.mailstore.com/en/products/mailstore-home/>
- DocFetcher —
  <https://sourceforge.net/projects/docfetcher/>

Demoted routes:

- MBOX evidence —
  <https://support.google.com/a/thread/249132211/pleasehelp-using-google-takeout-i-exported-a-folder-from-my-email-but-how-do-i-open-the-mbox-file?hl=en>,
  <https://support.mozilla.org/en-US/questions/1455205>,
  <https://support.mozilla.org/en-US/questions/1572448>,
  <https://www.reddit.com/r/GMail/comments/1tsg1o4/gmail_archive_inaccessible/>,
  <https://learn.microsoft.com/en-us/answers/questions/4313205/issues-in-opening-mbox-file>
- MBOX incumbents/counter —
  <https://sourceforge.net/projects/mbox-viewer/>,
  <https://documentation.its.umich.edu/mbox-thunderbird>,
  <https://www.reddit.com/r/Thunderbird/comments/1ug883b/how_to_retain_gmail_labels_when_importing_from/>
- MSG evidence and incumbent —
  <https://superuser.com/questions/1690247/configure-outlook-2016-as-a-msg-reader-only-without-any-profile-or-email-addres>,
  <https://learn.microsoft.com/en-us/answers/questions/5533098/how-to-open-msg-files-in-new-outlook>,
  <https://www.reddit.com/r/Office365/comments/1c1m3zn/msg_file_viewer/>,
  <https://apps.apple.com/us/app/msg-viewer-for-outlook/id973213640?mt=12&platform=mac&see-all=reviews>
- Microsoft current MSG behavior —
  <https://support.microsoft.com/en-us/outlook/mail/open-eml-msg-and-oft-files-in-new-outlook-and-outlook-on-the-web>

Local truth boundary:

- [Product](../../product.md), [positioning](../../positioning.md),
  [pricing](../../pricing.md), [traffic model](../../traffic.md), and
  [measurement rules](../../credibility.md).
- [Current search architecture](../../../tecotype/architecture/search.md),
  [proposed database encryption](../../../tecotype/architecture/database-encryption.md),
  [release analytics](../../../tecotype/architecture/distribution-updates-analytics.md),
  and [release infrastructure](../../../tecotype/infra/README.md).
