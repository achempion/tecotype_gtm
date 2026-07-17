# MonoMail funnel

Observed **2026-07-17** through public webpages, public repository metadata,
and public search results only. No app, release asset, store test, account,
mailbox authorization, Discord, donation, checkout, or payment flow was
entered.

## Funnel 1: public GitHub release

```text
Reddit, GitHub search, code index, direct mention, or owned landing page
→ repository or “Download Latest APK”
→ GitHub release page
→ release-asset download
→ install
→ provider account setup
→ first useful email action
→ retained use
```

Observed:

- permanent Reddit posts, repository, landing page, and release URLs;
- repeated latest-release CTAs;
- public release metadata;
- 30 releases from June 13 through July 15;
- 3,215 cumulative asset-download events; and
- visible disclosure that the public GitHub route lacks some maintained
  Google sign-in and notification capabilities.

Unobservable:

- landing visits and CTA click-through;
- download referrer;
- unique downloaders;
- successful installations;
- account-setup completion;
- connected inboxes;
- first useful action;
- day-seven or month-one retention; and
- payment or revenue.

No release page or asset was opened.

## Funnel 2: Play Store closed test

```text
owned landing page
→ “Get it on Google Play”
→ closed testing
→ store install
→ Gmail or other account connection
→ first useful email action
→ retained use
```

The landing page described the Play Store route as closed testing and the
full build. Public Reddit comments said the Google OAuth test cap had reached
100/100. The linked public store URL returned a not-found page in the
research snapshot.

This makes the accessible downstream state **unobservable**. The founder's
cap statement cannot establish that the places were all used by unique
people, that those people installed, or that they activated.

## Funnel 3: community and support

```text
Reddit, site, or GitHub
→ Discord
→ feedback, support, updates, and relationship
→ continued use or contribution
```

The Discord link is public, but membership and downstream behavior are not.
No referral token connects a Discord join to a later activation.

## Funnel 4: optional patronage

```text
landing-page appreciation
→ UPI or Ko-fi
→ voluntary donation
```

The project presents itself as free and open source. No feature upgrade,
recurring subscription, or paid tier was observed. A founder comment also
offered a `$5` personalized signed-build service when the user supplied cloud
credentials. No payment or completed delivery was observed.

These are support or service transactions, not evidence of an
activation-to-paid email-client funnel.

## Public offer

| Route | Public offer | Commercial interpretation |
| --- | --- | --- |
| GitHub | Free/open-source release path | No recurring revenue |
| Play Store | Closed-test full build | Access and activation unobservable |
| Discord | Community and support | No paid link observed |
| UPI / Ko-fi | Voluntary support | Donation, not subscription |
| Founder comment | `$5` personalized build offer | One-off service offer; completion unobserved |

## Candidate activation events

The public page's feature story suggests possible first-value events:

- merge two accounts into one view;
- find one old message through search;
- process one sender group;
- compose or reply successfully; or
- return to work offline.

These are **inferred from marketing copy**. No official activation event,
client telemetry, or user cohort was observed. A defensible Tecotype analogue
would need to be defined independently for a desktop workflow.

## Attribution evidence

The inspected public funnel exposed:

- direct links from the site to GitHub latest releases;
- direct links to the Play Store, Discord, UPI, and Ko-fi;
- public release counts by asset; and
- Reddit post-level vote and comment surfaces.

It did not expose:

- UTM or other source parameters on the inspected outbound CTAs;
- per-post landing visits;
- referrer-preserving desktop or app handoff;
- release downloads by source;
- activation events;
- product retention;
- donation completion;
- subscription conversion; or
- recurring revenue.

No analytics, advertising, or tag-manager marker was found in the inspected
server-delivered homepage HTML. This does not prove that no measurement
exists elsewhere.

## Funnel assessment

Strong:

- a short discovery-to-release path;
- permanent community and repository surfaces;
- transparent route limitations;
- frequent public release activity; and
- an obvious place for users to ask questions.

Weak or inconclusive:

- platform access split between public and closed-test routes;
- unavailable public store destination in the snapshot;
- no observed source preservation;
- asset downloads that cannot be deduplicated or joined to activation;
- support payments unrelated to a recurring product offer; and
- no public retention or revenue outcome.

Tecotype should borrow the simple public path and community dialogue, but
measure a desktop sequence from permanent source through first value,
payment, and renewal.
