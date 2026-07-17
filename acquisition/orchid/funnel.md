# Orchid funnel

Observed **2026-07-17** through public webpages, public metadata, and public
search results only. No account, Google connection, mailbox authorization,
trial, SMS, form, checkout, or payment path was entered.

## Funnel 1: Zero's 2025 email-client offer

```text
GitHub, Product Hunt, YC, HN, Reddit, or branded search
→ 0.email email-client landing page
→ “Get started” / Google account connection
→ Free plan or seven-day Zero Pro trial
→ AI chat, writing, labeling, and thread summaries
→ subscription
→ retention and renewal unobservable
```

The residual [pricing page](https://0.email/pricing) presents:

| Plan | Public offer | CTA |
| --- | --- | --- |
| Free | One email connection, basic inbox chat and labeling, limited writing | Get started |
| Zero Pro | `$20 / MONTH` under an annually billed presentation, unlimited connections and fuller AI features | Start seven-day free trial |
| Enterprise | Similar feature list plus dedicated Slack and priority support | Contact |

The [privacy page](https://0.email/privacy) says the premium trial requires a
valid card, rolls into paid billing unless canceled, and becomes
non-refundable after the trial except at the company's discretion. Checkout
was not entered, so price presentation, tax, billing interval, payment
provider, and actual purchase behavior were not verified.

The [about page](https://0.email/about) claims more than 15,000 early-access
signups in under three months. It does not define whether those people were
waitlist entries, accounts, connected mailboxes, activated users, trial users,
or subscribers.

## Funnel 2: the current `0.email` transition

```text
legacy brand query, old link, or existing user
→ “0.email is now Orchid”
→ choose:
   • Meet Orchid
   • Sign in to Zero
   • GitHub
```

This page preserves continuity, but it divides the audience:

- new assistant interest moves to `orchid.ai`;
- existing Zero users move to the legacy sign-in;
- developers and self-hosters move to GitHub.

No public metric shows how traffic or users divide across those routes.

## Funnel 3: current Orchid

```text
Orchid brand result, current content, case study, or 0.email transition
→ orchid.ai
→ personal-assistant message and concrete SMS demonstrations
→ “Get Started”
→ sms:+14152999916
→ text conversation and service connection
→ useful delegated outcome
→ paid subscription
```

Only the path through the SMS destination was observed. The SMS application
was not opened and no message was sent.

The public [terms](https://orchid.ai/terms) say certain features require a
monthly or annual paid subscription and describe a 30-day money-back guarantee.
The public pricing route returned no visible plan content beyond navigation
and footer. The current amount, trial mechanics, billing trigger, and paid
conversion path are therefore **unobservable**.

An existing-user path also exists:

```text
orchid.ai
→ Login
→ app.orchid.ai?source=site&utm_source=site&utm_campaign=login
→ account and connected tools
```

The parameters demonstrate source-tagging capability for the login route. They
do not show that a new-user SMS start preserves the source or that the app
connects it to payment.

## Enterprise path

```text
orchid.ai
→ Enterprise
→ Typeform
→ qualification, sales conversation, integration, contract
```

The external form destination was visible but not opened. Questions, lead
qualification, response times, pricing, and closed-won attribution remain
unknown.

## Activation clues

The [beta announcement](https://orchid.ai/blog/orchid-beta-is-here) says the
first users could connect Google and have Orchid begin learning within
minutes. The current site demonstrates:

- a request completed through messages;
- proactive inbox and calendar handling;
- recurring habits;
- a reminder delivered at the right time; and
- remembered personal context.

These suggest candidate first-value events, but Orchid publishes no official
activation definition. A defensible inferred activation sequence would be:

```text
start SMS conversation
→ connect one relevant service
→ receive one correct, useful prepared action
→ approve or use the outcome
→ return voluntarily for a second task
```

This is **inferred**, not observed competitor analytics.

## Attribution gaps

Visible measurement capability:

- source parameters on the app Login URL;
- a PostHog analytics component in the site payload;
- some third-party links to `0.email` with UTM or `ref` parameters; and
- public launch and repository counters.

Unobservable:

- whether the SMS CTA carries the landing source into Orchid;
- visits and click-through rates;
- Google or other integration completion;
- first useful action;
- day-seven or month-one retention;
- free-to-paid conversion;
- enterprise lead-to-contract conversion;
- overlap between Zero users and current Orchid users; and
- renewal or revenue by channel.

## Funnel assessment

Strong:

- multiple permanent discovery surfaces from the Zero launch;
- concrete current demonstrations;
- simple repeated current CTA;
- retained legacy-user access; and
- some visible source tagging.

Weak or inconclusive:

- two categories and brands in one inherited funnel;
- no visible current plan amount;
- an SMS primary CTA with no visible source token;
- undefined early-access signup quality;
- no public activation, retention, or payment cohort; and
- repository and launch metrics that stop before customer value.

Tecotype should borrow the demonstration and coordinated launch pattern, while
keeping one category, one canonical page, and a source token that survives
through desktop activation and paid renewal.
