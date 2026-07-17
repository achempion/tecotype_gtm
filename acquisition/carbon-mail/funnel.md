# Public funnel

Carbon Mail changed from a waitlist and manually approved Google test users to
a direct Gmail-connect flow. The current path was followed until Carbon
instructed the user to proceed through Google's unverified-app warning. No
Google account was authorized.

## January 2026: waitlist and test users

The [January 16 founder
post](https://www.reddit.com/r/StartupsHelpStartups/comments/1qe8kvh/15_17_built_a_working_product_750_requirement_for/)
described:

- a working beta used by the founders;
- a handful of testers, mostly friends and family;
- Google's 100-test-user limit;
- a website waitlist;
- manual addition of approved test users;
- an expected CASA assessment before a broader launch.

The public path was:

```text
Founder Reddit post
→ landing page
→ waitlist request
→ manual Google test-user approval
→ Google authorization
→ browser product
→ activation and retention unknown
```

The January 19 discussion shows that this path did not work consistently.
Visitors reported that the page failed on iPhone, the waitlist did not work,
and the desktop demo was missing. The founder said the mobile layout was fixed
the next day. No before-and-after conversion evidence is public.

## Current public path

Observed on 2026-07-17:

1. The homepage offers “Get Started,” “Sign In,” and “Connect Gmail.”
2. All three links point to `/login`.
3. `/login` says “Welcome to Carbon” and asks the user to connect Gmail.
4. The page says Carbon accesses only email metadata for labeling and does not
   store email content on its servers.
5. Selecting “Connect Your Gmail” opens Carbon's own “Security Check.”
6. The modal says Google will show “This app isn't verified.”
7. It instructs the user to choose “Advanced,” then “Go to Carbon Mail
   (unsafe).”
8. A checkbox must acknowledge that this is normal before “Continue to
   Google” becomes enabled.
9. An expandable explanation says Carbon is undergoing Google's CASA Tier 2
   review.
10. The research stopped before continuing to Google. No account, mailbox,
    permission grant, or personal data was used.

The current path is therefore:

```text
Reddit, directory, brand search, or direct visit
→ broad time/privacy landing page
→ untagged /login CTA
→ Connect Your Gmail
→ Carbon security explanation
→ acknowledge an expected Google warning
→ Google unverified-app path [not crossed]
⋯ consent to Gmail permissions [not observed]
⋯ sync and onboarding [not observed]
⋯ first categorized inbox [not observed]
⋯ activation, next-day return, and retention unknown
```

The public client bundle requests:

- `gmail.readonly`;
- `gmail.send`; and
- `gmail.modify`.

It also requests offline access and explicit account consent. Those scopes are
consistent with a full Gmail client, not the login page's narrow phrase “email
metadata for labeling.” A scope describes capability, not actual use.

## Offer and payment

The current homepage says:

- Carbon does not make money yet;
- optional power-user features may be added later;
- a robust, fully featured free tier will remain; and
- “a peaceful inbox shouldn't be a luxury item.”

There is no public pricing page, trial end, card step, paid tier, or checkout.
JSON-LD advertises a zero-dollar offer.

In January the founders considered preselling 15 lifetime licenses at $50 to
fund the compliance assessment. Public evidence does not show that this offer
was launched, accepted, or paid. It should be treated as a contemplated funding
mechanism, not Carbon's historical price.

Carbon therefore supplies no evidence about willingness to pay, paid
conversion, customer acquisition cost, or revenue retention. Its free access
is not linked to a current retention cohort. No public evidence shows whether
the earlier reported next-morning return to Gmail improved after the offer or
funnel changed.

## Instrumentation and attribution

The site loads Vercel Web Analytics. Homepage CTAs are untagged internal links,
and founder/community links found during research use the plain domain rather
than Carbon-controlled UTM parameters.

Vercel may record referrers and page activity. Public evidence does not show:

- a campaign taxonomy;
- a source handoff into the authenticated product;
- Gmail-connect completion events;
- first-value events;
- a day-one or day-seven cohort; or
- a source-to-retention report.

The installation of an analytics script does not prove that Carbon can connect
a Reddit visitor to retained product use.

## Friction and qualification

### Friction removed

- No current email waitlist.
- No manual invitation visible before OAuth.
- No price or card.
- One provider and one main CTA path.
- Browser delivery avoids an installer.

### Friction introduced or deferred

- The page makes Gmail the only supported provider.
- The user is asked to cross an unverified-app warning.
- Carbon's own instructions use Google's “unsafe” label.
- The footer privacy link returns 404.
- The page supplies no product screenshot or demo before authorization.
- The requested Gmail scopes are broader than the login reassurance suggests.
- Initial sync, model setup, classification quality, and first-value time are
  undisclosed.
- The public page promises future mobile companions but does not explain
  current responsive versus native access.

## Activation and retention boundary

Carbon does not publish an activation definition. Plausible events include:

- completing Google authorization;
- completing the first mailbox sync;
- seeing the first Decide, Act, Respond, and Review classification;
- completing an email action without opening the message;
- correcting a classification;
- composing or sending a message; or
- returning voluntarily the next workday.

These remain hypotheses. A waitlist request, Gmail connection, or positive
demo response is not activation.

The founders' January statement that users went back to Gmail the next morning
is the nearest public retention evidence. It has no cohort size, denominator,
measurement method, or percentage. Nine days earlier the founders described
only a handful of mostly friends-and-family testers, so it is unsafe to infer a
representative retention rate.

## Implication for Tecotype

Tecotype should not expose a public Gmail/download funnel until:

```text
accurate public promise
→ Apple Silicon download
→ usable first run
→ approved Gmail or secure generic IMAP connection
→ first sync
→ source-matched keyboard or search value
→ voluntary next-day return
→ retained use
```

Current source inspection found that Tecotype's no-account onboarding,
licensing/payment, and Gmail audit remain launch work, and proper reply sending
is not complete. These are release gates, not acquisition copy.

The Carbon lesson is not to force return through a redirect. It is to measure
whether a qualified user reaches value without founder rescue and chooses
Tecotype again the next day.
