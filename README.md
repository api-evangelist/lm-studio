# LM Studio

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

LM Studio is a desktop application for discovering, downloading, and running large language models (Llama, DeepSeek, Phi, Qwen, gpt-oss, and others) locally on macOS, Windows, and Linux. It runs GGUF and MLX models via llama.cpp and Apple's MLX engine, and ships a local HTTP server that developers can drive from their own apps: a native LM Studio REST API (beta) under /api/v1 with generation stats, model load/unload/download and MCP-via-API, an OpenAI-compatible surface under /v1 (chat/completions, completions, embeddings, models, responses), and an Anthropic-compatible /v1/messages endpoint. It is complemented by Python (lmstudio) and TypeScript (@lmstudio/sdk) SDKs, the MIT-licensed lms command-line tool, headless/daemon operation, LM Link cross-device routing, and MCP host support. Backed by Matrix Partners.

**Areas:** Company · Artificial Intelligence · Local LLM · Machine Learning · Inference · Developer Tools · LLM · MCP · SDK · Desktop Application

## LM Studio on APIs.io

Everything profiled for LM Studio is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/lm-studio/](https://apis.io/providers/lm-studio/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [LM Studio Anthropic Compatibility API](https://apis.io/apis/lm-studio/lm-studio-anthropic-compatibility-api/) — Anthropic-compatible messages endpoint.
- [LM Studio Chat API](https://apis.io/apis/lm-studio/lm-studio-chat-api/) — Native LM Studio chat inference with generation stats.
- [LM Studio Models API](https://apis.io/apis/lm-studio/lm-studio-models-api/) — List, load, unload, and download local models.
- [LM Studio OpenAI Compatibility API](https://apis.io/apis/lm-studio/lm-studio-openai-compatibility-api/) — OpenAI-compatible endpoints for reuse of existing OpenAI clients.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [lm-studio](https://apis.io/servers/lm-studio/lm-studio/)

#### Collections (4)

Postman and Open Collection request collections.

- [LM Studio Local Server Anthropic Compatibility API](https://apis.io/collections/lm-studio/open-lm-studio-anthropic-compatibility-api/)
- [LM Studio Local Server Anthropic Compatibility Chat API](https://apis.io/collections/lm-studio/open-lm-studio-chat-api/)
- [LM Studio Local Server Anthropic Compatibility Models API](https://apis.io/collections/lm-studio/open-lm-studio-models-api/)
- [LM Studio Local Server Anthropic Compatibility OpenAI Compatibility API](https://apis.io/collections/lm-studio/open-lm-studio-openai-compatibility-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Lm Studio Server Overlay](https://apis.io/overlays/lm-studio/lm-studio-server-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Lm Studio Authentication](https://apis.io/security/lm-studio/lm-studio-authentication/)
- [Lm Studio Domain Security](https://apis.io/security/lm-studio/lm-studio-domain-security/)
- [Lm Studio Vulnerability Disclosure](https://apis.io/security/lm-studio/lm-studio-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://lmstudio.ai)
- [Documentation](https://lmstudio.ai/docs)
- [Getting started](https://lmstudio.ai/docs/app)
- [API reference](https://lmstudio.ai/docs/app/api/endpoints/rest)
- [Support](https://github.com/lmstudio-ai/lmstudio-bug-tracker)
- [Blog](https://lmstudio.ai/blog)
- [Security](https://lmstudio.ai/vulnerability-disclosure)
- [Terms of service](https://lmstudio.ai/terms)
- [Privacy policy](https://lmstudio.ai/privacy)
- [GitHub](https://github.com/lmstudio-ai)

## API Evangelist rating

**Kin Score 28.5** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 11.9 |
| Contract governance | 4.5 |
| Operational transparency | 2.6 |
| Developer ergonomics | 63.7 |
| Access clarity | 21.1 |

**Agent readiness 17.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
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

**Regulatory alignment 28.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/lm-studio/](https://apis.io/providers/lm-studio/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for LM Studio: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/lm-studio/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
