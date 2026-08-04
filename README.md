# Blacksmith (blacksmith-sh)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Blacksmith runs your GitHub Actions up to 2x faster at half the cost on a fleet of modern gaming-CPU bare metal, booting ephemeral Firecracker microVMs in under three seconds. It is a drop-in replacement integrated as a GitHub App and selected via runs-on runner tags, with a co-located CI cache, 40x faster Docker layer caching, sticky disks, an observability dashboard, and a Testbox CLI. Blacksmith does not publish a general-purpose public REST API - integration is GitHub-App, YAML runner-tag, and GitHub Actions based.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/blacksmith-sh/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/blacksmith-sh/refs/heads/main/apis.yml)

## Tags

- CI/CD
- GitHub Actions
- Runners
- Caching
- Docker

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Blacksmith GitHub Actions Runners

Drop-in faster GitHub-hosted runner replacement selected by changing the runs-on tag (e.g. blacksmith-2vcpu-ubuntu-2404). Linux/Windows jobs run in ephemeral Firecracker microVMs; x64, ARM64, and macOS (Apple Silicon M4) families are offered in 2-32 vCPU sizes. Configured via the GitHub App and YAML workflow, not a programmatic REST API.

- **Human URL:** [https://docs.blacksmith.sh/blacksmith-runners/overview](https://docs.blacksmith.sh/blacksmith-runners/overview)
- **Base URL:** `https://app.blacksmith.sh`

#### Tags

- GitHub Actions
- Runners
- CI/CD
- Firecracker

#### Properties

- [Documentation](https://docs.blacksmith.sh/blacksmith-runners/overview)
- [API Reference](https://docs.blacksmith.sh/introduction/quickstart)
- [OpenAPI](openapi/blacksmith-sh-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/blacksmith-sh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/blacksmith-sh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Blacksmith Docker Builds

Accelerated Docker image builds via Blacksmith's BuildKit and the useblacksmith/build-push-action and useblacksmith/setup-docker-builder GitHub Actions, reusing cached layers on sticky disks to rebuild only what changed - up to 40x faster. Used as GitHub Actions in a workflow, not via a public REST API.

- **Human URL:** [https://docs.blacksmith.sh/blacksmith-caching/docker-builds](https://docs.blacksmith.sh/blacksmith-caching/docker-builds)
- **Base URL:** `https://app.blacksmith.sh`

#### Tags

- Docker
- BuildKit
- Layer Caching
- Builds

#### Properties

- [Documentation](https://docs.blacksmith.sh/blacksmith-caching/docker-builds)
- [OpenAPI](openapi/blacksmith-sh-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/blacksmith-sh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/blacksmith-sh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Blacksmith Cache

Co-located CI cache that transparently backs official GitHub and popular third-party cache actions (e.g. actions/cache, useblacksmith/cache) at roughly 400MB/s, plus Sticky Disks, container init pre-hydration, and Git checkout caching. Activated by running cache GitHub Actions on Blacksmith runners, not via a public REST API.

- **Human URL:** [https://docs.blacksmith.sh/blacksmith-caching/dependencies-actions](https://docs.blacksmith.sh/blacksmith-caching/dependencies-actions)
- **Base URL:** `https://app.blacksmith.sh`

#### Tags

- Cache
- Sticky Disks
- Dependencies
- Artifacts

#### Properties

- [Documentation](https://docs.blacksmith.sh/blacksmith-caching/dependencies-actions)
- [OpenAPI](openapi/blacksmith-sh-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/blacksmith-sh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/blacksmith-sh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Blacksmith Testbox CLI

Command-line interface (beta) that lets coding agents run CI against local changes instantly - blacksmith testbox warmup/run/status dispatch a workflow to a warm microVM, rsync local changes, and execute commands over SSH. The CLI is the programmatic surface; there is no documented public REST API.

- **Human URL:** [https://docs.blacksmith.sh/blacksmith-testbox/cli](https://docs.blacksmith.sh/blacksmith-testbox/cli)
- **Base URL:** `https://app.blacksmith.sh`

#### Tags

- CLI
- Testbox
- Coding Agents
- Beta

#### Properties

- [Documentation](https://docs.blacksmith.sh/blacksmith-testbox/cli)
- [API Reference](https://docs.blacksmith.sh/blacksmith-testbox/overview)
- [Postman Collection](collections/blacksmith-sh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/blacksmith-sh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Blacksmith Dashboard and Observability

Web dashboard at app.blacksmith.sh for organization setup, runner and cache management, and observability - CI analytics, run history, logs, machine metrics, monitors, SSH access, and test analytics. A management console, not a documented public REST API.

- **Human URL:** [https://docs.blacksmith.sh/blacksmith-observability/dashboard](https://docs.blacksmith.sh/blacksmith-observability/dashboard)
- **Base URL:** `https://app.blacksmith.sh`

#### Tags

- Dashboard
- Observability
- Analytics
- Management

#### Properties

- [Documentation](https://docs.blacksmith.sh/blacksmith-observability/dashboard)
- [Console](https://app.blacksmith.sh)
- [Postman Collection](collections/blacksmith-sh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/blacksmith-sh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/useblacksmith)
- [LinkedIn](https://www.linkedin.com/company/useblacksmith)
- [Website](https://www.blacksmith.sh/)
- [Documentation](https://docs.blacksmith.sh)
- [Console](https://app.blacksmith.sh)
- [Status](https://status.blacksmith.sh)
- [Plans](plans/blacksmith-sh-plans-pricing.yml)
- [Rate Limits](rate-limits/blacksmith-sh-rate-limits.yml)
- [Fin Ops](finops/blacksmith-sh-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
