# Public funnel

Quartz changed from an email waitlist to an ungated Mac download shortly before
its Product Hunt launch. The public record supports two separate funnels.

## May 2026: private-beta waitlist

The [May 23 archived
page](https://web.archive.org/web/20260523204711/https://www.quartzmail.ai/?ref=betalist)
showed:

- “MAC · iOS · GMAIL — PRIVATE BETA.”
- An email field with placeholder `you@yourcompany.com`.
- “Join waitlist.”
- “Quartz is in private beta on Mac and iPhone.”
- “We send invitations in small batches.”

The public path was:

```text
BetaList-attributed, newsletter, founder, or unknown discovery
→ attention/privacy landing page
→ email waitlist
→ invitation in a small batch
→ installation and activation unknown
```

No public evidence gives the waitlist size, invitation rate, time to invitation,
platform split, or activation.

## June 17 onward: public Mac beta

The Product Hunt launch page replaced the waitlist with a direct download.
Research followed the path through the public disk image and inspected the
mounted app bundle without launching it. No third-party app code was executed
or installed, no Gmail authorization was granted, and the temporary disk image
was removed on 2026-07-17 after the user clarified a no-client-download
research boundary. Everything after the disk-image
boundary below is a reconstruction from Quartz's own policy, maker comments,
case study, and static app artifacts:

```text
Product Hunt, maker post, newsletter, directory, search, or direct visit
→ Quartz homepage
→ Download Quartz for Mac
→ 307 redirect to versioned Apple Silicon disk image [directly observed]
⋯ launch app and connect Gmail [not manually walked]
⋯ complete onboarding and local-model download [Quartz-described]
⋯ initial categorized inbox [Quartz-described]
⋯ category correction or draft [Quartz-described]
⋯ activation and retention unknown
⋯ no current website payment step
```

The report does not establish the exact current screen order, permission
prompts, error handling, completion rate, or experienced first value.

## Current public path

Observed on 2026-07-17:

1. The homepage says Mac, Gmail, and public beta.
2. The primary CTA points to `/download`.
3. `/download` returns a 307 redirect to
   `Quartz_0.1.88_aarch64.dmg`.
4. The object is public, 15,628,612 bytes, and was last modified June 27.
5. No website email, account, sign-in, waitlist, or checkout step appears.
6. The closing copy says Quartz is free for beta users.
7. The terms say the service is currently free and any future fee requires the
   user's express agreement.

The small installer is not the complete setup cost. In the [Product Hunt
discussion](https://www.producthunt.com/products/quartz-3), a maker said Gemma
4 is downloaded during onboarding and that model updates currently re-download
the roughly 4 GB file. The same discussion
describes user-written categorization and writing-style preferences. The
[datarockets case
study](https://datarockets.com/case-studies/quartz-mail-ai/) says onboarding:

- connects Gmail;
- asks the user to describe themselves and what belongs in each importance
  tier;
- downloads local models; and
- prepares the app for the first categorized inbox.

The referenced model repository independently reports
`gemma-4-E4B-it-Q4_K_M.gguf` at 4,977,171,584 bytes, about 4.98 GB decimal or
4.64 GiB ([repository
API](https://huggingface.co/api/models/unsloth/gemma-4-E4B-it-GGUF/tree/main?recursive=true&expand=false)).
The 15.6 MB installer therefore cannot contain it, although static artifact
references do not prove that this variant is selected on every machine.

Quartz does not disclose the model size beside the website CTA. Download
completion, model setup, sync duration, and abandonment are unknown.

## Offer and payment

The current [terms](https://www.quartzmail.ai/terms) state:

- Quartz is offered without charge.
- Paid functionality, subscriptions, or other fees may be introduced later.
- A user will not be charged without express agreement.
- The product is a public pre-release beta and may change or be withdrawn.

The homepage JSON-LD also advertises a zero-dollar offer. No public current
price, trial end, card step, or paid conversion path was found.

Consequently, Quartz's public funnel points toward free-beta product use, but
public evidence does not reveal activation or retention. It also provides no
evidence about willingness to pay or acquisition economics.

## Instrumentation and privacy

The website loads PostHog capabilities for page behavior, web vitals, dead
clicks, surveys, and recording. The [privacy
policy](https://www.quartzmail.ai/privacy) says:

- website analytics include page views, clicks, device/browser, and
  IP-derived approximate location;
- the app sends PostHog product events;
- beta app events are associated with the connected email account;
- beta telemetry is mandatory and cannot be disabled in the app;
- mail content and correspondent data are not sent as analytics according to
  the policy.

This could support install and activation analysis if the website source is
preserved into the app identity. Public evidence does not show that linkage,
the event taxonomy, or any funnel report.

## Friction and qualification

### Friction removed

- No current email gate or scheduled call.
- No card or payment.
- Stable direct download.
- Clear Mac, Apple Silicon, Gmail, and free-beta qualification.
- Product screenshots and a short demo before the download.

### Friction deferred

- Gmail authorization occurs after installation.
- The roughly 5 GB referenced local model is not disclosed beside the CTA.
- Model download and first mailbox sync can delay value.
- Automated categorization requires personal preferences and later correction.
- Mandatory account-identified telemetry is disclosed in the privacy policy,
  not in the acquisition copy.
- Mac/Apple Silicon/Gmail eligibility excludes many visitors.
- Future price is unknown.

## Activation boundary

Quartz does not publish an activation definition. Plausible events include:

- completing Gmail authorization and first sync;
- seeing the first categorized inbox;
- correcting a classification and observing the preference later;
- sending a first assisted draft; or
- using Quartz on a later day.

These are hypotheses. A download or connected Gmail account alone does not
prove experienced value.

## Implication for Tecotype

Tecotype's signed Apple Silicon distribution is live, but its public site,
first-run/no-account onboarding, licensing/payment flow, and Gmail audit are
not complete. It should not imitate Quartz's direct launch until a
representative user can:

```text
understand the offer
→ download
→ open
→ connect Gmail or generic IMAP
→ complete first sync
→ perform a meaningful keyboard/search workflow
→ return later
```

Tecotype already makes one setup fact more explicit: the shipped Better-search
onboarding states the optional one-time 318 MB download before asking. Test
whether that disclosure improves trust, and preserve its factual clarity in
the public funnel.
