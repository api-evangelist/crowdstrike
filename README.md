# CrowdStrike

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

CrowdStrike is a US cybersecurity company and Fortune 1000 constituent whose Falcon platform delivers endpoint, cloud, identity and data protection from a single cloud-native agent. Its developer surface is substantial and public: a 1,463-operation OAuth2 REST API spanning 128 service collections, documented operation by operation on developer.crowdstrike.com, with 187 named permission scopes; six official SDKs (Python, PowerShell, Go, TypeScript/JavaScript, Rust, Ruby); a Terraform provider for Configuration as Code; Falcon Foundry, an app platform with its own CLI; a first-party open-source MCP server (falcon-mcp) exposing 166 agent tools across 28 modules; and a published set of Agent Skills for building Foundry apps. CrowdStrike does not publish an OpenAPI document, and API access requires a Falcon subscription — the API itself is included in every paid bundle.

**Areas:** Cybersecurity · Endpoint Security · Endpoint Detection and Response · Threat Intelligence · Cloud Security · Identity Protection · Vulnerability Management · SIEM · Security Operations · MCP

## CrowdStrike on APIs.io

Everything profiled for CrowdStrike is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/crowdstrike/](https://apis.io/providers/crowdstrike/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [CrowdStrike API](https://apis.io/apis/crowdstrike/crowdstrike-api/) — The CrowdStrike Falcon API — 1,463 documented operations across 128 service collections covering hosts, detections, incidents, real-time response, threat…
- [Falcon MCP Server](https://apis.io/apis/crowdstrike/falcon-mcp/) — CrowdStrike's first-party open-source MCP server. Self-hosted (uvx/pip/Docker/Bedrock/Cloud Run) and authenticated with the operator's own Falcon API…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Crowdstrike Event Streams](https://apis.io/asyncapis/crowdstrike/crowdstrike-event-streams/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [CrowdStrike Falcon MCP Server](https://apis.io/servers/crowdstrike/io-github-crowdstrike-falcon-mcp/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Crowdstrike Context](https://apis.io/jsonld/crowdstrike/crowdstrike-context/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [CrowdStrike API Rules](https://apis.io/rules/crowdstrike/crowdstrike-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Crowdstrike Authentication](https://apis.io/security/crowdstrike/crowdstrike-authentication/)
- [Crowdstrike Domain Security](https://apis.io/security/crowdstrike/crowdstrike-domain-security/)
- [Crowdstrike Trust Center](https://apis.io/security/crowdstrike/crowdstrike-trust-center/)
- [Crowdstrike Vulnerability Disclosure](https://apis.io/security/crowdstrike/crowdstrike-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Crowdstrike Scopes](https://apis.io/scopes/crowdstrike/crowdstrike-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Crowdstrike Plans Pricing](https://apis.io/plans/crowdstrike/crowdstrike-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Crowdstrike Rate Limits](https://apis.io/rate-limits/crowdstrike/crowdstrike-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Crowdstrike Finops](https://apis.io/finops/crowdstrike/crowdstrike-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.crowdstrike.com)
- [Documentation](https://developer.crowdstrike.com/)
- [Getting started](https://developer.crowdstrike.com/sdks/go/getting-started/)
- [API reference](https://developer.crowdstrike.com/api-reference/overview/)
- [Pricing](https://www.crowdstrike.com/en-us/pricing/)
- [Sign up](https://www.crowdstrike.com/en-us/products/trials/try-falcon/)
- [Support](https://supportportal.crowdstrike.com/)
- [Blog](https://www.crowdstrike.com/blog/feed/)
- [Security](https://www.crowdstrike.com/en-us/report-a-security-bug/)
- [Compliance](https://trust.crowdstrike.com/)
- [Terms of service](https://www.crowdstrike.com/en-us/legal/website-terms-of-use/)
- [Privacy policy](https://www.crowdstrike.com/en-us/legal/privacy-notice/)
- [GitHub](https://github.com/CrowdStrike)

## API Evangelist rating

**Kin Score 65.6** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.3 |
| Contract quality | 39.0 |
| Contract governance | 18.2 |
| Operational transparency | 50.0 |
| Developer ergonomics | 78.6 |
| Access clarity | 92.1 |

**Agent readiness 35.1** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | yes |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 52.9** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/crowdstrike/](https://apis.io/providers/crowdstrike/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for CrowdStrike: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/crowdstrike/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
