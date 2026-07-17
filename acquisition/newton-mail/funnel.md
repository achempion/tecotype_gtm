# Newton Mail funnel

Observed **2026-07-17** through public webpages, rendered page state, public
store listings, and public metadata only. No client, account, mailbox, trial,
form, checkout, subscription, download, or install flow was used.

## Public pipeline

The current public system exposes several possible pipelines rather than one
reconciled flow.

### Mature homepage route

```text
brand search, old press, review, store history, or recommendation
→ https://newtonhq.com/
→ “Email. Supercharged.”
→ “Try Newton for free”
→ platform or subscription route
→ stated 14-day evaluation
→ stated $49.99 annual subscription
```

### 2026 relaunch route

```text
owned relaunch story or returning-user link
→ “The calm inbox returns”
→ acknowledgment of shutdown history and architecture change
→ Request Access
→ provider and platform qualification
→ invitation or access state
```

### Store route

```text
brand/store search or old installed-app history
→ Apple App Store or Google Play listing
→ store evaluation and privacy declarations
→ install control
→ provider connection
→ in-app subscription or existing entitlement
```

Only the discovery, page, offer, and store states were observed. Later stages
are stated or inferred from first-party surfaces.

## Entry and CTA state

The homepage's primary `Try Newton for free` link moved to the footer in the
captured page. `Subscribe Now` had a `#` destination. Mac and Windows links
exposed direct artifact destinations; Linux used `#`; Apple and Google store
links pointed to their public listings.

The June relaunch article exposes a request-access structure with fields for
contact, provider, and platform. The form was not completed or submitted.

The linked UserJot changelog returned a page-does-not-exist state. This breaks
an evaluation route for a visitor specifically seeking current proof.

## Offer and price

The homepage and Apple listing support a **$49.99 annual** offer. The homepage
states a **14-day** free period. Historical sources show that Newton has used
other prices:

- the 2018 shutdown coverage described a $9.99 monthly or $99.99 annual
  subscription; and
- the 2019 return and 2020 independent-owner era used approximately $50
  annually.

These are dated offer states, not a normalized price experiment. No public
source provides current conversion, renewal, refund, support cost, or
contribution margin.

## Proof and objection handling

The mature route uses:

- 40K subscribers;
- press quotations;
- app-store ratings;
- a feature inventory; and
- 14-day evaluation.

The relaunch route uses:

- explicit acknowledgment of prior shutdowns;
- a causal explanation of server-heavy economics;
- a lighter-architecture claim;
- publisher/owner voice; and
- access scarcity created by an early cohort.

The latter is better matched to the current trust objection. The former is
better matched to a stable, immediately purchasable product. Showing both
without a shared status explanation increases decision friction.

## Attribution surfaces

The homepage loaded RudderStack, an Intercom integration, Seline analytics,
and Intercom. These can support acquisition measurement and support. They do
not prove:

- that campaign source survives into the client or store;
- that the request-access form is connected to a cohort;
- that privacy choices are respected consistently;
- that any particular event is defined as activation; or
- that source-level subscription or renewal is measured.

No public source joins:

```text
referrer or query
→ landing state
→ store, request, trial, or subscription handoff
→ provider connection
→ first useful action
→ voluntary return
→ payment
→ renewal
```

This absence does not imply that Newton lacks private measurement.

## Marketing interpretation

The main conversion problem visible from outside is not CTA friction alone. It
is state ambiguity:

- Is Newton open, invite-only, or a normal trial?
- Which providers and platforms are current?
- Is the 40K proof historical or current?
- Which price and entitlement apply?
- Where is the current changelog?

For Tecotype, assuming the client and billing system work, marketing should own
a synchronized state registry for every public surface and a source-token
contract with downstream systems. A campaign is countable distribution only
when those systems return coarse activation, paid, and retained events without
mailbox content.

## Funnel assessment

Strong:

- durable branded discovery;
- low-friction store presence;
- recognizable professional workflows;
- historical social proof;
- direct emotional acknowledgment of trust damage; and
- a clear annual price on several public surfaces.

Weak or unobservable:

- conflicting trial, purchase, and request-access states;
- inconsistent provider/platform scope;
- dead changelog route;
- undated legacy subscriber proof;
- no visible source continuity into stores or the client; and
- no public activation, paid-conversion, retention, or renewal cohorts.
