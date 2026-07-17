# Orchid landing-page research

Captured **2026-07-17** from:

- [`https://0.email/`](https://0.email/), the Zero-to-Orchid transition page;
- [`https://orchid.ai/`](https://orchid.ai/), the current Orchid homepage;
- [`https://0.email/about`](https://0.email/about), the residual Zero about
  page; and
- [`https://0.email/pricing`](https://0.email/pricing), the residual Zero
  offer page.

The in-app browser was unavailable. Findings therefore come from public search
extraction, server-delivered HTML and metadata, and public response headers,
not an interactive rendered-DOM inspection.

## The transition page at `0.email`

The current crawler-visible page says:

> 0.email is now Orchid.

It describes the earlier product as a fast open-source inbox and the new
product as an executive assistant spanning inbox, calendar, meeting
preparation, and follow-ups. It exposes three routes:

1. **Meet Orchid**, leading to the current product;
2. **Sign in to Zero**, preserving legacy access; and
3. **GitHub**, displaying a live-looking star count.

The server-delivered HTML does not contain that visible transition copy. It is
a client-rendered app shell whose metadata still says “Zero” and describes
“the first open source email app.” This creates an observable metadata/message
mismatch:

```text
search-visible body
→ Orchid rebrand

server HTML title and description
→ legacy Zero email client
```

The mismatch can fragment search snippets, social previews, and category
expectations even if the interactive page is clear.

## The current Orchid homepage

The current [homepage](https://orchid.ai/) leads with “Meet Orchid, your
personal assistant” and says the product works through messages. Its sequence
is:

- assistant demonstration in an iMessage-like conversation;
- connection to a broad tool stack;
- recurring habits and personal routines;
- administrative work such as inbox triage, replies, calendar, bills, and
  forms;
- proactive reminders; and
- long-term personal memory.

Every inspected **Get Started** link in the delivered homepage uses
`sms:+14152999916`. The desktop **Login** link uses:

`https://app.orchid.ai?source=site&utm_source=site&utm_campaign=login`

The navigation also exposes:

- an Enterprise Typeform;
- blog and case-study pages;
- Discord, LinkedIn, and X;
- Gmail, Google Calendar, Google Drive, Granola, and Sentry links; and
- a current SMS-first World Cup campaign.

No SMS, form, login, or account route was opened.

## Audience and message map

| Question | Evidence | Classification |
| --- | --- | --- |
| Who is it for? | The homepage addresses individuals; the [beta post](https://orchid.ai/blog/orchid-beta-is-here) names founders, sales teams, real-estate agents, operators, agency owners, and recruiters | **Observed** |
| What triggers interest? | Administrative coordination, follow-ups, calendar work, remembering details, and carrying work in one's head | **Observed** |
| What is the promise? | Work is handled through messages, with the user approving what matters | **Observed** |
| What is the mechanism? | Connections to inbox, calendar, chat, documents, CRM, and other tools | **Observed**, exact behavior not tested |
| Emotional angle | Relief, status, attentiveness, delegation, and personal care | **Observed/inferred** |
| What is the proof? | One named homepage testimonial, message demonstrations, one published agency case study, YC association, and legacy Zero visibility | **Observed**, outcomes are first-party |
| What is the offer? | SMS start, app login, and Enterprise Typeform; no visible public plan amount | **Observed** |
| What happens after CTA? | Unknown because SMS, login, Typeform, integrations, and checkout were not entered | **Unobservable** |

The current story is not “a better inbox.” Email is one input to a general
assistant. That distinction matters when comparing the current offer with
Zero's email-client launch history.

## Demonstration and proof

The homepage's strongest marketing device is a concrete conversation. It
shows a travel request becoming options, payment, calendar entry, and
itinerary. Other sections show example commands for daily news, weather,
calorie tracking, medication, and flight check-in.

The [agency case study](https://orchid.ai/case-studies/agency-owners) names a
solo fractional DevRel agency and claims zero time spent preparing for
meetings. It describes a flow from email, Slack, and Granola into a text
brief. This is useful qualitative proof, but it is a single first-party story,
not an independently measured cohort.

The public [sitemap](https://orchid.ai/sitemap.xml) listed one case study and
thirteen dated blog posts. The blog moved from AI-application and inbox-zero
essays toward executive-assistant economics, coordination work, product
integrations, SMS voice notes, and personal-life use cases.

## Technical and measurement evidence

Server-delivered evidence showed:

- Next.js on `orchid.ai`;
- a `PostHogAnalytics` component name in the page payload;
- a source- and campaign-tagged Login destination;
- an SMS primary CTA without an observed source token;
- an external Enterprise Typeform;
- Open Graph, Twitter, robots, and canonical metadata for `orchid.ai`;
- no visible cookie or consent interface in the delivered HTML; and
- no public price content on the `/pricing` response beyond navigation and
  footer links.

The PostHog component proves analytics capability, not which events fire or
whether the data is useful. The lack of a visible consent interface in static
HTML does not rule out regional, rendered, server-side, or app-level consent.

The `0.email` app shell was served through Cloudflare. `orchid.ai` identified
Next.js and Railway-related response headers behind Cloudflare. Hosting
details do not establish acquisition performance.

## Residual Zero pages

The [Zero about page](https://0.email/about) still describes an AI email
client and claims more than 15,000 early-access signups in under three months.
The [Zero pricing page](https://0.email/pricing) still presents Free, Pro, and
Enterprise plans, including a seven-day Pro trial. These pages belong to the
legacy email-client offer and must not be presented as current Orchid pricing.

## Landing-page assessment

Strong:

- concrete demonstrations;
- a primary CTA repeated consistently on the current homepage;
- an emotionally distinct “delegation” story;
- owned editorial and case-study surfaces; and
- at least one tagged login route.

Weak or uncertain:

- category, domain, and offer discontinuity between Zero and Orchid;
- legacy metadata on `0.email`;
- no visible current plan amount;
- mixed consumer, professional, and enterprise audiences;
- primary SMS links without visible source parameters; and
- no public evidence of CTA-to-activation or paid conversion.

For Tecotype, the useful lesson is to demonstrate one complete email outcome,
but retain an explicit desktop-email category and a continuous attributed
path from the first public mention to payment.
