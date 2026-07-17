# Public funnel

Captured: **2026-07-17**

The public, unauthenticated funnel ends at a waitlist success state. Everything
after that point is private or described only in first-party policy/terms.

## Reconstructed path

```text
SEO article, Reddit recommendation, direct visit, or product-aware search
→ homepage or newsroom article
→ “Get early access” / #waitlist
→ email submitted to /api/waitlist
→ submitted and success events sent to PostHog and /api/event
→ email stored in Notion according to privacy policy
→ “You’re on the list. We’ll be in touch.”
→ invitation, download, Gmail OAuth, sync, activation, retention, and payment
  unobservable
```

Only the steps through the form and its public client wiring were directly
observed. No email was submitted.

## Stage evidence

| Stage | Public evidence | Status |
| --- | --- | --- |
| Discovery | Indexable newsroom, current Reddit comments, live Google result for a product-aware query | Observed surfaces; traffic unknown |
| Landing | Product page with screenshot, features, privacy, FAQ | Observed |
| Intent | Two “Get early access” email forms | Observed |
| Form request | Public client posts `{email, website}` to `/api/waitlist` | Observed in bundle |
| Measurement | PostHog plus `/api/event`; distinct/session identifiers passed | Observed wiring |
| Storage | Privacy policy says private Notion database | First-party disclosure |
| Confirmation | “You’re on the list. We’ll be in touch.” | Observed client success state |
| Invitation | Site says private beta; one Reddit account says people are admitted slowly | Claimed, not walked |
| Download/install | No public binary or route found | Unobservable |
| Gmail authorization | Terms say Gmail-only beta; privacy describes direct Gmail API and Keychain tokens | Claimed, not walked |
| First sync/onboarding | No public flow | Unobservable |
| Activation | No public definition or event | Unobservable |
| Retention | No cohort or usage data | Unobservable |
| Payment | FAQ says free in beta and paid later; terms/privacy mention Polar | No active public checkout |

## Form and event sequence

The public bundle indicates this order:

1. validate the email field and honeypot;
2. capture `waitlist_signup_submitted` in PostHog with the email;
3. send a parallel event with the same name/properties to `/api/event`;
4. post email, honeypot, and PostHog distinct/session headers to
   `/api/waitlist`;
5. on success, identify the PostHog profile with the email;
6. capture a success event including the email and mirror it to `/api/event`;
7. display the confirmation copy.

This supports page-to-waitlist measurement and likely duplicate/client-server
reconciliation. It does not reveal deduplication rules, delivery rate,
dashboard use, invite attribution, or privacy retention.

The privacy policy describes PostHog as collecting pageviews, click events,
referrer, device/browser metadata, and anonymized IP information. Passing the
waitlist address as an event property and identifier is additional observable
client behavior not clearly stated in that list. Server behavior was not
tested.

## Conversion boundaries

### What the site can measure publicly

From client wiring, the operator could plausibly analyze:

- pageviews and referrer metadata;
- clicks and page exits;
- form submission attempts;
- successful waitlist responses;
- person/session association after an email is supplied.

“Could” is deliberate. No analytics output was available.

### What is not publicly connected

No visible event or identifier bridges the waitlist to:

- an invitation;
- a binary download;
- installation or first launch;
- Gmail OAuth completion;
- initial synchronization;
- first useful action;
- next-day or next-week return;
- a Polar license or payment.

Those links may exist privately. They cannot be inferred from the public site.

## Offer and friction

Observed offer:

- Mac only;
- Gmail only;
- macOS 26 or later;
- private beta;
- email required;
- free during beta;
- a paid app is planned after public launch.

Unpublished:

- price or billing interval;
- invitation cadence or eligibility;
- waitlist position;
- number of beta users;
- supported Gmail account types/scopes;
- installer size, signing, and system architecture;
- setup time or first-sync size;
- AI model size, hardware needs, or opt-out;
- trial length, refund policy, or launch date.

The page asks for low commitment but offers low immediacy. Its largest hidden
drop-off is not the form; it is the unknown interval and experience between
waitlist confirmation and first value.

## Activation hypotheses

ZenMail's page suggests possible activation events:

- approve or deny a first unknown sender in Screener;
- archive/reply/snooze a message by keyboard;
- snooze with a natural-language time;
- process a first message in Zen Mode;
- complete initial sync and find an older message;
- connect a second Gmail account.

None is confirmed as ZenMail's internal activation metric. “Joined waitlist”
is a lead event, not product activation.

## Funnel verdict

Observed:

- one clear public conversion;
- explicit submission and success events;
- a privacy policy naming storage and analytics vendors;
- a repeated waitlist CTA across owned content.

Unknown:

- visits by source;
- form start, validation, and success rates;
- duplicate or invalid addresses;
- waitlist size and invitation rate;
- time to invitation;
- OAuth, sync, and activation completion;
- cohort retention;
- beta-to-paid conversion and revenue.

No public evidence supports a claim that ZenMail's waitlist is large, that
private-beta demand is qualified, or that any channel produces retained users.
