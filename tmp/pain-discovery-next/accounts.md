# Sealed discovery ledger: high-consequence account workflows

Status: Independent second-funnel pass  
Research date: 2026-07-19  
Scope: wrong sender identity, one exact OAuth reauthentication mechanism, offline/draft/outbox reliability, and multi-account visibility.  
Excluded before research: the selected Classic Outlook search funnel and the previously examined provider-entitlement and mail-file routes.

This ledger was produced without reading or modifying prior pain-discovery ledgers, final reports, or acquisition documents.

## Outcome

**Strongest candidate: paid Superhuman users with three or more accounts who cannot see new mail from every account in one place.**

Exact mechanism:

> Superhuman Mail keeps accounts in separate tabs and does not have a unified inbox. Its desktop badge can represent only the active or most recent account for some users, and search is account-specific. People managing several client or work addresses must repeatedly cycle through tabs; if they do not, mail in an inactive account can remain unseen.

Verdict: **advance to a measured acquisition experiment, not a public claim or a validated channel.**

This is stronger than the other tested pains because it has:

- at least five homogeneous first-person incidents;
- direct reports of missed work mail, not only preference;
- an indexed, current official workaround that confirms the product gap;
- observed switches and recommendations to other full clients;
- direct same-person payment for broader email clients;
- a natural fit with Tecotype's calm, keyboard-first, all-accounts product thesis.

It is not yet a durable acquisition channel because query volume and conversion are unmeasured, free alternatives already provide unified inboxes, and Tecotype's licensing, payment, broad release, and full Microsoft-account support are not shipped.

## Candidate funnel

This is a **search and comparison acquisition funnel**, not distribution under the strict partner-placement definition.

```text
Searches or recommendations about Superhuman's missing unified inbox
  → factual Tecotype comparison/solution page
  → see the all-accounts workflow
  → install when the relevant platform and provider are supported
  → connect at least two accounts
  → open All accounts
  → complete one useful mail action in each account
  → choose Tecotype Individual
```

Candidate discovery queries:

- `superhuman unified inbox`
- `superhuman multiple accounts missing emails`
- `superhuman alternative unified inbox`
- `email client unified inbox keyboard shortcuts`

The exact query `superhuman unified inbox` currently returns Superhuman's own workaround page, which states that the feature is absent and instructs people to create a tab for each account. Current Reddit discussions and independent review pages are also discoverable for the same problem. This proves an observable discovery surface, not traffic volume.

Suggested page hypothesis:

- Working route: `/superhuman-unified-inbox-alternative`
- Page label: `All your accounts, one calm view`
- Factual comparison: Superhuman currently suggests a tab per account; Tecotype's target workflow is one all-account view with account-specific views still available.
- Proof, not promise: show two accounts in one list, switch to an individual account, then process one message from each.
- CTA only after release truth is satisfied: `Try Tecotype with your accounts`.

Do not lead with “never miss an email.” The current Tecotype source verifies an all-accounts view but does not verify a global desktop badge or notification behavior for inactive accounts.

## Five homogeneous first-person incidents

The unit is a person reporting the same workflow failure: several active mail accounts, no all-account visibility, repeated manual checking or unseen mail. Dates below are the public post or review dates, not crawl dates.

| ID | Date | Source type | First-person incident | Consequence | Paid adjacency |
|---|---|---|---|---|---|
| U1 | 2025-02-13 | Reddit user post | A Superhuman user has nine addresses on client domains and says they spend half the day cycling through tabs merely to see what arrived. | Constant attention and repeated checking across client accounts. | The person is an established Superhuman user and has requested the feature since the service's first version; payment is likely but not explicitly stated. |
| U2 | 2025-04-25 | Reddit comment | A person explicitly using the paid version says they are constantly missing messages because three work accounts must be checked manually and no desktop badges appear. | Unseen work mail after only two days of use; likely churn. | **Direct:** explicitly paid Superhuman use. |
| U3 | 2025-01-09 | Reddit user post | A new Superhuman user with three or four accounts says the icon badge shows only the most recent account and mail in the others will be missed completely. | Inactive-account mail is invisible without deliberate checking. | The person describes the purchase as a large financial commitment, but the thread also mentions a remaining free-month decision; treat payment as intent, not confirmed cash. |
| U4 | 2024-08-19 | Reddit user post | A former Superhuman user with seven accounts canceled because acting on mail required switching accounts and there was no unified view. | Product churn despite liking the client. | **Direct churn adjacency:** former Superhuman subscription user; exact payer is not independently verified. |
| U5 | 2025-01-04 and 2025-01-06 follow-up | Reddit user post and owner follow-up | A technology executive handles eight accounts daily plus three monitored accounts. The user says unified views in Spark and Outlook remove account switching, then reports paying for a full Superhuman month and receiving a refund after canceling. | A high-volume professional rejects the broader paid client as impractical for daily multi-account work. | **Direct:** paid month and refunded cancellation. |
| U6 | 2024-12-28 | Capterra verified review | A marketing user rates Superhuman highly but names both cost and lack of a unified inbox as the reasons it is not a five-star service. | Paid-client value is reduced by missing cross-account visibility. | Review is verified by Capterra; the user switched from Polymail and Mailbutler. |

Exact sources:

- U1 and U2: https://www.reddit.com/r/SuperhumanEmail/comments/1io7tcf/no_unified_inbox_how_do_you_survive/
- U3: https://www.reddit.com/r/SuperhumanEmail/comments/1hxccgd/new_sh_user_after_a_few_days/
- U4: https://www.reddit.com/r/SuperhumanEmail/comments/1evtsd8/unified_inbox_in_superhuman/
- U5: https://www.reddit.com/r/SuperhumanEmail/comments/1htix3s/do_i_just_not_get_it/
- U6: https://www.capterra.com/p/199278/Superhuman/

Independent aggregate corroboration:

- G2 currently groups **40 mentions** under the lack of a unified inbox slowing or complicating email management. The page contains current-user and validated-review labels, but some reviews are incentivized or seller-invited, so it is corroboration rather than an incident-count base: https://www.g2.com/products/superhuman-mail/reviews?page=7&qs=pros-and-cons
- Superhuman's current help center explicitly says the product does not have a Unified Inbox and offers per-account tabs as the workaround: https://help.superhuman.com/hc/en-us/articles/46005722297229-Unified-Inbox-Workaround

## Observed recommendations and actual switching

These are recommendations observed inside the incident discussions, not Tecotype commitments:

| Alternative | Observed behavior | Evidence quality |
|---|---|---|
| Polymail | A user says it replaced tab cycling, has been used for seven years, and supports nine accounts. A second person states they pay **$140/year for ten accounts**. | Strong same-person paid adjacency within the exact pain thread. |
| Spark Desktop | One former Superhuman user says the missing unified inbox drove the switch back to Spark; another executive points to Spark's unified inbox and account labels. | Direct switch behavior. |
| Mimestream | A user says they now use Mimestream for Gmail and calls it good, with the missing iOS app as the remaining issue. | Direct recommendation, but Gmail-only and not cross-provider. |
| Spike | A commenter recommends a unified inbox after six years of use. | Long usage claim, payment unknown. |
| simplehuman.email | A commenter says they moved away from Superhuman's higher price and value the unified inbox and Gmail interface. | Direct switch, but it is an extension rather than a full local client. |
| Separate tabs | Superhuman's official workaround is one native-app tab per account with keyboard shortcuts to cycle among them. | Authoritative current workaround and strong counter-positioning. |

The broader market already understands the job. Mailspring currently offers multi-account IMAP and Microsoft 365 support, cross-account search, a unified inbox, keyboard shortcuts, and direct local sync at no charge for the core workflow; Pro is $8/month:

- https://www.getmailspring.com/

That is strong counterevidence against charging for “unified inbox” alone.

## Same-person paid adjacency

The paid-adjacency requirement is met more clearly here than in the other tested clusters:

1. A paid Superhuman user with three work accounts reports constantly missing mail.
2. A high-volume executive reports paying for a full Superhuman month and then canceling.
3. A person in the exact pain thread reports paying $140/year for Polymail with ten accounts.
4. Former Superhuman users report canceling or switching specifically because all-account visibility is absent.
5. Superhuman's current plan page places Mail in the Business plan at **€33 per member per month billed annually, or €40 monthly** as accessed on 2026-07-19:
   https://superhuman.com/plans

This evidence shows willingness to pay for a broader professional client. It does **not** show that a unified inbox by itself earns Tecotype's €149 annual price. The paid value is the bundle: fast keyboard work, reliable all-account visibility, organization, search, reminders, and a coherent daily experience.

## Independent discovery evidence

Current search checks on 2026-07-19:

| Query | What surfaced | Interpretation |
|---|---|---|
| `superhuman unified inbox` | Superhuman's official workaround page and the active Reddit incident thread. | The exact problem is indexable and the incumbent confirms it. |
| `superhuman multiple accounts missing emails unified inbox` | The paid-user thread with missing-mail language. | High-consequence language is discoverable. |
| `superhuman alternative unified inbox privacy local email client` | Mailspring and current alternative discussions. | There is active solution comparison, but also intense incumbent competition. |
| `email client unified inbox keyboard shortcuts multiple accounts` | Mailspring and client roundups. | The generic query is crowded and likely less qualified than the competitor-gap query. |

An independent June 2026 setup guide also treats the desktop combined view as the cleanest way to unify accounts while preserving provider separation and sender identity:

- https://email-tools.me/posts/unified-inbox-setup/

The page carries affiliate disclosure and promotes Mailbird, so it is evidence of a monetized search surface, not an independent product endorsement.

No keyword volume, clicks, signups, or conversion are known. Search-engine visibility must not be described as attribution.

## Counterevidence and failure modes

### The all-account view is not universally desired

In the same Superhuman thread, one user says mixed accounts would create context switching and prefers deliberate separation. Another has adapted the existing badge system to a work/personal routine. The candidate must preserve account-specific views and make All accounts optional.

### Unified views can increase sender-identity mistakes

In the August 2024 Superhuman discussion, a commenter says a wrong-address send in Spark made account separation feel safer. A useful Tecotype experiment therefore needs both:

- a clear account marker on every row and compose surface;
- sender selection tied predictably to the received account, with a visible and reversible override.

Do not promote the all-account view without testing sender-confidence alongside it.

### Free and cheaper clients already solve the visible feature

Mailspring, Thunderbird, Apple Mail, Spark's basic experience, and other clients offer some form of combined inbox. The exact Superhuman threads recommend several alternatives. Tecotype cannot win on a feature checklist or price comparison alone.

### The incumbent may close the gap

Superhuman has published a workaround rather than a unified view, but this is a software gap, not a structural prohibition. A future release could invalidate comparison copy quickly. Any page needs a review owner and evidence date.

### Search intent may be support-seeking, not switching

A person searching the exact query may want a toggle or workaround inside Superhuman, especially after already paying for it. The experiment must measure downstream install and two-account activation, not rankings or clicks.

### “Never miss mail” is not verified

Tecotype's current source contains an `All accounts` state and cross-account inbox queries. The research did not find shipped operating-system notification or all-account badge behavior. The candidate solves the one-list review workflow, but not yet every passive-notification failure reported by Superhuman users.

## Product and release truth

Verified against `product.md`, `positioning.md`, and `../tecotype` on 2026-07-19:

- Tecotype's working product description includes unified views across accounts.
- The source has an explicit `All accounts` state, an `activeAccountId` of `null`, and cross-account thread/inbox queries.
- Gmail and generic IMAP connection are implemented to varying levels of completeness.
- Gmail and IMAP account data are handled in one local-first client.
- The current implementation does not establish Microsoft OAuth or Exchange support as a shipped public capability.
- No global inactive-account notification or desktop badge guarantee was verified.
- Licensing and payment flows, first-run onboarding, the public acquisition experience, and broader distribution beyond the Mac-first release remain unfinished.
- A permanent free plan and trial policy are undecided.

Implication: the funnel is a valid research target, but no page should yet promise universal Gmail, Outlook, Microsoft 365, iCloud, or cross-platform replacement. The workspace instruction permits building provider support when it materially improves acquisition; public copy must wait until the relevant integration and platform are actually released.

## Why the other clusters did not win

### Wrong sender identity: strong runner-up, mechanism not homogeneous enough

Current incidents have serious consequences:

- On 2025-11-13, eM Client users described work mail sent from a personal account, replies becoming lost in the personal inbox, six configured accounts, and a desire for enforced sender choice:
  https://forum.emclient.com/t/best-practise-choose-correct-email-account-for-sending/112459
- On 2025-07-31, an Apple Mail user said a reply from the wrong account exposed private banking information and responded by disabling the other accounts:
  https://talk.tidbits.com/t/order-of-smtp-servers/31381

However, the incidents split among different mechanisms: active-folder defaults, SMTP-account mapping, reply-address inference, manual oversight, and changed server configuration. Recommendations are mostly free extensions, color cues, separate windows, and domain fencing. Direct current payment caused by one exact wrong-sender mechanism was weaker than the Superhuman visibility cluster.

### Offline/draft/outbox reliability: real, but cause diversity and excluded-channel overlap

Current Outlook incidents include a 2026-01-28 message shown as an edited draft in Outbox and a 2025-05-30 business user whose messages send only after restarting:

- https://learn.microsoft.com/en-us/answers/questions/5746013/my-outgoing-email-is-stuck-in-outbox-how-can-i-fix
- https://learn.microsoft.com/en-us/answers/questions/4728769/outlook-msg-stuck-in-outbox-until-i-restart-my-out

The same symptom can be caused by offline mode, edited-message state, attachments, connectivity, add-ins, profiles, cached mode, or queue corruption. It did not form one homogeneous mechanism, and a Classic Outlook query funnel is explicitly excluded from this pass.

### OAuth reauthentication: one exact mechanism found, insufficient incident and payment evidence

The cleanest exact mechanism was a required Microsoft 365 work-password change leaving Thunderbird's stored OAuth token unusable. The user deleted the token, became trapped in a password loop, and ultimately recreated the account:

- 2026-02-25 Reddit user incident:
  https://www.reddit.com/r/Thunderbird/comments/1reau6p/office_365_mail_oauth2_issue/
- Current Mozilla documentation on Microsoft OAuth changes and troubleshooting:
  https://support.mozilla.org/en-US/kb/microsoft-oauth-authentication-and-thunderbird-202

This mechanism did not produce five homogeneous current incidents with observed broader-client payment. It is also a Microsoft/Thunderbird integration support problem rather than a clean Tecotype acquisition wedge.

## Minimum experiment

### Page

Create a dated, factual comparison page only when the supported provider and platform claims are true:

1. State that Superhuman's current help center recommends separate account tabs.
2. Demonstrate Tecotype's optional All accounts view and account-specific views.
3. Show the sender identity before any reply or new message.
4. Explain that mail remains with its providers and that Tecotype works from a local copy.
5. Avoid AI, urgency, pain dramatization, and unverifiable time-saved claims.

### Activation

The qualifying activation event is not installation:

> The same person connects at least two supported accounts, opens All accounts, then completes one useful action on a message from each account.

Useful actions can include open-and-reply, archive, move, or set a reminder. Instrumentation must avoid mailbox contents, addresses, subjects, senders, recipient domains, and provider credentials.

### Success and kill criteria

Advance only if all are true:

- the exact comparison query produces qualified visits rather than support-only bounces;
- visitors connect two accounts at a materially higher rate than general traffic;
- they use All accounts on more than the first session;
- sender-account mistakes do not increase;
- a meaningful share proceeds to the existing Individual purchase decision;
- interviews confirm that all-account visibility contributed to the purchase rather than merely attracting the click.

Kill or reframe if:

- users choose free Mailspring, Thunderbird, Apple Mail, or Spark after learning the feature is common;
- most target users have only one account or prefer strict separation;
- Microsoft-account support is required for most qualified demand and is not released;
- the all-account view lacks sufficient unread/new-mail signaling;
- activation does not reach both accounts;
- search visibility exists but source-to-paid attribution does not.

## Retained source register

Every retained public page below was opened during this pass.

| URL | Public date | Source type | Role |
|---|---:|---|---|
| https://www.reddit.com/r/SuperhumanEmail/comments/1io7tcf/no_unified_inbox_how_do_you_survive/ | 2025-02-13; retained comments through 2026-01-20 | First-person community thread | U1, U2, recommendations, direct paid adjacency, counterevidence |
| https://www.reddit.com/r/SuperhumanEmail/comments/1hxccgd/new_sh_user_after_a_few_days/ | 2025-01-09 | First-person community thread | U3 |
| https://www.reddit.com/r/SuperhumanEmail/comments/1evtsd8/unified_inbox_in_superhuman/ | 2024-08-19; retained comments through 2025-07-30 | First-person community thread | U4, switches, wrong-sender counterevidence |
| https://www.reddit.com/r/SuperhumanEmail/comments/1htix3s/do_i_just_not_get_it/ | 2025-01-04; paid follow-up 2025-01-06 | First-person community thread | U5 |
| https://www.g2.com/products/superhuman-mail/reviews?page=7&qs=pros-and-cons | Accessed 2026-07-19; individual reviews include 2025 dates | Verified-review platform | Independent aggregate corroboration and caveat |
| https://www.capterra.com/p/199278/Superhuman/ | U6 dated 2024-12-28 | Verified-review platform | U6 and paid alternative adjacency |
| https://help.superhuman.com/hc/en-us/articles/46005722297229-Unified-Inbox-Workaround | Accessed 2026-07-19 | Official product support | Authoritative current absence and workaround |
| https://superhuman.com/plans | Accessed 2026-07-19 | Official pricing | Current paid adjacency |
| https://www.getmailspring.com/ | Accessed 2026-07-19 | Competitor product page | Free-incumbent counterevidence |
| https://email-tools.me/posts/unified-inbox-setup/ | 2026-06-01 | Affiliate-disclosed independent guide | Monetized discovery surface and caveat |
| https://forum.emclient.com/t/best-practise-choose-correct-email-account-for-sending/112459 | 2025-11-13 to 2025-11-20 | Vendor community forum | Rejected wrong-sender runner-up |
| https://talk.tidbits.com/t/order-of-smtp-servers/31381 | 2025-06-30 to 2025-07-31 | Independent technical community | Rejected wrong-sender runner-up and consequence |
| https://learn.microsoft.com/en-us/answers/questions/5746013/my-outgoing-email-is-stuck-in-outbox-how-can-i-fix | 2026-01-28 | Vendor-hosted first-person Q&A | Rejected outbox cluster |
| https://learn.microsoft.com/en-us/answers/questions/4728769/outlook-msg-stuck-in-outbox-until-i-restart-my-out | 2025-05-30 | Vendor-hosted first-person Q&A | Rejected outbox cluster |
| https://www.reddit.com/r/Thunderbird/comments/1reau6p/office_365_mail_oauth2_issue/ | 2026-02-25 | First-person community thread | Rejected exact OAuth mechanism |
| https://support.mozilla.org/en-US/kb/microsoft-oauth-authentication-and-thunderbird-202 | Accessed 2026-07-19 | Official support documentation | OAuth mechanism corroboration |

## Final confidence

- Pain homogeneity: **high**
- Consequence: **high for a subset**, because unseen client/work mail is directly reported
- Independent discovery: **medium-high**, because exact queries and independent reviews surface the gap
- Observed recommendation behavior: **high**
- Same-person broader-client payment: **high**
- Tecotype product fit today: **medium**, because All accounts exists but global badge behavior and Microsoft support are not verified
- Paid differentiation from free clients: **medium-low**
- Funnel readiness: **medium-low until release truth and attribution are in place**

The opportunity is worth a narrow experiment because the audience already pays for speed and reports churn over this exact workflow. It should be killed quickly if the combined Tecotype experience cannot beat free all-account clients on calmness, keyboard speed, sender confidence, and local control.
