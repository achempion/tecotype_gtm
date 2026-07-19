# Sealed pain discovery, round 1: accounts, access, identity, trust, and local desktop use

Access date for every source: **2026-07-19**.

## Scope and method

This was an independent public-source pass. No workspace file, product document, feature request, experiment, provider/partnership document, or other agent work was read. The product boundary used for this pass was only: a future calm, keyboard-first desktop mail client for macOS, Windows, and Linux; no mobile; mailbox credentials and mailbox contents remain local; browser-local OAuth and local files are acceptable. It is not assumed to be a hosted provider, ticketing/sales suite, chat assistant, or unattended automation system.

Claims below concern public pain and incumbent behavior, not Tecotype's shipped state. Provider documentation and vendor copy are used only for current compatibility, incumbent, or discovery-surface checks. They are not counted as direct pain observations.

### Coverage audit

- **Pages opened and inspected:** 24 plausible pages; 14 retained as direct observations. Successful opens included 5 vendor-hosted support-community threads, 5 independent community threads, 1 Q&A page, 2 public issue reports, 2 review pages, 6 provider help/discovery pages, and 3 operating-system/app-directory pages. Some pages served multiple purposes, so these counts overlap.
- **Source types represented in retained evidence:** official support community, independent forum/community, Q&A, public issue tracker, and app/review site.
- **Underlying pain families investigated:** secure account setup and reauthentication; provider-specific authentication/client gaps; multi-account identity and sender selection; local/offline/sync reliability; privacy/security trust; provider switching and household/account continuity; desktop default-handler integration.
- **Materially distinct queries tested:** more than four. Representative exact queries:
  1. `site:discussions.apple.com Mail multiple accounts wrong from address sent from wrong account`
  2. `site:support.mozilla.org/questions Thunderbird OAuth login account setup first person Gmail Microsoft`
  3. `site:reddit.com email client multiple accounts identity wrong sender desktop`
  4. `site:github.com email client issue offline IMAP authentication multiple accounts first person`
  5. `site:apple.stackexchange.com Apple Mail wrong account sender multiple accounts alias`
  6. `site:reddit.com/r/ProtonMail desktop email client bridge multiple accounts offline first person`
  7. `site:bugzilla.mozilla.org/show_bug.cgi Thunderbird OAuth Microsoft login account setup user report`
  8. `Thunderbird user review OAuth setup multiple accounts offline review 2025`
  9. `site:reddit.com/r/privacy desktop email client requires account cloud credentials privacy concern first person`
  10. `site:fastmail.help third party email client setup Thunderbird Outlook Apple Mail desktop`

Search results were treated as discovery only. A result was not retained unless the underlying page was opened and the actor, trigger, job, failure, consequence, and behavior/workaround could be recovered.

## Executive synthesis

The densest current evidence is not “people want another unified inbox.” It is that provider authentication and account state can fail after users appear to do everything correctly: completing OAuth and 2FA, running current releases, enabling cookies, selecting the documented server, or using a previously working paid client. The consequence is binary—an account cannot be added, stops syncing, or cannot send/receive—and the workaround often becomes destructive or technical: remove/re-add the account, roll back the client, edit an internal configuration, switch forks, or abandon the client.

The second job is keeping the human identity behind each account unambiguous. Direct reports across Apple Mail, eM Client, and Proton contexts show replies or new messages selecting the wrong sender, hiding the intended account, or forcing separate clients/profiles. The consequence ranges from lost business adoption to sending as the wrong person. A unified view creates an ambiguity that incumbents often resolve by folder context or a default account rather than by explicit human intent.

The third job is dependable local use. Users explicitly test offline behavior, travel with it, or rely on multiple inboxes for appointments and work. Blank offline windows, disappearing drafts, stalled outboxes, and silently stale inboxes destroy trust because the client can look operational while being wrong. This pain is real, but free incumbents already claim or deliver local caching/offline use, so a generic “works offline” claim is not differentiated without evidence of completeness, visibility of sync state, and recovery.

Privacy is a purchase filter, not merely an abstract value. Users ask whether a client proxies mail or credentials through another server, and one current switcher wants more privacy without sacrificing practicality. However, a local client cannot remove provider-side access or make ordinary email end-to-end private. The defensible boundary is narrower: direct provider connections, locally stored credentials/content, explicit disclosure of what ever leaves the device, and no cloud proxy for mailbox access.

The strongest provider-controlled discovery surface found is Proton Mail Bridge: its installed setup flow asks the user to choose a desktop client, while its support site publishes a short officially supported list. Fastmail, Microsoft, Google, and Yahoo also name third-party desktop clients in provider help. These are real pre-install discovery or recommendation surfaces for people with zero Tecotype users, but no source evidences partner willingness. Only a permanent provider placement with an attributable first-action-to-paid path would count as distribution; directories and organic search alone do not.

## Retained direct observations

### Family A — securely connect or regain access to an existing provider

#### O1. Gmail account setup reaches provider login but fails until the OAuth conversion path is used

- **Source:** [Setting up gmail in Thunderbird](https://support.mozilla.org/en-US/questions/1445370)
- **Publication date:** 2024-04-20; resolution confirmed 2024-04-21.
- **Domain/type:** support.mozilla.org; official support community.
- **Author independence:** independent end user posting on a vendor-hosted forum; no affiliation stated.
- **Observation:** The user tried to add multiple Gmail addresses. Provider login returned an error even after trying no password, disabling 2FA, and manual setup. A link to Thunderbird's Google OAuth conversion guidance solved it.
- **Actor/context:** desktop Thunderbird user adding Gmail addresses.
- **Trigger:** reaches the final Google sign-in step during setup.
- **Desired job:** connect existing Gmail accounts without weakening account security.
- **Failure:** provider login errors after the client reports configuration found.
- **Consequence:** account setup cannot complete.
- **Behavior/workaround:** tried several security/configuration changes, then followed the OAuth conversion instructions and confirmed success.
- **Recency/current relevance:** medium. The 2024 flow predates Thunderbird's 2026 Account Hub, but Gmail still requires modern authentication and current provider guidance still emphasizes “Sign in with Google.”
- **Duplication check:** overlaps the same authentication family as O2–O6, but differs by provider (Google), client stage (initial setup), and successful recovery path.
- **Supported/contradicted claim:** supports “automatic discovery plus a provider login is not always sufficient”; contradicts “Gmail setup failure necessarily requires an app password or reduced security.”

#### O2. Adding a Microsoft passkey made the embedded OAuth window unusable

- **Source:** [OAuth2 pop-up says unable to connect](https://support.mozilla.org/en-US/questions/1585704)
- **Publication date:** 2026-06-05.
- **Domain/type:** support.mozilla.org; official support community.
- **Author independence:** independent end user; no affiliation stated.
- **Short quote (8 words):** “Thunderbird does not (yet) support passkeys.”
- **Actor/context:** Hotmail user who had previously connected the account and later added a passkey.
- **Trigger:** re-adds the Microsoft account and receives the OAuth popup.
- **Desired job:** authenticate with the account's current strong sign-in method.
- **Failure:** the in-client popup shows “Unable to connect”; copying the URL into normal browsers loads the passkey flow, but the result cannot return to Thunderbird.
- **Consequence:** the account cannot be set up in the client.
- **Behavior/workaround:** cleared cache, removed account traces, stopped a home-server Nginx instance, removed the passkey, signed in with a password, then re-added the passkey after setup.
- **Recency/current relevance:** high; one month before access.
- **Duplication check:** distinct from O4/O5 because the failure is passkey/browser handoff rather than provider redirect mismatch or Exchange protocol handling.
- **Supported/contradicted claim:** supports “supporting OAuth is not equivalent to supporting the provider's current authentication choices”; contradicts “an external browser alone automatically makes every passkey flow work.”

#### O3. A paid desktop client stopped syncing a locked-down university Exchange account

- **Source:** [Exchange Issues](https://forum.emclient.com/t/exchange-issues/115849)
- **Publication date:** 2026-04-07; successful workaround reported 2026-04-14.
- **Domain/type:** forum.emclient.com; official support community.
- **Author independence:** independent user with an eM Client Personal license; no affiliation stated.
- **Observation:** A previously working university account stopped syncing and repeatedly requested credentials. Automatic addition failed with an OAuth credential error; manual Exchange setup dismissed itself without completing.
- **Actor/context:** Windows 11 user with a paid personal client license and a university mailbox that offers Exchange/OWA but no POP, IMAP, or SMTP.
- **Trigger:** an existing account stops syncing.
- **Desired job:** keep using the university account in the chosen desktop client.
- **Failure:** correct credentials do not restore sync; auto and manual setup both fail.
- **Consequence:** the desktop account is unusable even though it still works on the user's phone.
- **Behavior/workaround:** applied the latest hotfix and Windows updates, checked with university IT, uninstalled the client, installed an older known-working version, added the account, then upgraded again.
- **Recency/current relevance:** high; current 2026 Windows/client versions and a provider-restricted environment.
- **Duplication check:** distinct from O4/O5 because the institution exposes only Exchange/OWA and may restrict approved clients; it also proves paid-client adjacency.
- **Supported/contradicted claim:** supports “provider policy and proprietary account types can be a hard client boundary”; contradicts “IMAP/OAuth coverage alone is enough for broad desktop account compatibility.”

#### O4. A current Outlook account repeatedly failed in Thunderbird despite all documented settings

- **Source:** [Thunderbird has authentication failure when connecting an outlook account](https://www.reddit.com/r/Thunderbird/comments/1u7lnvx/thunderbird_has_authentication_failure_when/)
- **Publication date:** 2026-06-16.
- **Domain/type:** reddit.com/r/Thunderbird; independent community.
- **Author independence:** independent end user; no affiliation stated.
- **Observation:** One Outlook account oscillated between working, showing errors while still working, and failing entirely. After deletion, it could not be re-added despite enabled cookies, firewall permission, disabled experimental Account Hub, OAuth2 for both directions, and current software.
- **Actor/context:** desktop Thunderbird user with Outlook and Hotmail accounts.
- **Trigger:** a problematic Outlook account is deleted and re-added.
- **Desired job:** restore a provider account without changing client.
- **Failure:** authentication remains stuck against outlook.office365.com; Hotmail accounts still work.
- **Consequence:** the account is unavailable and the user considers leaving Thunderbird.
- **Behavior/workaround:** checked all common settings, updated, tried Betterbird, and searched fragmented help; another user used an Owl add-on, while the reporter eventually found an unrecorded multi-step fix.
- **Recency/current relevance:** high; one month before access.
- **Duplication check:** corroborates O5 from an independent community but is not the same report or precise redirect regression.
- **Supported/contradicted claim:** supports “provider/account-specific failures survive generic troubleshooting”; contradicts “updating to the newest release or switching to a close fork reliably resolves Outlook setup.”

#### O5. A confirmed Thunderbird/Microsoft redirect mismatch blocked add-account and daily reauthentication

- **Source:** [Bug 2036505 — OAuth2 for Microsoft fails: redirectionEndpoint not defined causes http/https mismatch](https://bugzilla.mozilla.org/show_bug.cgi?id=2036505)
- **Publication date:** opened 2026-05 (Bugzilla displayed “2 months ago” at access); a second reporter states the failure began 2026-04-23.
- **Domain/type:** bugzilla.mozilla.org; public issue tracker.
- **Author independence:** independent reporters; maintainers later confirmed and patched the regression.
- **Short quote (9 words):** “Authentication fails and the account cannot be added.”
- **Actor/context:** Windows 11 users on Thunderbird 150 with personal Microsoft or Office 365 IMAP accounts; one account required daily reauthentication.
- **Trigger:** add a Microsoft account or reauthenticate after upgrading from Thunderbird 149 to 150.
- **Desired job:** complete OAuth and continue sending/receiving.
- **Failure:** Microsoft upgrades the redirect to HTTPS while the client waits for HTTP localhost, producing Connection Refused.
- **Consequence:** one user cannot add the account; another can neither send nor receive.
- **Behavior/workaround:** manually edited the client's provider configuration; another machine stayed on ESR 140. A fix was approved for the 152 beta/release line.
- **Recency/current relevance:** high but version-sensitive. The issue was actively patched in June 2026, so the exact regression may now be fixed; the underlying cross-provider redirect compatibility job remains current.
- **Duplication check:** technical corroboration of O4, not a duplicate: it identifies a specific root cause and confirmed release regression.
- **Supported/contradicted claim:** supports “provider authentication compatibility can regress independently of correct user settings”; contradicts “a generic OAuth implementation is stable across provider redirect changes.”

#### O6. Half of a switcher's accounts failed authentication in one client while working in others

- **Source:** [Multiple accounts “Authentication failed” problem](https://forum.emclient.com/t/multiple-accounts-authentication-failed-problem/85647)
- **Publication date:** 2022-10-27.
- **Domain/type:** forum.emclient.com; official support community.
- **Author independence:** independent prospective switcher; no affiliation stated.
- **Observation:** An employer Exchange account and an office mailbox on a small independent host failed during a trial of eM Client. The user tested protocol/port combinations; both worked in other clients, and the small host was not Exchange.
- **Actor/context:** person evaluating a switch to eM Client with a mixed-provider account set.
- **Trigger:** tries to add all existing accounts to the new client.
- **Desired job:** switch clients without losing any provider/account.
- **Failure:** about half of the accounts return authentication errors and the expected OAuth path is not offered.
- **Consequence:** the switch cannot be completed as a single-client move.
- **Behavior/workaround:** tried all visible security/protocol/port combinations and compared other clients; no resolution was recorded.
- **Recency/current relevance:** medium-low for implementation specifics; high for the persistent mixed-provider switching job.
- **Duplication check:** distinct from institutional Exchange-only O3 because it crosses employer Exchange and a small-host custom domain.
- **Supported/contradicted claim:** supports “supporting mainstream providers does not cover a heterogeneous account portfolio”; contradicts “one provider explanation accounts for every authentication failure.”

### Family B — preserve the intended human identity across accounts and aliases

#### O7. A previously correct eM Client setup exposed only the wrong sender account

- **Source:** [Reply is using wrong email account](https://forum.emclient.com/t/reply-is-using-wrong-email-account/97399)
- **Publication date:** 2024-05-20; resolved 2024-05-21.
- **Domain/type:** forum.emclient.com; official support community.
- **Author independence:** independent end user; no affiliation stated.
- **Observation:** With two accounts and Hotmail as primary, Reply and New suddenly selected the other account, and the From menu no longer offered Hotmail.
- **Actor/context:** eM Client 9.2 user with two accounts.
- **Trigger:** composes or replies after a service setting silently changed.
- **Desired job:** send from the intended account and retain an explicit choice.
- **Failure:** only the other account is selectable.
- **Consequence:** the user risks sending under the wrong identity or cannot use the intended identity.
- **Behavior/workaround:** checked account defaults and re-enabled AirSync; this restored the account.
- **Recency/current relevance:** medium-high. The exact AirSync state may be version-specific, but the identity-loss consequence is current.
- **Duplication check:** distinct from O8 because the intended identity disappears entirely rather than being ambiguously auto-selected for a message addressed to two accounts.
- **Supported/contradicted claim:** supports “sender selection can be a hidden account-health signal”; contradicts “showing a From dropdown guarantees the intended identity is available.”

#### O8. Apple Mail chose the other Exchange identity when replying to a message sent to both

- **Source:** [Default sender in Apple Mail when replying and more than one account](https://apple.stackexchange.com/questions/132241/default-sender-in-apple-mail-when-replying-and-more-than-one-account)
- **Publication date:** 2014-05-29.
- **Domain/type:** apple.stackexchange.com; independent Q&A.
- **Author independence:** independent end user; no affiliation stated.
- **Observation:** A user managing their own and another person's Exchange account replied to a message addressed to both. Apple Mail defaulted to the other person's identity even though the user's account was ordered first and set as the new-message default.
- **Actor/context:** delegate-like two-account use in Apple Mail.
- **Trigger:** reply to a message delivered to both managed identities from the unified context.
- **Desired job:** answer as oneself.
- **Failure:** the client selects the other managed person.
- **Consequence:** accidental impersonation/misdirected identity unless manually corrected.
- **Behavior/workaround:** manually changes From or first highlights a specific account inbox; SMTP/default settings did not solve the ambiguity.
- **Recency/current relevance:** low for Apple Mail version, high for the underlying multi-recipient/multi-identity ambiguity. A 2024 eM Client report (O7) independently confirms the broader job persists.
- **Duplication check:** not counted as current incumbent defect; retained as a clear first-person articulation of the underlying ambiguous-intent job.
- **Supported/contradicted claim:** supports “folder context and static defaults are insufficient when one person manages multiple identities”; contradicts “the account that received a message is always uniquely inferable.”

#### O9. Lack of multi-account visibility blocked a current Proton business move and complicated family care

- **Source:** [Adding second email address to Protonmail app](https://www.reddit.com/r/ProtonMail/comments/1u0sf6t/adding_second_email_address_to_protonmail_app/)
- **Publication date:** 2026-06-09.
- **Domain/type:** reddit.com/r/ProtonMail; independent provider community.
- **Author independence:** independent new Proton user; another independent commenter reports the business consequence.
- **Observation:** A person five days into moving from Gmail needed to see both their own Gmail and a parent's account used for bills. They could do this in Spark but could not determine whether Proton desktop supported it. A separate user said the missing capability kept their business mail on Exchange.
- **Actor/context:** new privacy-provider switcher who also helps a parent; corroborating business user with multiple accounts.
- **Trigger:** gradual Gmail-to-Proton migration and need to retain access to another person's mailbox.
- **Desired job:** see separate accounts in one desktop tree and reply from the correct account.
- **Failure:** the native app did not present the expected account model; advice pointed to Bridge plus Outlook, Thunderbird, or Evolution.
- **Consequence:** uncertainty during migration; for the corroborating user, no business-mail move to Proton.
- **Behavior/workaround:** considers Proton Bridge plus Apple Mail/another desktop client; commenters distinguish connected Gmail import from true multi-account use.
- **Recency/current relevance:** high; six weeks before access.
- **Duplication check:** distinct from O7/O8 because it is provider switching and cross-person account visibility, not a wrong-From defect.
- **Supported/contradicted claim:** supports “multi-account access is sometimes a prerequisite to provider adoption”; contradicts “import/forwarding is equivalent to managing separate live identities.”

### Family C — remain locally dependable when connectivity or sync is imperfect

#### O10. Proton's desktop app opened blank offline and required a restart after reconnecting

- **Source:** [Why desktop clients?](https://www.reddit.com/r/ProtonMail/comments/1bo42mc/why_desktop_clients/)
- **Publication date:** 2024-03-26.
- **Domain/type:** reddit.com/r/ProtonMail; independent provider community.
- **Author independence:** independent users; no affiliation stated.
- **Short quote (12 words):** “I also cannot access anything while being offline.”
- **Actor/context:** desktop user explicitly testing Proton Mail/Calendar offline; another user cites professional use.
- **Trigger:** disconnect Wi-Fi, close the desktop app, and relaunch it.
- **Desired job:** read previously available mail and preserve work without a network.
- **Failure:** the app shows a blank white screen; reconnecting alone does not recover it.
- **Consequence:** no mail access offline and a forced client restart; commenters reject it for professional use.
- **Behavior/workaround:** use Proton Bridge with a native mail client and shared calendar files so data remains locally available.
- **Recency/current relevance:** medium-high. The specific 2024 native app may have changed, but a 2026 thread still complained about incomplete offline behavior; vendor documentation also confirms Bridge/local-client caching as the incumbent workaround.
- **Duplication check:** distinct from O11/O12: provider-native offline launch failure rather than IMAP sync/outbox delay or draft loss.
- **Supported/contradicted claim:** supports “desktop packaging is not the same as local/offline capability”; contradicts “a desktop app inherently remains usable without connectivity.”

#### O11. A three-inbox desktop client silently delayed a time-sensitive message for ten days

- **Source:** [Mailspring Reviews](https://www.g2.com/products/mailspring/reviews) — review titled “Really Not Good — so many problems.”
- **Publication date:** 2022-12-16.
- **Domain/type:** g2.com; validated app review.
- **Author independence:** validated independent reviewer; review hosted by G2, not vendor copy.
- **Observation:** The reviewer reports one or more of three inboxes failing to sync roughly 70% of the time and outbox delays lasting days. One cancellation stayed queued for ten days and was later sent against the wrong appointment.
- **Actor/context:** small-business user operating three inboxes.
- **Trigger:** routine send and sync in a unified desktop client.
- **Desired job:** trust that all inboxes are current and time-sensitive outbound mail is delivered.
- **Failure:** sync and send state silently diverge from user intent.
- **Consequence:** a delayed cancellation affects the next appointment instead of the intended one; the reviewer abandons the client.
- **Behavior/workaround:** gives up on Mailspring; no successful recovery was reported.
- **Recency/current relevance:** medium-low for version, high for the trust job. Current provider/client issue reports show sync/auth regressions remain possible, but this frequency must not be generalized.
- **Duplication check:** distinct from O12 because delivery/sync invisibility causes an external scheduling error; O12 concerns local draft loss and crashes.
- **Supported/contradicted claim:** supports “silent stale state is more damaging than visible failure”; contradicts “easy setup and a unified inbox imply dependable ongoing operation.”

#### O12. Client freezes caused a Windows/Linux evaluator to lose five composed messages

- **Source:** [Anyone using MailSpring for their email client?](https://www.reddit.com/r/privacy/comments/vdmqqo/anyone_using_mailspring_for_their_email_client/)
- **Publication date:** 2022-06-16.
- **Domain/type:** reddit.com/r/privacy; independent community/recommendation thread.
- **Author independence:** independent evaluator; no affiliation stated.
- **Short quote (12 words):** “I just lost text of 5 messages I tried to compose.”
- **Actor/context:** privacy-conscious person who examined 25+ email clients and tested Mailspring on desktop.
- **Trigger:** composing several messages during a client trial.
- **Desired job:** write safely in a private/open desktop client.
- **Failure:** random freezes/crashes lose local draft text.
- **Consequence:** immediate work loss and abandonment after only hours; the original poster says they will skip the client.
- **Behavior/workaround:** switches back to evaluation/other clients; another commenter uses a paid eM Client subscription despite dissatisfaction.
- **Recency/current relevance:** medium-low for Mailspring version; high as evidence that draft durability and recovery are table stakes in client switching.
- **Duplication check:** same incumbent as O11, different source type, failure mode, actor, and consequence. A positive user in the same thread reported a year with zero issues, recorded below as counterevidence.
- **Supported/contradicted claim:** supports “local draft durability drives trust and word-of-mouth rejection”; contradicts any general claim that Mailspring fails for everyone.

### Family D — switch providers or clients without widening trust or breaking household continuity

#### O13. A privacy-motivated switcher had money to pay but conflicting client/privacy guidance

- **Source:** [Is the email client important in terms of privacy?](https://www.reddit.com/r/emailprivacy/comments/1r9us37/is_the_email_client_important_in_terms_of_privacy/)
- **Publication date:** 2026-02-20.
- **Domain/type:** reddit.com/r/emailprivacy; independent community.
- **Author independence:** independent user; one responding client developer disclosed their affiliation and is not used as direct independent evidence.
- **Observation:** A new wage earner planned to move from Gmail to Posteo, wanted more privacy without losing practicality, and found prior research conflicting. They specifically asked whether retaining Apple Mail would undermine the provider switch.
- **Actor/context:** first-time paid-service/privacy switcher.
- **Trigger:** has income to fund services and wants EU/privacy-respecting infrastructure.
- **Desired job:** change provider while keeping a convenient trusted desktop client.
- **Failure:** cannot determine the client's effect on privacy from available guidance.
- **Consequence:** confusion at a purchase/switching decision and risk of either abandoning practicality or making an uninformed trust choice.
- **Behavior/workaround:** asks a specialist community, later switches to Posteo, and continues evaluating Apple Mail; another Posteo user reports the ordinary IMAP setup works.
- **Recency/current relevance:** high.
- **Duplication check:** distinct from O14: individual trust-model uncertainty rather than household/ISP portability.
- **Supported/contradicted claim:** supports “clear data-path disclosure can influence provider/client choice”; contradicts “privacy-provider selection alone answers the client's trust model.”

#### O14. An ISP-tied household wanted provider portability without losing separate identities or ease of use

- **Source:** [want new email provider](https://www.reddit.com/r/emailprivacy/comments/1sz4jsu/want_new_email_provider/)
- **Publication date:** 2026-04-29.
- **Domain/type:** reddit.com/r/emailprivacy; independent firsthand account.
- **Author independence:** independent user; no affiliation stated.
- **Observation:** A household used ISP email with separate passwords and private addresses; one spouse downloaded mail locally with eM Client and found it easy. The user wanted to change ISPs, gain more privacy, preserve convenience, and explicitly had no problem paying.
- **Actor/context:** two-person household with multiple addresses, separate credentials, webmail plus a local desktop client.
- **Trigger:** desire for freedom to change internet provider.
- **Desired job:** move mail providers while keeping account separation, local desktop access, privacy, and ease for both people.
- **Failure:** the current address/provider is coupled to the ISP; Proton appeared suitable for one person but probably not the other.
- **Consequence:** provider lock-in and a household adoption mismatch.
- **Behavior/workaround:** seeks recommendations and considers paid providers; no final migration outcome recorded.
- **Recency/current relevance:** high.
- **Duplication check:** related to O9's family/care context but distinct: provider portability and separate credentials rather than one person managing another person's bills.
- **Supported/contradicted claim:** supports “provider switching is a household continuity job, not only data import”; contradicts “one privacy-focused provider/client choice necessarily fits every household member.”

## Near-misses and counterevidence

These were inspected but not counted as direct pain observations where they were vendor copy, generic requests, old implementation details without consequence, or second-hand claims.

1. **Current Thunderbird onboarding is materially newer than several retained reports.** [Account Hub for Thunderbird Desktop](https://support.mozilla.org/en-US/kb/account-hub-thunderbird-desktop), created 2026-06-18, documents automatic provider lookup, external-browser OAuth in versions 153+, MFA, and adding another email. This is strong counterevidence against treating older Gmail onboarding friction as current by default. It is vendor documentation, not firsthand outcome evidence.
2. **Microsoft publishes a complete modern-auth recovery path.** [Modern Authentication Methods now needed](https://support.microsoft.com/en-us/support/known-issues/modern-authentication-methods-now-needed-to-continue-syncing-outlook-email-in-non-microsoft-email-ap), last updated 2024-06-10, recommends current Outlook, Thunderbird OAuth2, or re-adding Apple Mail as Outlook.com. This shows a complete free outcome often exists. O3–O5 show it is not universal across institution policy, proprietary account types, and regressions.
3. **Google explicitly supports third-party clients with modern auth.** [Add Gmail to another email client](https://support.google.com/mail/answer/7126229?hl=en) names Outlook, Apple Mail, and Thunderbird and recommends “Sign in with Google.” This is a compatibility/discovery surface, not proof every client setup succeeds.
4. **The eM Client wrong-sender report was fixed by re-enabling AirSync.** O7 therefore supports a visible account-health/identity problem, not a conclusion that the client always chooses the wrong identity.
5. **A positive user in the same Mailspring thread reported more than a year without issues across Linux and Windows.** This directly counters generalizing O12's crashes. The unit of evidence is “some evaluated environments fail catastrophically,” not “Mailspring is universally unstable.”
6. **G2 includes positive multi-account and payment evidence.** A validated 2021 reviewer said they paid for Mailspring to manage all mail, used unified inbox and per-account aliases, and considered the cost worth the productivity gain. Another 2023 reviewer managed two personal and one work account across Linux, Mac, and Windows. This counters “free incumbents cannot handle multi-account identity” and supplies paid adjacency.
7. **Proton Bridge already offers combined and split-address modes and leaves existing mail in the client when signed out.** [How to install Proton Mail Bridge](https://proton.me/support/protonmail-bridge-install) documents both. O9's problem is separate live accounts/cross-provider access, which is not identical to addresses within one Proton account.
8. **Tuta claims free desktop clients on all three target operating systems with offline cache and OS integration.** [Free secure desktop email client](https://tuta.com/blog/desktop-clients-tutanota), published 2025-02-03, is vendor copy and provider-specific, so it is not direct evidence. It does show “free, private, offline desktop app” is already an incumbent claim, and its offline cache has limits (mail must be viewed or indexed; offline login is paid; write access was still planned).
9. **Generic “best email client” pages and recommendation snippets were excluded.** They usually lacked a trigger, failure, consequence, and workaround, and often repeated vendor feature lists.
10. **Feature requests and votes were excluded.** Requests for aliases, unified inboxes, passkeys, or offline mode did not count unless the author described a real job and consequence.
11. **Second-hand security claims were excluded.** Community assertions about clients uploading credentials or providers scanning mail were not treated as direct observations without the actor's own experience or primary documentation.
12. **Search volume was not inferred from result density.** Repeated search hits establish discoverability and duplication, not market size or recommendation.

## Current discoverability, recommendation, sharing, and incumbent surfaces

| Surface | Current evidence | Zero-user source? | Recommendation vs. mere discovery | Distribution status under the strict rule | Exact blockers |
|---|---|---:|---|---|---|
| **Proton Mail Bridge installed setup flow and support list** | [Install guide](https://proton.me/support/protonmail-bridge-install) says the installed Bridge presents buttons to choose an email client; [supported clients](https://proton.me/support/clients-supported-bridge) lists Thunderbird, Outlook, and Apple Mail by OS. Bridge is [paid-plan only](https://proton.me/support/imap-smtp-and-pop3-setup). | Yes: a paid Proton user can have zero Tecotype usage before choosing a client. | Strong provider-controlled recommendation/certification surface, not merely search. | **Candidate only, not counted.** It could meet permanent pre-install discovery and an attributable client-install/paid funnel if Tecotype became a tested option with a trackable first action. | No evidence of Proton willingness; official testing/support burden; Bridge compatibility; local loopback/TLS behavior; Linux packaging/keyring support; paid Proton prerequisite; must prove no mailbox/cloud proxy; provider-specific features may be lost. |
| **Fastmail device setup directory** | [Set up Fastmail on your device](https://www.fastmail.help/hc/en-us/articles/360058752834-Set-up-Fastmail-on-your-device) lists Apple Mail, Thunderbird, Outlook, eM Client, MailMate, Vivaldi Mail, and others. Third-party clients are unavailable on Basic plans. | Yes: provider customers choose a desktop client before installing it. | Provider-controlled guide/list; a real recommendation surface, although not an exclusive endorsement. | **Candidate only, not counted.** A permanent listed setup guide plus an attributable first-action-to-paid client path could qualify. | No partner willingness; app-password flow; non-Basic-plan requirement; no current Tecotype guide; support handoff to client vendor; must show multi-account value beyond Fastmail web/app. |
| **Microsoft modern-auth support page** | [Microsoft Support](https://support.microsoft.com/en-us/support/known-issues/modern-authentication-methods-now-needed-to-continue-syncing-outlook-email-in-non-microsoft-email-ap) recommends current Outlook and gives explicit Thunderbird and Apple Mail setup paths. | Yes. | Provider-controlled recommendation/recovery surface. | **Candidate surface, not counted.** It is durable and pre-install, but currently advantages Microsoft's free incumbent and named clients. | Strong incumbent conflict; no willingness; modern-auth certification; Exchange/OWA/EWS/Graph/IMAP coverage; tenant admin consent and Conditional Access; trackable client-paid handoff absent. |
| **Google Gmail third-party-client help** | [Gmail Help](https://support.google.com/mail/answer/7126229?hl=en) names Outlook, Apple Mail, and Thunderbird and requires modern Google sign-in. | Yes. | Weak recommendation/compatibility surface; primarily setup guidance. | **Not counted.** No permanent Tecotype placement or attributable funnel. | OAuth verification/brand review; Google sign-in policy; no partner willingness; support burden; page does not operate as a broad client marketplace. |
| **Yahoo IMAP help** | [Yahoo Help](https://my.help.yahoo.com/kb/new-mail-for-desktop/manually-download-yahoo-emails-sln28681.html) names Thunderbird, Outlook, and Mac Mail and warns that large mailboxes can take days and clients may cache only previews. | Yes. | Provider-controlled compatibility guidance. | **Not counted.** Potential listing surface only. | App-password/OAuth behavior; large-mailbox/offline completeness; no willingness; no attributable client-paid path. |
| **Flathub email category and verified listing** | [Email category](https://flathub.org/en/apps/collection/tag/email/1) currently shows 8 apps; [Thunderbird](https://flathub.org/apps/org.mozilla.Thunderbird) is verified with about 1.5 million installs at crawl. | Yes. | App-directory discovery, not an evidenced partner recommendation. | **Does not count as distribution** under the stated rule. | Crowded category; ranking unknown; no recommender introduction; installs are not attributable paid conversion; packaging/security review required. |
| **G2 and Trustpilot reviews** | [G2](https://www.g2.com/products/mailspring/reviews) includes validated positive/negative recommendations and explicit paid-client adjacency. [Trustpilot](https://www.trustpilot.com/review/getmailspring.com) includes an unprompted 2025 power-user recommendation after trying about 15 clients. | Yes. | Independent person-to-person recommendation/sharing surface. | **Organic acquisition evidence, not distribution.** | Review recency/representativeness; no permanent partner placement; attribution to paid may be weak; cannot control ranking or claims. |
| **OS default-email settings** | [Apple Support](https://support.apple.com/en-mide/102362) says Mail is the default and another client can be selected; [Microsoft Support](https://support.microsoft.com/en-us/outlook/make-outlook-the-default-program-for-email-contacts-and-calendar) documents file/protocol defaults. | No for acquisition: the alternative client must generally already be installed. | Retention/desktop-integration surface, not recommendation. | **Does not count as distribution.** | On macOS, users may need to open/configure Apple Mail before changing the default unless the alternative can self-register; Windows has per-file/protocol choices; no zero-user intro. |

### Incumbent solution map

- **Thunderbird:** free, cross-platform, multiple accounts, offline mode, current Account Hub, broad provider documentation, and the dominant named Linux option in provider guides. Current issue evidence shows provider auth can still regress or fragment into advanced settings.
- **Apple Mail:** preinstalled/default on macOS and frequently named by providers. Its advantage is zero install and OS integration; its limitations in this pass are identity ambiguity in a unified context and the awkward OS path for choosing a different default.
- **Microsoft Outlook:** free current app plus paid/subscription variants, privileged recommendation from Microsoft, and broad account support. New Outlook's cloud-mediated architecture is [incompatible with Proton Bridge's localhost model](https://proton.me/support/proton-mail-bridge-new-outlook-for-windows-set-up-guide), creating a meaningful local-client boundary.
- **eM Client:** commercial/free tiers, cross-provider account support, and paid support. Direct reports show Exchange/provider setup and account-service state can break; direct paid adjacency is strong.
- **Mailspring:** cross-platform, unified inbox, aliases, and paid productivity features. Review evidence is sharply mixed: some users pay and recommend it, while others report silent sync/outbox failure or draft loss.
- **Proton native desktop + Bridge:** provider-specific privacy incumbent. Bridge decrypts locally and feeds a local client, is available only on paid Proton plans, and creates an unusually concrete provider-controlled client-selection surface.
- **Tuta desktop:** provider-specific, free, cross-platform, encrypted cache/offline claim, but it is not a broad multi-provider client and therefore does not complete the multi-account/provider-switching jobs observed here.
- **Betterbird/Owl add-on/legacy versions/browser profiles:** observed workarounds when mainstream account setup fails. They solve the immediate access problem at the cost of extra client choice, paid add-ons, version pinning, or fragmented identity contexts.

## Registry by underlying job

### J1. Connect or reauthenticate every existing account without weakening security

- **Evidence count/diversity:** 6 direct observations (O1–O6); 4 distinct surface types: two vendor support communities, independent Reddit, and a public issue tracker; Google, Microsoft, employer/university Exchange, Hotmail/Outlook, and a small custom-domain host.
- **Possible complete free outcome:** yes for mainstream accounts when automatic configuration selects current OAuth, provider login returns cleanly to the client, and errors expose an actionable recovery path. Thunderbird, Apple Mail, and current Outlook demonstrate that the user-facing outcome can be free. It is not complete for every institutional Exchange/OWA tenant or provider policy.
- **Zero-user source:** Proton Bridge setup, Fastmail client setup, Microsoft modern-auth help, Gmail third-party-client help, Yahoo IMAP help, and organic troubleshooting queries all reach people before installing a new client.
- **Evidenced recommender/sharing actor and surface:** Microsoft Support explicitly recommends current Outlook and documents Thunderbird/Apple Mail; Proton officially supports named clients; Fastmail lists named clients; independent users recommend Betterbird, Owl, or switching clients in troubleshooting threads.
- **Same-person paid adjacency:** O3 is a paid eM Client Personal-license user who wants to keep a university Exchange account. G2 also has a reviewer who paid for Mailspring to manage all mail. Proton Bridge users necessarily have a paid Proton plan, but that is provider payment, not proof of willingness to pay for a broader client.
- **Exact blockers:** OAuth application verification; external-browser/passkey callback handling; Microsoft tenant admin consent and Conditional Access; Exchange/OWA/EWS/Graph/ActiveSync protocol decisions; SMTP vs. IMAP vs. POP scopes; provider-specific autoconfiguration; cookies/system browser; keychain/keyring availability; version regressions; support for custom domains that resolve to a mainstream provider; honest error/recovery UX.
- **Next materially different query:** first-person Microsoft 365 administrator and university IT threads about why specific desktop clients are approved or blocked, including admin-consent, Conditional Access, and client-certification requirements. This tests the organizational gate rather than another end-user OAuth symptom.

### J2. Keep account, alias, and human identity explicit at compose/reply time

- **Evidence count/diversity:** 3 direct observations (O7–O9); official support community, independent Q&A, and independent provider community; eM Client, Apple Mail/Exchange, Proton/Spark/Bridge contexts.
- **Possible complete free outcome:** plausibly yes. A client can preserve distinct accounts/identities, show a highly visible From context, derive the reply identity where unambiguous, and force a choice where the same message reached multiple managed identities. Free incumbents already support multiple identities; the missing piece is predictable intent handling, not necessarily a paid service.
- **Zero-user source:** provider client-setup guides for Fastmail/Proton/Microsoft; organic “wrong sender” Q&A; app review/category pages for multi-account clients.
- **Evidenced recommender/sharing actor and surface:** G2 reviewer says paid Mailspring handles per-account aliases smoothly; Proton commenters direct users to Outlook, Thunderbird, Evolution, or Apple Mail; Ask Different shares folder-context workarounds.
- **Same-person paid adjacency:** the G2 validated reviewer explicitly paid for Mailspring to manage all mail and cited smooth alias handling. O3 and O12's thread also include paid eM Client users, though their payment is not specifically attributed to identity handling.
- **Exact blockers:** ambiguity when one message targets multiple managed addresses; aliases versus independent accounts versus delegated/shared mailboxes; provider enforcement of From/SPF/DKIM; hidden account-service failures that remove an identity; reply-to versus From semantics; unified inbox context; shared-account authorization; avoiding accidental impersonation without making every send noisy.
- **Next materially different query:** firsthand professional incidents where a wrong sender identity caused confidentiality, client, legal, or reputational harm across two real work domains. Avoid generic “choose From” requests; look for consequence and the user's prevention behavior.

### J3. Trust local mail, drafts, outbox, and search when the network or provider is unreliable

- **Evidence count/diversity:** 3 primary observations (O10–O12) across independent provider community, validated app review, and privacy community; corroborated by O5's send/receive regression and Yahoo/Proton provider guidance.
- **Possible complete free outcome:** yes for local caching, durable drafts, visible outbox state, offline reading/search, and queued sending; Thunderbird and Tuta claim free versions of much of this. “Complete” must be defined: cached time range, attachments/body availability, offline compose/send queue, search index, encryption at rest, reconnect behavior, and explicit stale-state indicators.
- **Zero-user source:** travel/offline community queries, provider Bridge pages, app reviews, Flathub category, and privacy-provider comparison threads.
- **Evidenced recommender/sharing actor and surface:** Proton users recommend Bridge plus a native client specifically for offline copies; Yahoo tells users to ensure full-content download; G2 reviewers recommend or reject clients based on multi-inbox reliability.
- **Same-person paid adjacency:** G2 paid-client reviewer values the productivity of managing all mail; Proton Bridge is paid-provider adjacency; Tuta reserves instantaneous offline login for paid accounts. None proves a user paid a broader client specifically for offline reliability.
- **Exact blockers:** local database durability; encrypted local cache; attachment/body completeness; large-mailbox indexing and disk use; clear sync freshness per account; queued-send semantics; crash-safe draft writes; restart/reconnect recovery; provider Bridge availability; filesystem backup/restore; platform keychain/keyring; honest distinction between cached web wrapper and offline-first client.
- **Next materially different query:** firsthand accounts from frequent travelers, field workers, or unreliable-connectivity users where offline email was needed to complete a concrete deadline, including what data had to be present and what they paid for. This tests outcome value beyond general “offline mode.”

### J4. Know exactly who can access mailbox credentials/content when choosing a client

- **Evidence count/diversity:** 3 direct observations (O12–O14) plus the 2020 eM Client privacy thread inspected as corroboration; independent privacy forums and vendor-hosted support community.
- **Possible complete free outcome:** partially. A free client can connect directly, store tokens/content locally, publish a precise data-flow disclosure, and avoid a mailbox proxy. It cannot prevent the mailbox provider or recipients' providers from accessing ordinary unencrypted mail and should not imply it can.
- **Zero-user source:** privacy communities, provider-switching threads, client security/privacy pages, open-source repositories, and app reviews.
- **Evidenced recommender/sharing actor and surface:** privacy-community users name Apple Mail and Thunderbird as trusted local-process incumbents; a disclosed client developer provides a four-question trust checklist but is excluded as independent evidence; Mailspring publishes a security statement permitting local-only use.
- **Same-person paid adjacency:** O13 has new income explicitly allocated to privacy services; O14 says payment is acceptable for a provider; O12's thread includes an eM Client subscriber. Only the eM/Mailspring examples prove payment for a broader client, and neither proves local-only architecture caused the payment.
- **Exact blockers:** verifiable direct connections; OAuth token storage; telemetry/crash logs; link/open tracking; remote feature dependencies; local encryption/key management; privacy policy clarity; open-source versus signed binary trust; support workflows requesting logs or mail content; provider-side limits that a client cannot solve.
- **Next materially different query:** first-person security/compliance buyers rejecting or approving a desktop email client specifically because it proxies mailbox data, stores OAuth tokens remotely, or cannot document local-only processing. Prefer audit/procurement outcomes over general privacy opinions.

### J5. Switch provider or client without breaking a household or heterogeneous account portfolio

- **Evidence count/diversity:** 4 direct observations (O6, O9, O13, O14); independent provider/privacy communities plus official support community; mixed employer/custom-host accounts, parent-care access, an individual Gmail→Posteo move, and ISP-tied household mail.
- **Possible complete free outcome:** partially. A free desktop client can preserve multiple live accounts, local history, identities, and familiar workflows across a provider switch. Provider migration/forwarding, encrypted-provider bridges, custom domains, and household onboarding can create paid dependencies.
- **Zero-user source:** provider migration guides, ISP/provider communities, privacy forums, Fastmail/Proton setup directories, and organic searches for mixed-account clients.
- **Evidenced recommender/sharing actor and surface:** community members recommend Mailbox.org, Proton, Posteo, Apple Mail, Thunderbird, Outlook, Evolution, and eM Client; Fastmail and Proton publish provider-controlled setup lists.
- **Same-person paid adjacency:** O14 explicitly accepts paying for the new provider; O13 has funds earmarked for privacy services; O3 pays for eM Client; G2 reviewer pays Mailspring for multi-account use. The evidence joins payment and the broader job, but not always the same exact purchase.
- **Exact blockers:** importing old mail without uploading it through Tecotype infrastructure; aliases versus separate users; delegated access; app passwords and OAuth; custom domains; provider forwarding limitations; separate household credentials; encryption-provider bridges; training a less technical household member; preserving sent mail, folders, contacts, calendars, and default handler; avoiding a forced all-at-once migration.
- **Next materially different query:** detailed first-person migration diaries from ISP mail or Google Workspace/Microsoft 365 to another provider where two or more household/business identities had to remain live during a staged desktop transition. Look for actual sequence, breakage, rollback, and paid purchases.

## Boundary decisions and implications

1. **Provider authentication compatibility is a distribution-enabling core, not a side feature.** A provider cannot credibly recommend a client it does not test with its current OAuth, passkey, app-password, and account-policy flows.
2. **Exchange support is a boundary decision.** “Any IMAP provider” does not cover universities and organizations that expose only Exchange/OWA or restrict approved apps. Research must distinguish Outlook.com IMAP/OAuth from Microsoft 365 tenant policy and proprietary protocol support.
3. **Encrypted providers create a local integration opportunity and a feature-loss risk.** Proton Bridge proves a provider-supported local bridge can preserve the no-cloud-proxy boundary. The client may still lose provider-native encryption, filtering, calendar, invite, or alias behavior unless explicitly integrated and tested.
4. **Identity safety should not be reduced to a default-account preference.** The actor may be oneself, a parent, a client, an employer, or another delegated person. When intent is ambiguous, a quiet confirmation is more honest than a guessed From address.
5. **Offline must be specified and observable.** “Desktop,” “cached,” and “offline” are not synonyms. A trustworthy client must reveal what is local, what is stale, what is queued, and what will happen after reconnect.
6. **Privacy claims must stay narrow.** Local credentials and local mailbox contents are defensible. Claims that a client makes Gmail/Outlook mail private from those providers, or makes ordinary email end-to-end private, are contradicted by the trust model.
7. **No inspected surface proves a partnership.** Proton, Fastmail, Microsoft, Google, and Yahoo surfaces are concrete current placements, not evidence of willingness or commitment. They become distribution only with permanent pre-install introduction and an attributable first-action-to-paid funnel.

## Ranked follow-up, without commitment

1. **Microsoft 365 institutional approval and client-certification research** — materially different actor, highest blocker severity, and directly relevant to O3–O5.
2. **Proton Bridge supported-client qualification mechanics** — the clearest provider-controlled zero-user selection surface, with paid-provider adjacency and a structurally local data path.
3. **Wrong-sender consequence research** — current evidence proves the failure, but the economic/reputational consequence needs fresher professional cases.
4. **Offline completeness research with travelers/field workers** — distinguish cached reading from draft/outbox/search/reconnect reliability and determine paid value.
5. **Staged household/provider migration diaries** — tests whether a calm local desktop client can be the continuity layer while providers and identities change.

No opportunity above is a recommendation, commitment, or shipped-product claim.
