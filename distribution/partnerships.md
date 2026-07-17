# Tecotype provider endorsements and distribution

Status: Working program design; no provider is endorsed or confirmed and no
distribution relationship is agreed.
Last reviewed: 2026-07-18

## Primary model: independent provider endorsements

Tecotype independently selects a deliberately small number of email providers
that deserve support. Each endorsed provider receives a permanent public review
explaining the decision and one mailbox on its approved infrastructure can be
used in Tecotype for free.

Endorsement does not require an agreement. Tecotype asks the provider in
advance to confirm connection facts, permit logo use, and supply a contact for
future endpoint changes. That consent makes the review provider-confirmed; it
does not make the provider a partner, give it editorial control, or imply that
it endorses Tecotype.

The provider may then link to its review from setup documentation, onboarding,
mailbox creation, or the customer dashboard. A permanent provider-controlled
link creates distribution. Tecotype can publish and maintain the endorsement
even when the provider does not link.

The offer:

- One authenticated mailbox on any currently endorsed provider infrastructure
  can be used in Tecotype for free.
- Its aliases still count as the same mailbox, and the user may replace the
  eligible mailbox.
- A second account, or an account outside endorsed infrastructure, requires
  Tecotype Individual.
- Tecotype owns client support. The provider remains responsible for its
  mailbox service, credentials, DNS, deliverability, quota, and incidents.

This is a provider-specific entitlement, not a general free plan and not
payment for an inbound link. Removing a provider from the endorsed set stops
new free activations under a published transition policy; treatment of
existing users must be decided before launch.

There are two possible paths:

```text
Tecotype provider directory
→ independent provider review
→ create a provider account or connect an existing one
→ one provider mailbox in Tecotype, free
```

```text
provider signup, documentation, or dashboard
→ provider-specific Tecotype review
→ one provider mailbox in Tecotype, free
→ add Gmail, work mail, or another account
→ Individual
```

Tecotype infrastructure never receives mailbox credentials or contents.
Providers link to Tecotype's signed desktop builds rather than repackaging
them.

## Program states

Use four explicit states:

1. **Compatible provider:** Tecotype can connect through standard IMAP/SMTP.
   Compatibility is not an endorsement and receives no provider-specific free
   entitlement.
2. **Endorsed provider:** Tecotype has tested the service and independently
   determined that it meets the published ownership, privacy, standards, and
   support criteria. It receives a full review and the one-mailbox entitlement.
3. **Provider-confirmed endorsement:** The provider has confirmed technical
   details, permitted the agreed brand use, and named an update contact. The
   endorsement remains Tecotype's opinion.
4. **Distribution provider:** The provider also gives Tecotype permanent,
   attributable pre-install discovery on a provider-controlled surface.

No provider may buy an endorsement or obtain one by applying. Confirmation,
linking, or promotion does not guarantee continued inclusion. Keep no more
than five active endorsements at launch and renew each editorial decision
annually.

Only the fourth state counts as distribution under this workspace's
definition. Public pages must disclose confirmation, inbound links, payments,
or other material relationships without implying reciprocal endorsement.

## Independent provider review

Every endorsed provider receives a stable page such as
`tecotype.com/providers/nubo`. It serves two audiences:

- a Tecotype visitor deciding whether the provider deserves their business;
- an existing provider customer arriving to connect one mailbox for free.

Call it an independent review, not an audit. “Audit” can imply formal assurance
or exhaustive certification beyond what Tecotype performs.

The page should include:

1. Why Tecotype endorses the provider.
2. Ownership, funding, governance, and named operators.
3. Mail privacy, retention, public-site tracking, and subprocessors.
4. IMAP/SMTP interoperability and the behavior Tecotype tested.
5. Support scope, export path, limitations, and unresolved concerns.
6. Test date, review date, primary sources, and a visible change history.
7. “Connect one [Provider] mailbox to Tecotype for free.”
8. A direct, non-affiliate provider signup link unless another relationship is
   clearly disclosed.

Use a disclosure near the title:

> This is an independent review by Tecotype. [Provider] confirmed the
> connection settings and permitted use of its logo, but does not control our
> conclusions. No payment was made for inclusion.

When applicable, add:

> [Provider] links to this page from its website. This does not affect
> Tecotype's assessment.

The provider may correct facts and supply current primary evidence. It cannot
approve, edit, or veto Tecotype's conclusions. Tecotype may update or withdraw
the endorsement even while an inbound link exists.

Use the provider name in text before consent. Display its logo only after
written permission or under brand terms that clearly allow this use. Never use
“official,” “approved by,” or “partner” unless the corresponding relationship
is true and disclosed.

### Provider confirmation

A normal written reply is enough for the first version. Ask the provider to:

1. Confirm its legal name and current ownership/funding statement.
2. Confirm canonical IMAP and SMTP endpoints, ports, TLS modes, authentication,
   autoconfiguration domains, aliases, and custom-domain behavior.
3. Permit use of its name and logo on the review and inside the provider
   directory, and provide the preferred asset or brand rules.
4. Confirm that Tecotype may offer one free mailbox connection when a user
   authenticates through the approved provider definition.
5. Name a technical contact and make reasonable efforts to report endpoint,
   authentication, service-domain, or ownership changes.
6. Confirm the factual support boundary: Tecotype supports the client; the
   provider supports the email service.

Do not ask the provider to approve the editorial recommendation. “Confirmed by
provider” refers only to enumerated facts and permissions.

## Endorsement gate

An endorsed provider must:

1. Sell a real mailbox service with direct, standards-based IMAP and SMTP. A
   bridge, forwarding-only service, or provider-specific client is not enough.
2. Be independent and customer-funded. Verify the current owner and obtain a
   direct written statement that the provider has taken no venture capital or
   other financial investment that controls its decisions.
3. Fund the service through customers rather than advertising, mailbox
   profiling, or sale of personal data.
4. Publish comprehensible privacy, retention, legal-request, and subprocessors
   information.
5. Use no advertising, cross-site, or behavioral tracking on its public
   website. Functional session cookies are acceptable. Disclosed, first-party,
   cookie-less aggregate analytics are acceptable but rank below no analytics.
6. Provide human support with honest scope and availability, usable
   documentation, and an incident escalation path. A small team does not need
   to promise 24/7 support.
7. Let users leave through standard export or IMAP without a proprietary
   lock-in path.
8. Pass Tecotype interoperability testing and provide a stable technical
   contact for endpoint or behavior changes.

Founder personality, public writing, open-source work, and principled positions
are strong preferences. They do not compensate for weak ownership, privacy, or
support evidence.

Personal use by Tecotype's founder is useful evidence, not a qualification by
itself. Disclose it on the provider review and test against the same criteria.

Recheck ownership, funding, privacy policy, public-site tracking, endpoints,
support terms, and product behavior every year and after any acquisition.
Remove the endorsement plainly when the provider no longer qualifies and
record the reason in the review history. Publish the effect on existing free
entitlements before the program launches; do not depend on a provider agreement
for this policy.

### Compatibility test

Test with a paid production account before endorsement:

- automatic and manual setup;
- TLS and authentication, including an app password when 2FA is enabled;
- initial and incremental sync, folder discovery, and special-use folders;
- archive, restore, move, delete, spam, and read-state behavior;
- SMTP submission and the Sent-folder append path;
- aliases and custom domains without counting an alias as another account;
- rate limits, large mailboxes, disconnects, and credential failure;
- import/export documentation and provider support escalation.

Record the tested plan, endpoints, date, and known limitations. “Uses IMAP” is
compatibility evidence, not an endorsement.

## Distribution gate

Ask first: **If Tecotype had no users, would this provider still introduce it
to existing customers because Tecotype improves the provider's offer?**

Proceed only when:

1. Customers can discover Tecotype before choosing or installing a client on a
   permanent provider-controlled surface such as setup documentation,
   onboarding, mailbox creation, or the account dashboard.
2. The provider links to its Tecotype review or another dedicated Tecotype
   destination and confirms the placement and support boundary in writing.
3. A privacy-respecting path can measure discovery → install → first provider
   account → second account → paid.
4. A named contact and a 30- or 90-day review are agreed before launch.

The independent review, provider confirmation, standard compatibility, or a
launch post alone does not count as distribution. They remain worthwhile
editorial and acquisition work.

### First-contact offer

Lead with the completed research and the benefit to the provider:

> Tecotype would like to independently recommend [Provider], maintain its
> desktop-client configuration, and let your customers connect one mailbox for
> free. Could you confirm the settings and ownership facts, permit logo use,
> and name a contact for future changes? We have prepared a dedicated review
> page. If you are comfortable with it, would you link to it permanently from
> your client setup, onboarding, or account area? Tecotype provides all client
> support.

No payment, exclusivity, reciprocal endorsement, or formal contract is needed
for the review. Make clear that the page can exist without the link and that
the provider is confirming facts rather than approving the conclusion.

## First outreach

These are research candidates, not current Tecotype endorsements. The order
starts with the clearest values-led pilot, then tests increasingly established
distribution surfaces. Complete one review and confirmation cycle before
expanding the public set.

| Order | Provider | Why it fits | Public-site privacy and support | GTM and entitlement assessment |
| --- | --- | --- | --- | --- |
| 1 | [Nubo](https://nubo.coop/) | A Belgian social cooperative building user- and community-controlled email and cloud services with free-software roots. Its [CHATONS profile](https://www.chatons.org/index.php/chatons/nubo) and [2025 operating profile](https://economiesociale.be/fil_actu/nubo-le-mail-et-cloud-belge-qui-se-construit-pas-a-pas-avec-sa-communaute/) describe direct community support, roughly 800 users and 1,000 cooperators, and named operators. | Nubo publicly rejects advertising and tracking, but complete the live website, policy, support, retention, and mailbox test before publishing a review. Canonical IMAP/SMTP endpoints were not confirmed in the initial research. | Best first values-led review. Prepare the independent page, then ask Nubo to verify ownership and settings, permit logo use, name an update contact, and link permanently from its client setup or member onboarding if comfortable. Its modest reach is acceptable: the pilot tests trust and cooperation before scale. |
| 2 | [Runbox](https://runbox.com/) | [Independent and employee-owned](https://runbox.com/why-runbox/) in Norway. Its subscription model, long operating history, open-standards position, and existing [recommended email programs](https://help.runbox.com/email-programs/) page fit the program. | Runbox [states](https://runbox.com/why-runbox/privacy-protection/) that it uses no tracking cookies or third-party analytics and offers personal support seven days a week. Its [documented settings](https://help.runbox.com/email-program-settings/) use the fixed `mail.runbox.com` endpoint for IMAP and SMTP. | Clearest existing client-discovery surface. Ask it to confirm the review and add a permanent, dedicated Tecotype link in signup, onboarding, the account dashboard, or client guidance. |
| 3 | [Migadu](https://migadu.com/) | Migadu [describes itself](https://migadu.com/about/) as a small, bootstrapped, independent Swiss company started by Michael Bruderer and Dejan Strbac, with no investment taken. Its opinionated writing about standards and local clients supplies the clearest founder-like personality in the shortlist. | Its [privacy policy](https://migadu.com/privacy/) says it uses no tracking or analytics cookies and no behavior analytics. Support comes directly from its postmasters, with plan-specific availability stated in [pricing](https://migadu.com/pricing/). Its [guides](https://migadu.com/guides/index.html) specify `imap.migadu.com` and `smtp.migadu.com`. | Strong audience overlap with developers, freelancers, and operators managing several domains and mailboxes. Custom domains make endpoint-based eligibility essential. Ask for a dashboard or post-setup client choice; a help guide alone is useful but weaker distribution. |
| 4 | [Mythic Beasts](https://www.mythic-beasts.com/) | Founder-, employee-, and former-employee-owned hosting company with no external investors, more than 25 years of operation, human technical support, and a visible technical voice through Pete Stevens. Its low-cost email-only service supports many mailboxes and addresses. | Its [privacy policy](https://www.mythic-beasts.com/static/documents/privacy-policy.pdf) says the public site uses only necessary cookies. Confirm the scope and retention of server and subject-line logging during diligence. Email uses fixed `mail.mythic-beasts.com` and `smtp-auth.mythic-beasts.com` endpoints. | Strong independent-hosting audience and an established domain/customer dashboard. Ask for a provider review link from email setup and account management. Verify the exact ownership statement, support boundary, and email-only customer reach. |
| 5 | [Uberspace](https://uberspace.de/en/about/) | A small, owner-managed German team with unusually clear personality, pay-what-you-can pricing, open technology, and direct human support. | Its [privacy page](https://uberspace.de/en/about/privacy/) says the public site uses no cookies or external tracking and runs self-hosted, anonymous Umami analytics. The [mail manual](https://manual.uberspace.de/mail-access/) documents IMAP/SMTP, but endpoints are tenant-specific Uberspace hostnames. | Excellent values and developer fit. It needs a provider-signed definition for tenant-specific hosts rather than a fixed hostname allowlist. Ask for a permanent link from the mail manual or dashboard after a safe entitlement method is agreed. |
| 6 | [ServerMX](https://www.servermx.com/en/about-us/) | Independent Sardinian provider founded by Antonio Cordeddu in 2012. It calls itself an email artisan, names the founder, and promises answers from real people rather than autoresponders. | Its [privacy policy](https://www.servermx.com/en/utility/privacy-policy/) discloses one functional session cookie and locally hosted, anonymized Matomo analytics. It [states](https://www.servermx.com/en/contacts/) a two-hour office-time response target. Its [client configuration](https://www.servermx.com/en/help/howto/email-client/client-configuration-with-encryption/) uses `imap.servermx.com` and `smtp.servermx.com`. | Strong small-provider fit and simple entitlement detection. Ask for mailbox-creation or account-dashboard placement after the first review establishes the workflow. Verify active paid desktop reach and second-account propensity. |

Start with Nubo. It is the clearest expression of why the endorsement program
exists. Then approach Runbox and Migadu as contrasting distribution tests:
Runbox has the strongest existing client-discovery surface, while Migadu has
the strongest multi-domain operator fit. Do not publish all candidates merely
because they reply.

## Diligence queue

| Provider | Reason to continue research | Missing or conflicting evidence |
| --- | --- | --- |
| [mail.coop](https://mail.coop/about) | A UK cooperative email provider run through Innovation Cooperative Limited by three worker cooperatives. It presents itself as private, advertising-free, open-source, renewable-energy-hosted, and supported by real people. Its [terms](https://mail.coop/legal/terms-of-service) document direct IMAP/SMTP access. | Young and modest in reach, which is acceptable for a values pilot but limits near-term distribution. Review the live site and clarify the [privacy policy's](https://mail.coop/legal/privacy-policy) generic analytics language before endorsement. |
| [GreenNet](https://www.greennet.org.uk/node/4) | Not-for-profit ethical collective ISP established in 1985, owned by the GreenNet Educational Trust charity, with a long activist and anti-surveillance history. Its [email service](https://www.greennet.org.uk/internet-services/email) supports IMAP and SMTP with personal technical support. | Verify current ownership details, funding, public-site tracking, canonical endpoints, customer scale, and whether its NGO/activist audience has a meaningful desktop multi-account path. |
| [AltMail](https://www.altmail.se/) | Independent, subscriber-funded Swedish personal email with direct IMAP/SMTP, named technical culture, no webmail, and unusually explicit rejection of tracking, analytics, profiling, fingerprinting, and non-functional cookies. | Young service with unnamed operators and unclear legal identity. Its [terms](https://www.altmail.se/doc/terms-of-service.html) allow broad discretionary termination, support is scoped to three business days, and it does not support custom domains. Establish operating durability before endorsement. |
| [Mailfence](https://mailfence.com/) | ContactOffice Group [says](https://kb.mailfence.com/kb/who-are-we/) it has no third-party financial investors and keeps development and infrastructure in house. Cofounder Patrick De Schutter has a visible privacy-activist voice. Paid plans expose fixed `imap.mailfence.com` and `smtp.mailfence.com` endpoints. | The public privacy policy located in the initial review was last updated in 2021. Obtain current ownership, policy, tracking, support, and paid-desktop confirmation before endorsement. |
| [Posteo](https://posteo.de/en) | Its [company profile](https://posteo.de/en/site/about_posteo) describes an independent, self-financed German provider founded by Patrik and Sabrina Löhr, free of advertising and tracking and funded by more than 500,000 paid accounts. | Confirm canonical endpoints and current support directly. Its size, lack of custom domains, €12-per-year account price, and likely low second-account conversion make it values-aligned but weaker as the first distribution test. |
| [Forward Email](https://forwardemail.net/en/about) | Founder-owned, fixed [IMAP/SMTP endpoints](https://forwardemail.net/en/faq), fully published code, and a [privacy policy](https://forwardemail.net/en/privacy) that rejects third-party and persistent-identifier analytics. Nicholas Baugh is a visible technical founder. | Obtain written team-size and no-VC statements, separate paid mailbox users from the claimed 1.6 million hosted or forwarded domains, test ordinary-plan support, and review whether its superlative-heavy public claims meet Tecotype's endorsement standard. Small team does not mean small reach. |
| [Kolab Now](https://kolabnow.com/) | Independent Swiss service with an explicit [“no venture capital investments”](https://kb.kolabnow.com/documentation/why-kolab-now-is-the-right-thing-for-you) statement, fixed IMAP/SMTP endpoints, free-software roots, and a strong individual in FSFE founder Georg Greve. | Verify current ownership and website analytics, paid active users, support performance, and the disposition of the uncompleted Roundcube Next crowdfunding project before lending Tecotype trust. |
| [mailbox.org](https://mailbox.org/) | Fixed endpoints, [cookie-less self-hosted Matomo](https://mailbox.org/en/data-protection/), and a strong public founder in Peer Heinlein. | The [Heinlein Group](https://www.heinlein.group/en/) reports more than 150 employees and 325,000 customers, so it is beyond the preferred first cohort. Directly verify capital ownership. Consider later for reach, not as proof that the small-provider model works. |
| [Thexyz](https://www.thexyz.com/about/) | Explicitly employee-owned, no venture capital, no advertising or tracking, and led by visible founder Perry Toone. | Its main service uses shared Rackspace endpoints, which makes provider-specific entitlement ambiguous and raises a reseller-infrastructure question. Separate its newer self-hosted SOGo offer from the core service before deciding. |
| [StartMail](https://www.startmail.com/about-us/) | Founder-led, independently operated service with its own team and infrastructure, direct `imap.startmail.com` and `smtp.startmail.com` endpoints, and a public privacy position against third-party advertising and tracking. | Obtain a current direct no-VC and ownership statement. Its main privacy policy is old and a separate migration portal uses Google Analytics and remarketing, so clarify product and subprocessor boundaries. |
| [Fastmail](https://www.fastmail.com/company/values/) | Employee-owned, independent, customer-funded, advertising-free, standards-oriented, and personally used by Tecotype's founder. It offers product quality and compatibility evidence. | It is already large and popular, outside the preferred small-provider proof point, and its current public site uses analytics and cookies. Founder use must be disclosed. Keep it tested rather than endorsed until there is a distinct reason Tecotype should lend it scarce editorial attention and a meaningful permanent discovery path. |

## Hold

- **MXroute:** family-operated by Jarland and Christine Donnell, unusually
  strong founder voice, and transparent low-cost positioning. Hold because
  endpoints may be server-specific or customer-branded, the service sends
  order data to fraud-screening services, and its intentionally combative
  documentation and support terms may conflict with the “fair support” promise.
  Revisit only with a provider-signed entitlement and a mutually acceptable
  support boundary.
- **Purelymail:** sold by founder Scott Johnson to Add Rabbit LLC in March 2025.
  Its current $10-per-year offer and self-service support are transparent, but
  current capital ownership is not public enough for the no-VC gate and premium
  conversion is likely weak.
- **Greatmail:** a privately held provider with a useful client marketplace,
  but “privately held” does not prove no venture funding. Ownership,
  public-site tracking, individual desktop reach, and a visible operator remain
  unverified.
- **Neomailbox:** no convincing pre-client discovery surface is confirmed.
- [Soverin](https://press.thesharinggroup.com/253554-the-sharing-group-strengthens-portfolio-with-privacy-first-email-provider-soverin/)
  was acquired and is outside the intended independent cohort.
- **Tuta:** does not provide standard IMAP/SMTP access.
- **Proton Mail:** ordinary desktop-client access requires Proton Mail Bridge,
  so it does not fit the direct-provider-endpoint entitlement.
- **Disroot and Riseup:** values-aligned community services, but the
  commercial support, placement, and attributable paid-conversion exchange is
  absent.

Shared, tenant-specific, reseller, self-hosted, and customer-branded endpoints
need a provider-signed entitlement method. Do not approve arbitrary domains,
MX records, or user-entered server names.

## Entitlement and measurement

The free entitlement applies to one provider mailbox in total, not one mailbox
per endorsed provider:

- Both the incoming and submission connection must match an approved provider
  definition and complete a TLS-authenticated connection.
- An alias is not another account. A user may replace the qualifying mailbox.
- A custom-domain address qualifies when it authenticates through the
  provider's canonical endpoints.
- Adding any second account, including another endorsed provider, requires
  Tecotype Individual.
- The provider owns mailbox, DNS, deliverability, password, quota, and service
  incident support. Tecotype owns installation, local behavior, licensing, and
  client defects. Provider confirmation names the interoperability escalation
  path even when there is no distribution agreement.

Endpoint matching alone is not a durable license proof because the current
generic IMAP form is editable and some providers allow custom hostnames. The
eventual license design should use a signed provider definition or another
revocable provider assertion after successful local authentication. It must
not send the address, domain, credentials, server hostname, or mailbox content
to Tecotype.

Bundle confirmed provider definitions with the application or deliver them as
signed directory updates. A definition may include fixed endpoints,
provider-controlled endpoint patterns, autoconfiguration domains, and an
effective date. Do not try to enumerate customer email domains: providers with
custom-domain service can have an unlimited set. Tenant-specific, reseller,
or shared infrastructure needs an explicit provider assertion rather than a
loose hostname suffix.

The provider's promise to report changes is a useful early-warning path, not
the only control. Recheck definitions on release and during the annual
endorsement review.

For a distribution provider, measure only:

```text
permanent provider surface
→ dedicated provider review
→ signed install
→ first qualifying provider account
→ first useful action
→ second-account attempt
→ Individual purchase
```

The stable review URL itself supplies the provider source, for example
`tecotype.com/providers/nubo`. Preserve that source through the install and
purchase path with a provider code or short-lived first-party session; do not
add third-party pixels, cross-site tracking, or address-level reporting. Give
providers only aggregate cohort results.

The generic IMAP/SMTP client path is implemented. The provider entitlement and
second-account license gate, signed provider definitions, public reviews, and
attribution path are pre-release work. Public provider material must describe
the current release as Mac-first until Windows and Linux each pass their
release gate.

## Secondary model: workflow products

A workflow product qualifies only when it permanently introduces Tecotype to
its existing users before installation. Tecotype may provide a useful local
integration, but no free mailbox entitlement is included by default.

| Candidate | Possible discovery path | Required deal | Current assessment |
| --- | --- | --- | --- |
| [addy.io](https://addy.io/perks/) | Paid subscribers discover privacy products through public and in-account Perks | Perks placement, reciprocal offer, launch support, and useful alias actions in compose | Strong pre-install surface to validate |
| [Hookmark](https://hookproductivity.com/af/partner-of-the-month/) | Partner campaign with a listing, guide, newsletter, blog, and social posts | Complete campaign, permanent tagged guide, and first-link-to-paid attribution | Plausible co-marketing pilot; linkability alone will not cause switching |
| [Dropshare](https://kb.dropshare.app/how-to/how-can-i-enable-dropshare-integrations.html) | Featured private attachment-to-link workflow | Featured placement, dedicated guide, launch support, and tagged first-upload funnel | Conditional; a passive directory entry is insufficient |

**Receipts Space** qualifies only if it recommends Tecotype inside
receipt-email intake or onboarding and launches it to existing users.
Studiometry, GrandTotal, C-Command, Itinirare, Lunatask, and generic launcher,
directory, keyboard, or hardware listings are compatibility unless their
owners actively feature and launch Tecotype.

The command API, durable links, and mail-file export are not shipped. Their
requirements remain in [feature requests](../feature-requests.md).

## Pilot

Build the Nubo review and confirmation workflow first. Publishing that review
and enabling the provider entitlement are valid even without reciprocal
placement because they express Tecotype's editorial position. Keep the first
public set small enough that every review and integration can be maintained.

Before counting a provider as distribution, obtain a permanent placement and
attribution commitment. Validate paid users, desktop fit, multi-account
propensity, support ownership, and the first successful provider-sourced
action. Measure only aggregate licensing and activation events; never collect
addresses or mailbox content.

Continue a distribution placement only if it sends qualified activations and
paid conversion can plausibly exceed integration and support cost. Written
confirmation or a lightweight agreement should define endpoint updates,
placement, termination, support boundaries, and the free-entitlement
transition. It does not need to control the editorial endorsement.

See [pricing](../pricing.md) for the Individual price.
