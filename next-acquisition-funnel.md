# Current acquisition decision

Current verdict: **Provider placement is Parked. No route qualifies as an
Experiment.**

Research date: 2026-07-19

## Parked: provider client-choice placement

Test whether an email provider will introduce Tecotype while a customer is
choosing a desktop email client:

```text
provider setup, dashboard, or migration surface
→ normal Tecotype website and signed download
→ user evaluates the complete desktop email client
→ paid Individual plan
```

This is the clearest remaining serious lead because the person is already
choosing an email client. It does not rely on selling Tecotype through an
unrelated shortcut, archive viewer, or note-taking helper. Whether provider
users will actually buy Tecotype remains unknown.

The first step is **partner fact-finding, not product work**. No provider has
committed placement or supplied qualified monthly traffic.

## Candidates

| Provider                | Evidence                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Missing fact                                                                                                                                                             |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Namecheap Private Email | Its [general client guide](https://www.namecheap.com/support/knowledgebase/article.aspx/1179/2175/general-private-email-configuration-for-mail-clients-and-mobile-devices/) showed 274,346 cumulative views; it publishes [eM Client setup](https://www.namecheap.com/support/knowledgebase/article.aspx/10736/93/private-email-account-setup-in-em-client/) and [migration](https://www.namecheap.com/support/knowledgebase/article.aspx/10746/2226/how-to-transfer-emails-to-a-private-email-account-using-em-client/) guides. Its [August 2026 migration](https://www.namecheap.com/support/knowledgebase/article.aspx/10818/2178/new-private-email-webmail-heres-what-to-expect/) removes Unified Mail while ordinary clients continue to work. | Exact Tecotype placement, monthly unique exposure, outbound clicks, affected-user count, price fit, and partner acceptance. Cumulative counters are not monthly traffic. |
| Fastmail                | Its [device guide](https://www.fastmail.help/hc/en-us/articles/360058752834-Set-up-Fastmail-on-your-device) lists third-party desktop clients; its [partner page](https://www.fastmail.com/company/partners/) invites mail-app integrations; its [developer documentation](https://www.fastmail.com/dev/) provides the OAuth/JMAP path.                                                                                                                                                                                                                                                                                                                                                                                                             | Exact placement, qualified traffic, partner acceptance, and paid conversion.                                                                                             |

Namecheap tests capacity and timing. Fastmail tests audience fit and whether a
provider with explicit integration machinery will list Tecotype.

## Facts required before code

Ask each provider for:

- the exact permanent, host-controlled pre-install placement;
- monthly unique views of that surface;
- observed outbound clicks for comparable desktop clients;
- placement duration and removal terms;
- a direct link to Tecotype's normal signed download;
- aggregate impression and click reporting; and
- confirmation that no partner SDK, repackaging, managed updater, mailbox-data
  exchange, or per-user referral identifier is required.

Translate provider impressions into visits only with the provider's observed
outbound rate, not an invented click-through rate. Apply this capacity screen:

- below **2,800 relevant visits/month:** **Rejected** on capacity;
- **2,800–4,999:** **Parked** unless a current, tightly matched Tecotype cohort
  has an observed conversion rate sufficient for 10 purchases/month; and
- **5,000 or more:** capacity may pass for an **Experiment** using the 0.2%
  working visitor-to-paid assumption in [traffic.md](traffic.md).

This screen requires observed surface traffic. It qualifies only pre-launch
capacity; live Tecotype conversion determines whether the route becomes an
**Excellent channel**.

## Live experiment gate

Launch only after the discovery, capacity, paid-bridge, privacy, updater, and
cost gates all pass.

Success requires, on a rolling three-month average:

- at least 10 attributable new paid users/month;
- incremental channel CAC below USD 50;
- at least 60% retained at 90 days or first renewal; and
- continued host-controlled discovery without paid media.

At 10 new paid users/month, total incremental channel cost must stay below USD
500/month to preserve the CAC ceiling. Count provider-specific engineering,
review, creative, support, measurement, fees, and maintenance.

## Privacy and product control

- Tecotype ships one normal signed application and keeps its licensing,
  release policy, and updater.
- Mailbox credentials and tokens stay in local secure storage and are used only
  with the user's chosen provider.
- Mailbox content, addresses, domains, hostnames, messages, searches, and
  derived mailbox data never enter acquisition attribution.
- The provider receives no new mailbox information from Tecotype.
- Removing the partner link cannot disable, relicense, or strand the installed
  application.

Prefer provider-reported aggregate impressions and clicks plus a
channel-specific checkout source. Coarse source-to-paid measurement can qualify
an acquisition channel. A strict distribution claim additionally requires a
consented first-use-to-paid join using a random token scoped to this
experiment, with no mailbox fields. Delete it within 14 days after the 90-day
retained or cancelled outcome and always by day 120. Declining measurement
cannot reduce product value.

## Parked and rejected routes

| Route                             | Status       | Reason                                                                                                                                                                                                 |
| --------------------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| AlternativeTo                     | **Parked**   | Publish an accurate listing after Tecotype is publicly obtainable, but treat it as launch hygiene until exact traffic and paid conversion are known.                                                   |
| Raycast or Obsidian               | **Parked**   | Potentially useful local integrations, but exact capacity and same-user paid conversion are unknown. Build only for independent product value.                                                         |
| Todoist                           | **Rejected** | The thin email-to-task action duplicates Todoist's own task creation. A reply-aware workflow would be substantial product work with no evidenced acquisition capacity.                                 |
| ImportExportTools NG              | **Rejected** | It serves a one-time Thunderbird archive-export job, depends on maintainer promotion, and lacks a recurring paid-client bridge.                                                                        |
| Works With YubiKey                | **Parked**   | Catalog traffic and paid adjacency are unknown. Do not build hardware-backed mail security merely to test the route.                                                                                   |
| Paid Outlook or Superhuman search | **Rejected** | Capacity and CAC fail; see the [pain evidence](confirmed-pain-opportunities.md).                                                                                                                       |
| Setapp Membership                 | **Rejected** | Its [application requirements](https://docs.setapp.com/docs/preparing-your-application-for-setapp) and [update model](https://docs.setapp.com/docs/faq) replace Tecotype's licensing/updater boundary. |

Provider-panel variants such as cPanel, Plesk, Open-Xchange, and mailcow are
the same provider-client-choice hypothesis, not additional funnels. They remain
**Parked**; exact placement and traffic are the next missing facts, not
sufficient conditions to leave that status.

## Product boundary

The integration, placement, attribution path, and partner relationship are
proposed, not shipped or committed. Public platform and capability claims
remain governed by [product.md](product.md) and
[positioning.md](positioning.md). Pricing remains €149/year or €15/month as
defined in [pricing.md](pricing.md).
