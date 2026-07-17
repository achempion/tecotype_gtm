# HEY funnel

Observed **2026-07-17** through public webpages only. No account was created,
no form was submitted, no trial was started, no mailbox was connected, and no
payment details were entered.

## Primary personal funnel

```text
founder/company audience, press, Product Hunt, referral, or branded search
→ https://www.hey.com/
→ “We finally fixed your email + calendar”
→ product mechanisms, testimonials, and walkthrough
→ “Try HEY free”
→ https://app.hey.com/sign_up
→ create HEY account
→ choose @hey.com address
→ receive and screen a sender
→ experience Imbox / Feed / Paper Trail / Reply Later
→ decide whether to pay $99/year
```

The [public signup page](https://app.hey.com/sign_up) says:

- 30 days free;
- no credit card required;
- $99/year afterward; and
- account setup comes before choosing an address.

The pricing page says the personal plan is annual only. Because no payment
method is collected for the trial, an inactive evaluator cannot be silently
converted into a charge. That is a calm and reversible entry mechanic.

## Offer structure

| Offer | Price | Trial | Important condition |
| --- | ---: | --- | --- |
| HEY for You | $99/year | 30 days, no card | Annual billing; includes @hey.com address, 100 GB, calendar, and HEY World |
| HEY for Domains | $12/user/month; first user $10 | No product trial | Monthly; 30 days allowed for setup and switchover |
| HEY Families | $179/year | Starts from a personal account | Up to five individual accounts |

Two- and three-character addresses carry separate high annual prices. They are
a scarcity-based naming product, not evidence about the standard plan's
economics.

## Provider-switch friction

HEY is explicitly a provider, not a client for existing accounts. Its
[FAQ](https://www.hey.com/faqs/) says:

- users receive a new @hey.com address;
- HEY does not support IMAP or POP;
- another email app cannot access a HEY mailbox;
- other accounts can forward new mail into HEY; and
- historical mail cannot be imported.

The [Gmail migration guide](https://www.hey.com/moving-from-gmail/) tries to
make the switch incremental:

1. configure Gmail forwarding and, optionally, Google-authorized send-as;
2. export contacts and import a vCard;
3. optionally export old mail to an MBOX file; and
4. retain Gmail for searching old messages.

The guide estimates about three minutes for forwarding/send-as and five
minutes for contacts. Those estimates are first-party and were not tested.
Replies sent from HEY are not saved back into Gmail, and old mail remains
outside HEY. The evaluator therefore has both setup work and a split historical
record.

## Activation hypothesis

A defensible activation event is not “account created” or “address claimed.”
The first value sequence is more likely:

```text
address chosen
→ first real sender arrives
→ user makes a Yes/No Screener decision
→ message lands in the intended Imbox, Feed, or Paper Trail
→ user completes a real reply or retrieval task
→ user voluntarily returns on another day
```

That sequence is inferred from the product story. HEY does not publish its
activation definition or cohort data.

## Measurement

The public homepage:

- emits a Plausible `signup_start` event on marked signup links; and
- passes public `source`, `utm`, `ref`, `referrer`, and `utm_source`
  parameters into the signup destination.

This could preserve discovery source into account creation. Public scripts do
not reveal whether the same identity is connected to migration, first value,
payment, or renewal. The absence of public evidence is not evidence that
internal attribution is absent.

## Strong and weak conversion mechanics

Strong:

- a no-card trial;
- exact price before signup;
- mechanisms demonstrated before commitment;
- a dedicated migration guide;
- clear export and cancellation language; and
- apps across major platforms.

Costly:

- new provider and often a new identity;
- annual-only personal payment;
- no historical mail import;
- proprietary app requirement;
- no HEY for Domains trial; and
- a deliberately unfamiliar workflow.

The 2020 attention data shows that many people were willing to start. It does
not show how many completed migration or renewed.
