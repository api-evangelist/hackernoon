# Hackernoon

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

HackerNoon is an independent technology publishing platform and community CMS, founded in 2016
by David Smooke and headquartered in Edwards, Colorado. It operates a free library of 150,000+
practitioner-authored, human-edited technology stories from 35,000+ contributing engineers, and
open-sources the publishing software behind the site.

## Machine-readable surface (probed 2026-08-22)

**HackerNoon publishes no public API.** No OpenAPI, Swagger, GraphQL, MCP server, A2A agent card,
gRPC or WSDL contract was found on any HackerNoon-controlled host, including `api.hackernoon.com`.
Its `llms.txt` advertises a "Live content feed API (coming Q3 2026)" that has not shipped.

What it does publish, and what this profile captured:

| Surface | Where | Status |
|---|---|---|
| `llms.txt` | https://hackernoon.com/llms.txt | 200 — saved verbatim to `llms/` |
| `robots.txt` AI-access policy | https://hackernoon.com/robots.txt | 200 — saved verbatim to `llms/` |
| RSS 2.0 feeds (site + per tag) | https://hackernoon.com/feed | 200 |
| Sitemap index (34 sitemaps) | https://hackernoon.com/sitemap.xml | 200 |
| Status page (Checkly) | https://status.hackernoon.com | 200 |
| First-party npm packages | `@hackernoon/*` | 3 packages, front-end only |
| `/.well-known/` documents | all hosts | none — every path 404 |

## Notable findings

- **Three dead pointers inside HackerNoon's own machine-readable discovery documents.**
  `llms.txt` sends AI licensing traffic to `https://hackernoon.com/ai-licensing` (308 to the site
  root); `robots.txt` sends it to `https://business.hackernoon.com/ai-licensing` (404) and points
  at `https://hackernoon.com/llms-full.txt` (308 to the site root). The licensing product is
  advertised to machines; the pages describing it are gone.
- **A prose TDM reservation with no machine-readable form.** `llms.txt` reserves rights under
  Article 4 of EU Directive 2019/790 — the exact reservation TDMRep exists to express — but
  `/.well-known/tdmrep.json`, `/.well-known/rsl.xml` and `ai.txt` are all absent.
- **The only published consumption limit is `Crawl-delay: 10`** in robots.txt. No rate-limit
  response headers of any family were observed.
- **The @hackernoon npm packages are publishing components, not SDKs** — an icon library, a
  markdown editor and an upload widget. No `SDKs` pointer is emitted, because there is no API
  for an SDK to wrap.

## Links

- Website: https://hackernoon.com
- GitHub organization: https://github.com/hackernoon
- Business / pricing: https://business.hackernoon.com/business-blogging
- Help center: https://help.hackernoon.com
- Status: https://status.hackernoon.com
- Secondary-market listing: https://www.hiive.com/securities/hackernoon-stock
