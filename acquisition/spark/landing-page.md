# Spark Mail landing page, offer, and public implementation

Captured: **2026-07-17**

Primary source: [sparkmailapp.com](https://sparkmailapp.com/)

Inspection boundary: The public homepage, pricing, about, privacy, help,
feature, and migration pages; response headers and initial HTML; public store
metadata; and a rendered homepage were inspected. The rendered state was used
to verify the message order, Free download and Buy now routes, platform links,
security section, and visible cookie-choice dialog. No CTA was clicked. In
particular, `/download` was not opened because it can initiate delivery of a
platform installer. No client artifact, account, trial, form, demo, or checkout
was accessed.

## Current promise

The homepage title and H1 are both:

> Smart. Focused. Email.

The supporting line says:

> Fast, cross-platform email designed to filter out the noise - so you can
> focus on what's important.

The two hero actions are:

- **Free download**, linked to `/download`;
- **Buy now**, linked to `/pricing`.

This is a more singular lead than Spark's complete feature set suggests. It
combines:

1. a product idea: intelligence and prioritization;
2. an emotional benefit: focus;
3. a performance claim: fast;
4. a distribution claim: cross-platform;
5. a direct free-versus-paid decision.

The words overlap Tecotype's territory, but the emotional contract differs.
Spark soon expands into “true productivity,” “master your inbox,” AI
assistance, meetings, team collaboration, and integrations. Tecotype can
remain quieter and more precise rather than compete for the same generic
“focused email” phrase.

## Page sequence

The observed homepage follows this structure:

| Section | Public message | Acquisition job | Evidence limit |
| --- | --- | --- | --- |
| Hero | “Smart. Focused. Email.” | Establish a simple category promise | “Smart” and “focused” are broad and widely claimed |
| Entry actions | Free download / Buy now | Route free and paid intent immediately | Post-click behavior was not tested |
| Platform row | Windows, Android, Mac, iPhone, iPad, Apple Watch | Demonstrate cross-device breadth | Does not establish feature or quality parity |
| Scale proof | 4.8, 154K ratings, Editors' Choice, 19.5 million downloads | Reduce adoption risk | Aggregate definitions and periods are absent |
| Prioritize / Organize / Focus | Priority, Pin, Group by Sender, Done, Set Aside, Send Later, Reminders | Turn the promise into workflow examples | No measured time or attention outcome |
| Inbox control | Home Screen, Smart Inbox, newsletter and notification grouping | Show a visible filtering system | User fit and classification quality are private |
| AI | Assistant, writing, translation, summaries | Expand the premium productivity story | Data processing and quotas require separate explanation |
| Accounts | Gmail, IMAP, iCloud, Exchange, Outlook, Yahoo, Google | Reduce provider-fit uncertainty | Setup success and sync quality are not public |
| Teams | Shared drafts, thread comments, delegation, shared work | Create a team expansion route | Cases do not reveal conversion or retention |
| Security and privacy | Security, encryption, Google Cloud, no third-party sharing | Address a high-risk decision | Homepage wording compresses material policy exceptions |
| Repeated CTA | Free download | Convert product understanding into distribution | Installer route was deliberately not opened |

The page uses screenshots, workflow demonstrations, ratings, publisher logos,
and a user quote attributed to Octavian Maxim. The visible press-logo row
includes TechCrunch, Lifehacker, Mashable, The Verge, and Fast Company. A logo
or quoted line establishes public association, not current endorsement,
traffic, procurement, or downstream results.

## Product and platform proof

Spark's public platform links and store records support current availability
on:

- Windows 10 or later through direct distribution and Microsoft Store;
- macOS through a current Spark Desktop app;
- macOS through the separately maintained Spark Classic app;
- iPhone, iPad, and Apple Watch;
- Android.

Public Apple metadata showed:

| Listing | Initial release | Current version | Current update | Requirement | US rating |
| --- | --- | --- | --- | --- | ---: |
| [Spark Mail: AI Email Assistant](https://apps.apple.com/us/app/spark-mail-ai-email-assistant/id997102246) | 2015-05-29 | 3.19.20 | 2026-07-15 | iOS 16.4+ | 4.62744 from 82,019 ratings |
| [Spark Classic](https://apps.apple.com/us/app/spark-classic-email-app/id1176895641?mt=12) | 2016-11-30 | 2.11.64 | 2026-06-17 | macOS 10.13+ | No current US rating returned |
| [Spark Desktop](https://apps.apple.com/us/app/spark-mail-ai-email-inbox/id6445813049?mt=12) | 2023-08-31 | 3.30.1 | 2026-07-15 | macOS 12+ | No current US rating returned |

Google Play's public [Spark listing](https://play.google.com/store/apps/details?id=com.readdle.spark&hl=en-US)
showed 1M+ downloads, 4.1/5 from 88.4K reviews, and an update on
2026-07-07.

Spark's homepage says **4.8 from 154K ratings**. The current US iOS and Android
counts together exceed 154K, while their visible scores differ. The homepage
figure may use a different set of platforms, dates, markets, or weighting, but
the method is not stated. It should be treated as an undefined first-party
aggregate rather than reconciled into false precision.

The [current migration explanation](https://sparkmailapp.com/blog/spark-vs-spark-classic)
says Spark Classic remains supported with occasional maintenance and bug
fixes, while new features go to Spark Desktop on Mac and Windows. The two can
run side by side and preferences can be transferred. Current store updates
corroborate maintenance of both in June and July 2026.

This is honest migration documentation, but the product split creates
decision-stage work:

- Which Mac app should a new person choose?
- Which Classic behavior has reached Spark Desktop?
- What does “supported” mean over time?
- Which review applies to which product generation?

Tecotype should avoid creating this ambiguity around its first public release.

## Current offer and pricing

The public [individual pricing page](https://sparkmailapp.com/pricing) presents
four levels:

| Plan | US price | Public role | Important qualification |
| --- | ---: | --- | --- |
| Free | $0 | Core multi-account email, Smart Inbox, notifications, calendar, and essential productivity | Functional acquisition tier, not merely a time-limited demo |
| Plus monthly | $10/user/month | Productivity, Spark +AI, AI Assistant, integrations, templates, team essentials, 40 AI Meeting Notes | True monthly billing |
| Plus annual | $99/user/year, displayed as $8.25/month | Discounted Plus commitment | Compared with a $120 annualized monthly total |
| Pro monthly | $20/user/month | Read statuses, advanced team collaboration, unlimited AI Meeting Notes, HubSpot, Spark CLI triage access | True monthly billing |
| Pro annual | $199/user/year, displayed as $16.58/month | Discounted Pro commitment | Compared with a $240 annualized monthly total |
| Enterprise | Contact sales | Security, controls, customer success, and coaching | No public price |

The page labels annual Plus as a 17% saving. Localized prices can differ; a
rendered Denmark state showed euro annual pricing. The US values above are
used for the report's US market.

The page and FAQ also say:

- Plus and Pro can be tried for seven days when subscribing directly in the
  app;
- support can sometimes change or extend the starting day;
- one Spark Account carries a subscription across supported platforms;
- AI is disabled by default;
- AI use has quotas, with additional credits available for purchase;
- existing Premium subscribers retain their legacy plan;
- personal and team subscriptions use related but separately framed pricing.

Current Pro rows mark **Workflows**, **Auto-Labels**, and **Auto-Drafts** as
**SOON**. They are acquisition promises for future delivery, not currently
shipped capabilities.

The inspected pricing HTML exposed Stripe checkout links for monthly and
annual Plus and Pro. Their destinations were recorded from `href` attributes
but not opened.

## Privacy and security message

The homepage says:

> Spark guarantees security and data privacy. Your data is solely used for
> product optimization and is never shared with third parties. Data storage
> and encryption is secured through Google Cloud service.

The first and third sentences are broad. The middle sentence is materially
overcompressed relative to Spark's detailed
[app privacy policy](https://sparkmailapp.com/legal/privacy-app) and
[privacy help](https://sparkmailapp.com/help/privacy-data/spark-email-privacy-everything-you-need-to-know).
Those sources describe legitimate sharing and processing through service
providers, integrations, analytics systems, AI providers, payment providers,
and legal authorities.

The detailed public account is more useful:

- email and calendar data are primarily processed on-device;
- Spark stores app-specific OAuth tokens for Gmail, Outlook, and Yahoo;
- for AOL, Exchange, and generic IMAP, an encrypted stored access credential
  may be an email login and password;
- push delivery can temporarily store encrypted subject or message content,
  deleted after four hours;
- server processing supports shared mail, shared drafts, Send Later,
  comments, read statuses, meeting notes, and related features;
- backups are made daily and typically retained for one week in Google Cloud
  SQL;
- recent emails, shared links, large attachments, read statuses, and account
  data have feature-specific retention periods;
- technical and product data can include identifiers, IP-derived location,
  device and settings data, screen/click events, feature and trial activation,
  and crash logs;
- data can be processed in the United States and European Economic Area.

The public Apple privacy label for Spark Desktop described several categories
as linked to identity, including support content for marketing and email/name,
message content, and device identifiers for app functionality. Google Play's
Data Safety label said the app may share Financial info, App activity, and
other categories, and may collect Personal info, Financial info, and other
categories. Store labels are developer declarations, but they reinforce the
need for qualified language.

“Never shared with third parties” should therefore not be repeated literally
as a complete description. A narrower formulation such as “not sold and not
used outside stated product, service-provider, integration, payment, and legal
purposes” would be more consistent with the policy.

## AI data-flow qualifications

Spark's [AI Assistant page](https://sparkmailapp.com/features/ai-assistant) and
privacy sources say:

- AI is opt-in;
- some models can run on-device;
- hosted providers can include Azure OpenAI, OpenAI, Anthropic Claude, and
  Google Vertex AI, with Spark able to switch providers;
- submitted material is not used to train those models;
- providers may retain inputs for up to 30 days for misuse monitoring;
- the Assistant builds a local index and sends a query plus a small number of
  relevant emails, not the entire inbox, to a provider;
- My Writing Style selects sent-mail samples, sends them for analysis, and
  stores samples and a style description in Spark's backend;
- Meeting Notes records audio on-device, sends audio for transcription, and
  stores the resulting transcript and summary in the Spark Account; providers
  may retain audio for up to 30 days;
- personalization context can include role, location, timezone, workflow,
  contacts, schedule, industry, projects, and interests, and can be deleted.

Three claims must remain distinct:

1. a local index is not the same as wholly local inference;
2. “not used for training” does not mean “never leaves the device”;
3. Spark not storing a source item does not mean a contracted provider has no
   temporary retention.

Tecotype's optional Better search has a narrower job and runs on-device. It
should describe that concrete path without implying that mail never reaches
the person's email provider.

## Public measurement and experimentation

The initial HTML, response headers, and rendered page exposed:

- a first-party `spark_conv_r` cookie with source, medium, initial source,
  initial medium, and campaign fields, set for one year even on a direct visit;
- Google Tag Manager container `GTM-TR9K2WV`;
- Google consent mode defaulting `ad_storage` and `analytics_storage` to
  `denied`, with a 500 ms wait and ad-data redaction;
- a public page-view event named `ev_page_view`;
- UTM source, medium, and campaign metadata;
- Free download events named `ev_free_download` and
  `Free Download Clicked`;
- Buy now events named `ev_buy_now` and `Buy Now Clicked`;
- pricing events named `Checkout Clicked` and `ev_checkout_event`, with
  product, plan, monthly/annual, and element-position fields;
- Amplitude and an exposed public project key;
- Tailor AI experimentation code connected to Amplitude;
- Google, Meta, cookie-management, first-party Spark, Amplitude, and Tailor
  script hosts in the rendered page.

The rendered page showed a cookie dialog with **ACCEPT ALL** and **MANAGE
COOKIES**. It was not interacted with.

This is unusually direct evidence of an acquisition-measurement design:

```text
source persistence
→ page view
→ free-download or buy-now choice
→ plan and billing-cadence checkout event
→ client/store/payment handoff
```

It does not disclose:

- consent choices or whether each script transmitted data;
- event counts or deduplication;
- source recovery after store installation;
- activation definitions;
- experiment assignments or results;
- revenue or retention.

## Organization and proof

Spark's [about page](https://sparkmailapp.com/about) identifies Readdle as the
company behind Spark and other productivity products. It says Readdle is
privately held, has more than 300 people across 30 countries, has exceeded
200 million downloads across its portfolio, and has taken no external funding.

These are first-party company-scale statements. The 200 million figure applies
to Readdle's product portfolio, not Spark, while Spark's 19.5 million figure is
the product-specific homepage claim.

Public [case studies](https://sparkmailapp.com/case-study) include executives,
assistants, freelancers, businesses, and DALI Lab's 100-plus-student
environment. They demonstrate use cases but often lack measured before/after
outcomes. A case whose slug references Zapier describes a freelance writer who
worked with Zapier and other clients; it should not be represented as a Zapier
corporate endorsement.

## What Tecotype should take from the page

- Keep one emotional promise dominant and use concrete workflow proof.
- Make Free versus paid entry clear, but do not put future features into the
  current paid-value calculation.
- Persist acquisition source only as far as privacy and user benefit justify,
  then measure provider readiness and first value rather than CTA clicks.
- Put data-flow qualifications beside privacy claims.
- Maintain one clear desktop product path and one release-truth page per
  platform.
- Treat ratings, downloads, company scale, and case studies as defined
  evidence, never interchangeable audience proof.
- Preserve Tecotype's distinction: calm control, keyboard speed, and on-device
  retrieval are more specific than another “smart, focused” suite.
