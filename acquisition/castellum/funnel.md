# Castellum public funnel

Research date: **2026-07-17**

No client was downloaded or installed. No account was created, no mailbox was
connected, no Google authorization was attempted, no form was submitted, and
no purchase or trial was started. The reconstruction below uses only the
current public site, legal pages, release metadata, manifests, repository
history, and third-party documentation.

## Executive finding

Castellum has a short public path to a disk image and no observable path from
that request to a working, retained user.

```text
unknown awareness
→ manager/private-AI homepage
→ untagged GitHub disk-image request
→ launch
→ sample data, skip, Gmail, or IMAP setup
→ first useful mail workflow
→ voluntary return
```

Only the homepage, release asset, and aggregate asset-request counts are
publicly visible. Launch success, provider connection, first value, return,
and retained use are unknown.

The latest explicit Gmail note adds an important break:

```text
download
→ Sign in with Google
→ developer-approved test-user check
→ access or block
```

[v0.2.1](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.1)
says the OAuth token-exchange defect was fixed but Google’s consent screen was
still in testing mode. The July 17 legal-page commit says the pages were added
to support verification. No later public release note establishes that general
Google authorization became available.

## Homepage to disk image

The current path is:

```text
castellummail.com
→ “Download for Mac” page anchor
→ final direct GitHub asset URL
→ Castellum-arm64.dmg
```

Observed:

- no email capture, account, card, or checkout before download;
- no visible trial clock;
- no source or campaign parameter on the asset link;
- Apple Silicon only, macOS 12 or newer;
- “free in early access”;
- first-party signed-and-notarized claim;
- public release-page digest and release notes;
- direct `latest/download` URL rather than a version-pinned homepage link.

The current v0.2.2 asset metadata reports:

| Field | Public value |
| --- | --- |
| Release | `v0.2.2` |
| Published | 2026-06-30 10:31 UTC |
| Disk-image size | 120,094,490 bytes |
| Asset requests | 8 |
| SHA-256 digest | `3521532f93fc3743eba3b552e1f00302bac69a52956548683ff43ba9c5f8dacb` |

The digest is GitHub release metadata. Because the client was not downloaded,
the bytes, signature, notarization ticket, quarantine behavior, launch, and
updater were not independently validated.

## Release-request ledger

| Release | Published | Disk image | Requests | Update manifest | Requests | Material release note |
| --- | --- | ---: | ---: | --- | ---: | --- |
| v0.1.0 | 2026-06-29 21:06 | 119,506,996 bytes | 3 | None | — | First public build; claimed signed and notarized |
| v0.1.1 | 2026-06-29 21:54 | 119,610,653 bytes | 9 | None | — | Fixed v0.1.0 launch crash caused by packaged SQLite native-module ABI |
| v0.2.0 | 2026-06-30 08:31 | 120,099,775 bytes | 2 | Present | 1 | Added updater, sample/connect/skip onboarding choices, AI setup, and problem reporting |
| v0.2.1 | 2026-06-30 09:00 | 120,098,625 bytes | 2 | Present | 1 | Fixed Gmail token exchange; disclosed test-user restriction |
| v0.2.2 | 2026-06-30 10:31 | 120,094,490 bytes | 8 | Present | 2 | Added 31 provider guides and Thunderbird autoconfig fallback |
| **Total** |  |  | **24** |  | **4** |  |

GitHub calls these values download counts in API fields, but operationally
they are asset requests. They can include repeated requests, maker testing,
research, interrupted transfers, or automated activity. They are not unique
visitors, downloads completed, installs, launches, or users.

The four manifest requests similarly cannot establish four active clients.
They can include app checks, manual inspection, development, or research.

## First launch and onboarding

The public v0.2.0 release note says a first launch can:

- explore sample data;
- connect email;
- skip for now.

That is a useful no-mailbox comprehension path. Public material does not show:

- the exact current screen order;
- whether a fresh install reaches it reliably;
- how much of the product works with sample data;
- which event counts as onboarding completion;
- whether sample exploration predicts mailbox connection;
- whether the app stores or transmits onboarding telemetry.

The first-release history is a sharp reliability warning. v0.1.1 says v0.1.0
crashed on launch because a native SQLite module was compiled for the wrong
Electron ABI. Its nine disk-image requests exceeded the first build’s three,
but that cannot reveal whether affected people returned successfully.

## Provider branches

### Gmail

The homepage says “Gmail in one click” and “Sign in with Google instantly.”
The latest explicit release evidence says:

1. v0.2.0 had a Gmail token-exchange failure;
2. v0.2.1 fixed the missing client-secret exchange issue;
3. Google’s consent screen remained in testing mode;
4. non-approved addresses could still receive an access-blocked message.

The current privacy policy lists:

- `gmail.readonly`;
- `gmail.modify`;
- `gmail.send`.

Google classifies `gmail.readonly` and `gmail.modify` as
[restricted scopes](https://developers.google.com/workspace/gmail/api/auth/scopes).
Google’s
[verification guidance](https://developers.google.com/identity/protocols/oauth2/production-readiness/restricted-scope-verification)
requires public apps using restricted scopes to complete the applicable
verification process; an additional security assessment can apply when
restricted data is stored or transmitted through a server.

The Castellum policy says mailbox content remains local except for optional
user-selected cloud-AI processing. That describes the intended data boundary;
it does not establish the current verification state. No authorization was
attempted, so the public Gmail funnel remains unverified.

### Guided IMAP and SMTP

v0.2.2 says it added guided presets for 31 providers and a Thunderbird
autoconfig fallback. Public material supports that setup surface, not
successful end-to-end compatibility with every named provider.

The likely path is:

```text
select provider
→ enter address and provider-required credential or app password
→ resolve IMAP/SMTP settings
→ connect and sync
→ first useful action
```

Unknowns include credential guidance, TLS validation, sync completeness,
provider-specific failure recovery, sent-mail behavior, and return.

The homepage’s “Proton Mail” chip needs the release note’s “Proton (Bridge)”
qualification. Proton’s
[desktop IMAP/SMTP documentation](https://proton.me/support/imap-smtp-and-pop3-setup)
says normal third-party desktop clients require Proton Mail Bridge, which is
available on paid Proton plans. Provider naming is not proof of a direct
consumer-login flow.

Microsoft OAuth is described as future work in the provider copy. It should
not be counted as a current path.

## Local-AI branch

The landing page makes AI optional and describes a separate dependency:

```text
working Castellum install
→ install and open Ollama
→ Castellum detects it
→ install the recommended llama3.2 model
→ model download completes
→ summary, triage, or draft-reply value
```

This is more transparent than an unexplained “local AI” label. It also adds a
second application, model download, hardware expectations, and another
failure surface before AI value.

No Ollama component or model was downloaded. Detection, model installation,
latency, output quality, mail-data flow, and successful AI activation remain
first-party claims.

The privacy page says optional cloud AI is off by default and can send selected
content to the provider a user chooses. The homepage FAQ appears to contain a
copy error: it says nothing is sent to cloud AI “unless you explicitly turn
that off.” The surrounding policy implies “turn that on.” That sentence should
not be used as reliable consent guidance until corrected.

## Feedback and support

The site links to the public GitHub issues page. The v0.2.0 release note says
`Report a Problem` can open a prefilled issue with diagnostics.

The repository’s public workflow:

- labels new issues `needs-triage`;
- adds `from-app` when diagnostic markers are present.

There were zero open issues at capture. That does not establish zero problems,
successful reporting, or fast resolution. No issue was submitted and no
diagnostic payload was generated or inspected.

## Early access and future payment

The current path stops before commerce:

```text
free early-access build
→ installed version continues under current terms
→ future paid licensing may be introduced
→ price, date, entitlement, upgrade, and conversion unknown
```

Observed:

- no current price;
- no public checkout;
- no current license-key step;
- no visible account or billing portal;
- terms say future paid licensing may be introduced;
- terms say later changes do not retroactively invalidate the installed
  version’s existing license;
- privacy policy names Lemon Squeezy and self-hosted n8n/EspoCRM for future
  purchase and license handling.

Naming processors in a policy is preparation, not proof that checkout,
licensing, renewal, cancellation, refund, or upgrade behavior has shipped.

## Observable conversion evidence

| Stage | Public evidence | What is not known |
| --- | --- | --- |
| Awareness | Homepage exists; founder profiles exist | Source, reach, qualified visits |
| Landing | Current public page and message | Unique visitors, comprehension, CTA rate |
| Asset request | 24 disk-image requests | Unique people, completion, source |
| Launch | Release notes, including a launch-crash fix | Clean launches by release |
| Onboarding | Public description of sample/connect/skip | Completion and abandonment |
| Provider connection | Gmail and IMAP setup claims | Successful authorized accounts |
| First value | Feature claims and screenshot | Which action occurs and for whom |
| AI activation | Ollama setup instructions | Completed models and useful outputs |
| Return | Four update-manifest requests | Voluntary second use or retention |
| Payment | Future terms/processors | Offer, checkout, conversion, revenue |

## Tecotype implications

Castellum’s short no-form download is a useful surface pattern, but its history
shows that download availability cannot substitute for a release gate.

For Tecotype:

- keep implemented distribution plumbing distinct from a validated public
  release;
- test a clean install, signed/notarized acceptance, first run, no-account
  state, update, rollback, and recovery on release-candidate bytes;
- finish the intended Gmail restricted-API review before promising public
  Gmail access;
- treat generic IMAP setup as provider-specific until representative
  connections succeed;
- measure source, install intent, first launch, provider connection,
  message-matched first value, and voluntary return as separate events;
- do not call an asset request an install or user;
- do not lead people into a free preview before future price, entitlement,
  notice, and installed-version behavior are explicit;
- do not expose broad acquisition until sending, failure, and recovery
  behavior is safe.

Tecotype’s distribution worker, update path, core Gmail/IMAP client, and
sending foundation are implemented to meaningful degrees. The public website,
first-run/no-account experience, licensing/payment, Gmail release review,
source attribution, and remaining send UI/recovery work are still release
conditions. They must not be described as shipped merely because the
underlying path exists.
