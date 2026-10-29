# Astronomer

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

Astronomer is the company behind Astro, a fully managed data operations platform powered by Apache Airflow. Astro lets data teams author, orchestrate, run, and observe data pipelines (DAGs) at scale across a managed control plane and data plane. The Astro Platform API is a production-ready REST API for programmatic control of Astro resources — Organizations, Workspaces, Deployments, Clusters, Users, Teams, role-based access control, API tokens, deploys, and environment objects — authenticated with bearer API tokens. Astronomer also ships the Astro CLI, an official Terraform provider, the Astro Python SDK, a documentation MCP server, and Astro Runtime, its distribution of Apache Airflow.

**Areas:** Company · Data Orchestration · Apache Airflow · Data Pipeline · Data Engineering · Workflow Automation · MLOps · Managed Platform

## Astronomer on APIs.io

Everything profiled for Astronomer is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/astronomer/](https://apis.io/providers/astronomer/)** — or go straight to one of the APIs or properties below.

### APIs (15)

- [Astronomer AllowedIpAddressRange API](https://apis.io/apis/astronomer/astronomer-allowedipaddressrange-api/) — The AllowedIpAddressRange API from Astronomer — 4 operation(s) for allowedipaddressrange.
- [Astronomer Authorization API](https://apis.io/apis/astronomer/astronomer-authorization-api/) — The Authorization API from Astronomer — 1 operation(s) for authorization.
- [Astronomer Cluster API](https://apis.io/apis/astronomer/astronomer-cluster-api/) — A `cluster` object represents an Astro cluster, which is a Kubernetes cluster that hosts the infrastructure required to run Deployments. Make requests to…
- [Astronomer Deploy API](https://apis.io/apis/astronomer/astronomer-deploy-api/) — The Deploy API from Astronomer — 4 operation(s) for deploy.
- [Astronomer Deployment API](https://apis.io/apis/astronomer/astronomer-deployment-api/) — The `deployment` object represents an Astro Deployment, which is a hosted Airflow environment that is powered by all core Airflow components, including…
- [Astronomer Environment API](https://apis.io/apis/astronomer/astronomer-environment-api/) — The Environment API from Astronomer — 3 operation(s) for environment.
- [Astronomer Invite API](https://apis.io/apis/astronomer/astronomer-invite-api/) — The Invite API from Astronomer — 2 operation(s) for invite.
- [Astronomer Options API](https://apis.io/apis/astronomer/astronomer-options-api/) — The Options API from Astronomer — 2 operation(s) for options.
- [Astronomer Organization API](https://apis.io/apis/astronomer/astronomer-organization-api/) — The `organization` object contains the metadata and configurations of an Astro Organization. It does not include objects within the Organization, such as…
- [Astronomer Role API](https://apis.io/apis/astronomer/astronomer-role-api/) — The Role API from Astronomer — 4 operation(s) for role.
- [Astronomer Team API](https://apis.io/apis/astronomer/astronomer-team-api/) — The `team` object represents an Astro Team, which is a group of users that share the same permissions across your Organization and Workspaces. Make requests…
- [Astronomer User API](https://apis.io/apis/astronomer/astronomer-user-api/) — The `user` object represents a user account in your Astro Organization. Astro creates a new `user` object whenever you invite a user by email or add a user…
- [Astronomer Workspace API](https://apis.io/apis/astronomer/astronomer-workspace-api/) — The `workspace` object represents an Astro Workspace, which is a collection of Deployments that can be accessed by a specific group of users. It contains…
- [Astronomer Agent Token API](https://apis.io/apis/astronomer/astronomer-agent-token-api/) — The Agent Token API from Astronomer — 2 operation(s) for agent token.
- [Astronomer API Token API](https://apis.io/apis/astronomer/astronomer-api-token-api/) — The `apitoken` object represents a single API token within your Organization. API tokens are used to authenticate automated tools and processes to your…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [fern-docs-mcp-server](https://apis.io/servers/astronomer/fern-docs-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Astronomer Agentic Access](https://apis.io/agentic-access/astronomer/astronomer-agentic-access/)

#### Collections (15)

Postman and Open Collection request collections.

- [Astro Platform AgentToken API](https://apis.io/collections/astronomer/open-astronomer-agenttoken-api/)
- [Astro Platform AgentToken AllowedIpAddressRange API](https://apis.io/collections/astronomer/open-astronomer-allowedipaddressrange-api/)
- [Astro Platform AgentToken ApiToken API](https://apis.io/collections/astronomer/open-astronomer-apitoken-api/)
- [Astro Platform AgentToken Authorization API](https://apis.io/collections/astronomer/open-astronomer-authorization-api/)
- [Astro Platform AgentToken Cluster API](https://apis.io/collections/astronomer/open-astronomer-cluster-api/)
- [Astro Platform AgentToken Deploy API](https://apis.io/collections/astronomer/open-astronomer-deploy-api/)
- [Astro Platform AgentToken Deployment API](https://apis.io/collections/astronomer/open-astronomer-deployment-api/)
- [Astro Platform AgentToken Environment API](https://apis.io/collections/astronomer/open-astronomer-environment-api/)
- [Astro Platform AgentToken Invite API](https://apis.io/collections/astronomer/open-astronomer-invite-api/)
- [Astro Platform AgentToken Options API](https://apis.io/collections/astronomer/open-astronomer-options-api/)
- [Astro Platform AgentToken Organization API](https://apis.io/collections/astronomer/open-astronomer-organization-api/)
- [Astro Platform AgentToken Role API](https://apis.io/collections/astronomer/open-astronomer-role-api/)
- [Astro Platform AgentToken Team API](https://apis.io/collections/astronomer/open-astronomer-team-api/)
- [Astro Platform AgentToken User API](https://apis.io/collections/astronomer/open-astronomer-user-api/)
- [Astro Platform AgentToken Workspace API](https://apis.io/collections/astronomer/open-astronomer-workspace-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Astronomer Astro Overlay](https://apis.io/overlays/astronomer/astronomer-astro-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Astronomer Authentication](https://apis.io/security/astronomer/astronomer-authentication/)
- [Astronomer Domain Security](https://apis.io/security/astronomer/astronomer-domain-security/)
- [Astronomer Trust Center](https://apis.io/security/astronomer/astronomer-trust-center/)
- [Astronomer Vulnerability Disclosure](https://apis.io/security/astronomer/astronomer-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://astronomer.io)
- [Documentation](https://www.astronomer.io/docs)
- [Getting started](https://www.astronomer.io/docs/astro/api/v-1/get-started)
- [Pricing](https://www.astronomer.io/pricing)
- [Sign up](https://www.astronomer.io/try-astro/)
- [Blog](https://www.astronomer.io/blog/)
- [Security](https://www.astronomer.io/vulnerability-disclosure/)
- [Compliance](https://trust.astronomer.io)
- [Terms of service](https://www.astronomer.io/legal/terms-of-service)
- [Privacy policy](https://www.astronomer.io/privacy)
- [GitHub](https://github.com/astronomer)
- [Status](https://status.astronomer.io)

## API Evangelist rating

**Kin Score 52.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 41.0 |
| Contract governance | 4.5 |
| Operational transparency | 52.6 |
| Developer ergonomics | 63.2 |
| Access clarity | 60.5 |

**Agent readiness 30.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | verified |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/astronomer/](https://apis.io/providers/astronomer/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Astronomer: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/astronomer/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
