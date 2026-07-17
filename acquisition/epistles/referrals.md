# Epistles referrals and community acquisition

Research date: **2026-07-17**

Scope: **attributable founder activity, independent public discussion, the
branded subreddit, backlink rows, and narrow exclusions**

Public votes, memberships, comments, and anecdotes are dynamic. They show that
somebody engaged; they do not expose source-to-install attribution or represent
all users.

## Headline result

Epistles' strongest visible discovery loop is provider-specific community
research followed by rapid public replies and patches.

The best evidence is not the generic 1.0 launch. It is:

- a [Fastmail feedback request](https://www.reddit.com/r/fastmail/comments/1t3sny6/multiaccount_email_client_with_fastmail_native/)
  that asked about JMAP, aliases, domains, and identity edge cases;
- a [Proton tester request](https://www.reddit.com/r/emailprivacy/comments/1t3scps/protoncapable_desktopmobile_mail_client_no_bridge/)
  that disclosed the reverse-engineered path and asked Bridge users for
  concrete pain points;
- a [Stalwart/JMAP post](https://www.reddit.com/r/stalwartlabs/comments/1u8978r/email_client_compatible_with_stalwart_jmap/)
  with a captured score of +9, implementation questions, an invite request,
  and one stated intention to join; and
- an [independent Stalwart beta report](https://www.reddit.com/r/stalwartlabs/comments/1u6yyj7/epistlesmail_jmap_client_user_report/)
  with a captured score of +4 and conditional lifetime-purchase intent.

That is real problem discovery and attention. It is not a verified install or
sale funnel.

## Attributable community activity

| Date | Surface | Actor | Message and response | Interpretation |
| --- | --- | --- | --- | --- |
| 2026-05-04 | `r/fastmail` | Founder/product account | Native JMAP and Fastmail OAuth; asked which real setups a normal client breaks | Specific research prompt, not a launch blast |
| 2026-05-04 | `r/emailprivacy` | Founder/product account | Proton without Bridge, risks and missing WebAuthn disclosed; asked for Bridge pain points; +1 captured | Low reaction but unusually clear qualification |
| 2026-06-16 | `r/stalwartlabs` | Independent user | Said beta was fast, responsive, and the only tested Android JMAP client with working arrival notifications; calendar/contact issues remained; +4 | Strongest independent use anecdote; purchase only conditional |
| 2026-06-17 | `r/stalwartlabs` | Founder/product account | Native Stalwart JMAP alongside other providers; +9, questions, invite request, signup intent | Strongest founder post in captured evidence |
| 2026-06-17 | `r/degoogle` | Founder/product account | Near-identical Stalwart/provider message; +4 captured | Some cross-community reach, weaker specificity |
| 2026-07-08 | `r/stalwartlabs` | Founder/product account | 1.0 launch; +2; discussion exposed compose, attachment, stability, closed-source, and price objections | Launch produced product feedback, not broad endorsement |
| 2026-07-08 | `r/tutanota` | Founder/product account | Removed launch post; comments challenged credential trust and reported Tuta sign-in failures | Distribution attempt met trust and reliability resistance |
| 2026-07-09 | Privacy Guides forum | Independent user | Tried with a low-value account and liked it enough to ask about regular use | Genuine trial anecdote, followed by source/telemetry objections |
| 2026-07-16 | `r/ProtonMail` | Independent user | Asked whether the unofficial integration risks account or session stability; +5 | High-value trust question, not promotional endorsement |
| 2026-07-17 snapshot | `r/EpistlesMail` | Mixed | 82 members, release posts, requests, praise, and setup/failure reports | Small support and feedback surface |

Scores are captured observations and can change.

## What provider specificity achieved

The community messages worked best when they contained an implementation fact
that the audience could interrogate:

- native JMAP to a self-hosted server;
- Fastmail OAuth plus JMAP semantics;
- Proton without Bridge, with explicit unofficial-API risk;
- several provider accounts in one client; and
- direct device-to-provider communication for normal mail sync.

That specificity produced better questions than a generic “new email client”
post:

- how Stalwart authentication and Cloud Vault storage work;
- whether Proton works on mobile;
- whether ordinary IMAP is supported;
- which secrets reach Epistles infrastructure;
- whether closed source is acceptable for mailbox access; and
- what happens when an unofficial provider API changes.

These questions are acquisition research and trust objections at the same
time.

## Branded subreddit

[r/EpistlesMail](https://www.reddit.com/r/EpistlesMail/) was created on
2026-05-02 and displayed **82 members** on the research date.

The current feed contained:

- version announcements;
- praise and lifetime-offer discussion;
- feature requests;
- Gmail connection trouble;
- iCloud timeout reports;
- Proton sign-in loops;
- Stalwart setup questions;
- Ubuntu and Flatpak issues;
- generic “not working” reports; and
- questions about safety and the company behind the app.

This is useful because it brings the repair loop into public view. It also
makes launch instability conspicuous. Membership is not active-user count,
and post authors cannot be assumed representative.

## Independent use and purchase anecdotes

Three public anecdotes are more informative than reaction counts:

1. The independent Stalwart reporter said the beta was fast and responsive and
   expressed an intention to buy lifetime **if** the remaining features worked.
   That is conditional purchase intent, not a transaction.
2. The Privacy Guides thread starter said they tested with an account they did
   not use, liked the app, and were considering broader use. Replies then
   challenged closed source and marketing-site telemetry. The current security
   page now explicitly distinguishes app telemetry from Google Analytics on
   the site.
3. In a
   [Spark Mail discussion](https://www.reddit.com/r/SparkMail/comments/1ukthc9/considering_a_switch/),
   one commenter said they bought lifetime as “Berean 54,” regretted it, and
   requested a refund after product and support problems. This is an
   unverified self-report, but it is stronger evidence of a purchase and
   dissatisfaction than the public seat counter alone.

None of these anecdotes establishes a conversion rate, refund rate, or
retention pattern.

## Trust and criticism as acquisition evidence

The July 16
[Proton thread](https://www.reddit.com/r/ProtonMail/comments/1uyebz4/new_email_cli%C3%ABnt_epistles_mail_using_proton/)
is a compact view of the trust barrier:

- the original poster wanted to understand the reverse-engineered integration
  before relying on it;
- the founder acknowledged that Proton does not sanction the integration and
  described two session/sign-in bugs fixed in 1.3.8;
- highly upvoted replies advised against trusting the closed-source product;
- other replies questioned licensing, reliability, and how the product was
  built.

This is one thread, not a sentiment survey. Its value is diagnostic: technical
novelty gets attention, but a sensitive integration makes identity,
independent proof, source availability, and failure handling part of the
acquisition funnel.

## Backlink audit

DataForSEO reported:

| Metric | Result |
| --- | ---: |
| Backlinks | 86 |
| Referring domains | 46 |
| Referring main domains | 43 |
| Referring pages | 84 |
| Backlink spam score | 53 |
| First seen | 2019 |
| Detail rows returned | 43, one per domain |

The domain existed long before the current product. The detail rows therefore
cannot be treated as 46 product referrals.

### Credible current rows

- [Privacy Guides: “Has anybody tried Epistles mail?”](https://discuss.privacyguides.net/t/has-anybody-tried-epistles-mail/39055)
  was directly captured and discussed the current product.
- A row pointed to a
  [Mac Power Users email-client thread](https://talk.macpowerusers.com/t/what-email-clients-are-people-using-in-2026/45455?page=4).
  Epistles was not visible in the current captured page, so the row is not
  counted as a verified current mention.
- The founder's public Reddit posts are important discovery surfaces but were
  not the meaningful part of the backlink-detail sample.

### Noise and inherited domain history

Most rows were:

- automated website reports;
- shortener/share mirrors;
- nameserver and domain lists;
- low-quality directories;
- unrelated old-domain pages;
- the founder's existing software-business sites; or
- a 1990s/2000s immigration page under the reused domain.

The backlinks headline therefore overstates current editorial authority.

## Other channels and exclusions

- The footer links X, Instagram, Facebook, LinkedIn, and Reddit. Reliable
  public reach and downstream outcomes were not obtained.
- Generic or near-duplicate launch messages sometimes had little response or
  were removed.
- Narrow checks found no material Product Hunt, Hacker News, or press launch.
- The Google Ads archive checks returned no matching result.
- DataForSEO Content Analysis returned no exact-domain mention rows.

“Not found” means not established in the captured sources, not proof of
permanent absence.

## Referral conclusion

Epistles has demonstrated a viable **research and attention loop**:

```text
provider-specific implementation claim
→ technically literate community
→ questions, invite interest, criticism, or trial
→ founder reply and rapid patch
→ activation, retention, and payment mostly unobservable
```

For Tecotype, the transferable move is a precise, honest invitation around an
already-working job. The non-transferable move is broad cross-posting before
mail correctness and the trust surface are ready. Every community link should
carry a source token, and success should be a retained, voluntarily paying
user—not a vote score or comment count.

Exact request details are in [requests.md](./requests.md).
