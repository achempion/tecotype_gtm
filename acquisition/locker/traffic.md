# Locker search traffic

Research date: **2026-07-17**

Market: **Google United States, English, desktop Windows**

Target: **`inbox.locker`, including subdomains only where explicitly stated**

Search evidence is a point-in-time third-party snapshot. DataForSEO Labs
estimates rankings and traffic; the live SERPs show visible results, not
clicks. Neither source exposes Locker's analytics.

## Headline result

Locker has weak exact-brand visibility and no observed top-ten category
visibility in the two tested queries.

- Domain Rank Overview returned no items.
- Ranked Keywords returned no items.
- Relevant Pages returned no items.
- The live exact-brand query showed the homepage and founder Reddit post.
- The homepage did not appear in the tested top-ten category results.

This is consistent with a new product whose public release began on June 23.
It is not evidence that nobody searches for or visits Locker.

## Labs snapshot

| Endpoint | Result |
| --- | ---: |
| Domain Rank Overview | 0 items; `total_count` null |
| Ranked Keywords | 0 items; `total_count` null |
| Relevant Pages | 0 items; `total_count` null |
| Modeled organic ETV | Unavailable |
| Modeled paid ETV | Unavailable |

The API returned successful tasks with empty item sets. “No returned item” is
more accurate than an all-time zero.

## Live SERPs

### `inbox locker email client`

| Absolute position | Result |
| ---: | --- |
| 6 | [Locker homepage](https://www.inbox.locker/) |
| 7 | [Founder Reddit beta post](https://www.reddit.com/r/software/comments/1uemnda/mac_looking_for_beta_testers_for_locker_a/) |

The results above appeared after an AI Overview and several ambiguous products
using “Locker,” including a password-manager email-alias feature and
LockrMail. The new email client did not own the top organic result for its
descriptive brand query.

The homepage result title was:

> Locker — Email, with the cloud taken back out.

That is an earlier page title, not the current live title, “A private AI inbox
that runs on your Mac.” Search therefore captured the domain but had not
fully reflected the current landing page.

### `local AI email client Mac`

The Locker domain was absent from the returned top-ten page. Results included
established client roundups, Canary Mail, Airmail, Apple support, and Mailbird.

### `private AI email client Mac`

The Locker domain was also absent. Results included Canary Mail, an App Store
page, a roundup, a Reddit discussion, EmailOps, Apple support, and Mailbird.

These two queries were selected from Locker's actual local/private Mac
positioning. Their absence establishes only that Locker was not visible in
these two returned top-ten pages; it does not measure broader category
visibility, query quality, future demand, or click-through rate.

## Search readiness

Observed basics:

- Public `robots.txt` allows normal crawling.
- Public sitemap lists five pages.
- Homepage title and description state the product category and platform.
- The public changelog creates crawlable release content.

Observed limitations:

- No canonical URL was found in the homepage markup.
- No structured data or Open Graph image was found.
- Search still showed an older homepage title.
- The site has no category, comparison, use-case, provider, or help-content
  program beyond the product and policy pages.
- The brand is ambiguous with several unrelated “Locker” products.
- The current homepage overstates some in-testing capabilities, making more
  indexable feature pages risky until the release boundary is corrected.

## Acquisition conclusion

Current organic search is best described as partial brand capture. It is not a
repeatable category-acquisition system.

The Reddit post ranking immediately after the homepage is useful: a small,
specific community post can become a search result before the product domain
develops category authority. No public data shows whether either result
produced a download.

Tecotype should not infer that broad local-AI SEO is easy. A safer first test,
after the product and public funnel are ready, is one release-accurate page
around a concrete job:

- Find an email from remembered meaning.
- Process a real inbox from the keyboard.
- Work across Gmail and IMAP in one Mac client.

Success should be a source-attributed retained user or paid customer, not a
ranking alone.

## Request audit

Exact bodies, costs, task IDs, and the full result boundary are recorded in
[requests.md](./requests.md).
