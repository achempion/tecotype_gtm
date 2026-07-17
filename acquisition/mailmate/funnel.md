# MailMate funnel

Observed **2026-07-17** through public webpages and release metadata only. The
client link was not followed to an artifact. No app, account, mailbox, trial,
license, subscription, or checkout was used.

## Public pipeline

```text
power-user recommendation, integration, old review, or brand search
→ https://freron.com/
→ exact IMAP / keyboard / Markdown / search promise
→ “Download Beta macOS 10.12+”
→ configure IMAP and SMTP account
→ use search, smart mailbox, Markdown, or keyboard workflow
→ 14 active-use days
→ start $10-per-quarter subscription for Paid Mode
→ continue paying or cancel into Free Mode
```

Only the public-web stages were observed. Configuration and product behavior
come from first-party documentation, not a local test.

## Entry

The homepage's primary CTA is a direct beta link. There is no waitlist,
account-creation page, sales call, or email gate between the message and the
application trial.

The [download page](https://freron.com/download/) recommends the beta for new
users and says the public 1.13.2 release is more than four years old. The
current beta requires macOS 10.12 or later. Test releases are separately
labeled as potentially very unstable.

Direct access is low marketing friction. Depending on a beta and a stale
stable release raises product-risk and trust friction.

## Trial, paid, and free modes

The [pricing page](https://freron.com/pricing/) defines:

| Mode | Trigger | Features | Visible consequence |
| --- | --- | --- | --- |
| Trial | Initial use | No feature restriction for currently 14 active-use days | `MailMate Trial` mail-client header |
| Paid | Start subscription | All features | `MailMate` header |
| Free | Paid period expires | All features continue | `MailMate Free Mode` header and status button |

Paid Mode costs **$10 every three months**, plus local tax where required.
An annual $40 schedule is also offered on the
[support page](https://freron.com/support). Business use is required to remain
in Paid Mode; non-profit use does not require it.

The model lowers the technical penalty for cancellation, but it is cognitively
expensive:

- the user must understand that payment primarily funds maintenance;
- “subscription” does not imply exclusive features;
- cancellation is followed by a nudge visible in outgoing-message metadata;
- business and non-profit obligations differ; and
- payment does not guarantee support.

## Payment and support

The privacy policy identifies Fastspring as the primary payment-data holder
and Linode as the store for name, email address, and license records. Checkout
was not entered.

The pricing page and EULA say:

- payment supports maintenance and development;
- support is email-only and may not be provided;
- refunds are generally available when recent behavior is not as expected;
- the user must maintain backups;
- provider compatibility is not guaranteed; and
- native Exchange is unsupported.

This is unusually candid. It can also limit conversion for people who expect a
commercial support commitment.

## Activation hypothesis

A meaningful first-value sequence is more demanding than a download:

```text
one real IMAP account configured
→ initial sync completes without loss or provider error
→ user creates or uses a high-value search / smart mailbox
→ user completes a real keyboard or Markdown task
→ user returns voluntarily after the novelty period
```

MailMate does not publish an activation event, download count, trial cohort,
or conversion rate.

## Attribution

The current homepage exposes no client-side analytics or source propagation.
The public link goes directly to the beta artifact. The absence of a visible
tag does not rule out web-server or application telemetry, but no public
evidence connects:

```text
referrer
→ artifact request
→ launch
→ account configuration
→ first value
→ subscription
```

For a privacy-sensitive product, this path can still be measured with
source tokens and coarse events that never include mailbox content.

## Funnel assessment

Strong:

- exact audience filter;
- direct, ungated trial;
- all features available for evaluation;
- local/client architecture;
- durable documentation; and
- candid risk and refund language.

Weak:

- beta as default acquisition build;
- stale public release;
- no obvious web attribution;
- complicated paid/free distinction;
- no guaranteed support;
- macOS-only reach; and
- unobservable activation and retention.
