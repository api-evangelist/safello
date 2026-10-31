# Safello

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

Safello is a Swedish cryptocurrency brokerage founded in 2013, registered with the Swedish Financial Supervisory Authority (Finansinspektionen) and listed on Nasdaq First North Growth Market since 2021. It lets people buy, sell, trade, and store digital assets, and exposes a "Cryptocurrency as a Service" (CaaS) Institutional API so third-party organisations can embed crypto buying/selling, BankID customer onboarding, KYC and compliance verification, market data, order management, and wallet balances. The v2 Institutional API (base https://api.safello.com) uses OAuth2 with client-credentials, authorization-code, and a custom Swedish BankID grant, plus a staging environment at api.s4f3.io for testing.

**Areas:** Company · Fintech · Cryptocurrency · Bitcoin · Brokerage · Payments · Sweden · Trading · KYC · BankID · Financial Services

## Safello on APIs.io

Everything profiled for Safello is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/safello/](https://apis.io/providers/safello/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Safello Account API](https://apis.io/apis/safello/safello-account-api/) — Account management
- [Safello Auth API](https://apis.io/apis/safello/safello-auth-api/) — Authentication flow
- [Safello Compliance API](https://apis.io/apis/safello/safello-compliance-api/) — User's compliance information/status
- [Safello Market API](https://apis.io/apis/safello/safello-market-api/) — Market endpoints
- [Safello Orders API](https://apis.io/apis/safello/safello-orders-api/) — Buy and sell crypto
- [Safello Prices API](https://apis.io/apis/safello/safello-prices-api/) — Price endpoints
- [Safello Wallet API](https://apis.io/apis/safello/safello-wallet-api/) — User's wallet

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (2)

Multi-step workflows that chain operations into a business task.

- [Safello — buy cryptocurrency](https://apis.io/arazzos/safello/safello-buy-crypto/)
- [Safello — onboard a customer with BankID](https://apis.io/arazzos/safello/safello-onboard-customer/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [safello](https://apis.io/servers/safello/safello/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Safello Agentic Access](https://apis.io/agentic-access/safello/safello-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [Safello account API](https://apis.io/collections/safello/open-safello-account-api/)
- [Safello account auth API](https://apis.io/collections/safello/open-safello-auth-api/)
- [Safello account compliance API](https://apis.io/collections/safello/open-safello-compliance-api/)
- [Safello account market API](https://apis.io/collections/safello/open-safello-market-api/)
- [Safello account orders API](https://apis.io/collections/safello/open-safello-orders-api/)
- [Safello account prices API](https://apis.io/collections/safello/open-safello-prices-api/)
- [Safello account wallet API](https://apis.io/collections/safello/open-safello-wallet-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Safello Institutional Overlay](https://apis.io/overlays/safello/safello-institutional-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Safello Authentication](https://apis.io/security/safello/safello-authentication/)
- [Safello Domain Security](https://apis.io/security/safello/safello-domain-security/)
- [Safello Vulnerability Disclosure](https://apis.io/security/safello/safello-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Safello Scopes](https://apis.io/scopes/safello/safello-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://safello.com)
- [Documentation](https://safello.github.io/safello-api/docs/intro)
- [Getting started](https://safello.github.io/safello-api/docs/getting-started/getting-started-intro)
- [API reference](https://safello.github.io/safello-api/api)
- [Pricing](https://help.safello.com/en/articles/166728-what-are-safello-s-fees)
- [Sign up](https://app.safello.com)
- [Support](https://help.safello.com/en/)
- [Security](https://safello.com/security-bug-bounty)
- [Terms of service](https://safello.com/legal/terms)
- [Privacy policy](https://safello.com/legal/privacy)
- [GitHub](https://github.com/safello)

## API Evangelist rating

**Kin Score 50.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 52.3 |
| Contract governance | 18.2 |
| Operational transparency | 13.2 |
| Developer ergonomics | 63.7 |
| Access clarity | 44.7 |

**Agent readiness 34.5** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 36.6** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/safello/](https://apis.io/providers/safello/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Safello: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/safello/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
