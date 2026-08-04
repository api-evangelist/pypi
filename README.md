# PyPI (pypi)

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

PyPI (Python Package Index) is the official third-party software repository for Python, serving as the central hub where developers publish and distribute Python packages. Their developer platform provides a suite of APIs for querying package metadata, downloading distributions, publishing packages, verifying supply chain integrity, and tracking download statistics across the Python ecosystem.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/apis.yml)

## Tags

- Developer Tools
- Open Source
- Package Management
- Packages
- Python

## Timestamps

- **Created:** 2025-03-01
- **Modified:** 2026-05-19

## APIs

### PyPI JSON API

The PyPI JSON API provides metadata about individual Python packages hosted on the Python Package Index. It returns project-level information including the latest version, all available releases, download URLs, and hash digests for MD5, SHA256, and BLAKE2b-256. Developers can query endpoints like /pypi/{project}/json for the latest release metadata or /pypi/{project}/{version}/json for a specific version. Responses are cached by CDN and support ETag headers for conditional requests.

- **Human URL:** [https://docs.pypi.org/api/json/](https://docs.pypi.org/api/json/)

#### Tags

- Metadata
- Open Source
- Packages
- Python

#### Properties

- [Documentation](https://docs.pypi.org/api/json/)
- [OpenAPI](openapi/pypi-json-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/pypi-json-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-json-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PyPI Index API

The PyPI Index API implements the PEP 503 (HTML) and PEP 691 (JSON) simple repository standards for discovering and downloading Python packages. It provides a machine-readable index of all registered projects and their available distribution files. The API is available in both HTML and JSON formats, with JSON recommended for new integrations. This is the primary API that package installers like pip use to resolve and download dependencies from the Python Package Index.

- **Human URL:** [https://docs.pypi.org/api/index-api/](https://docs.pypi.org/api/index-api/)

#### Tags

- Index
- Packages
- PEP 503
- PEP 691
- Python

#### Properties

- [Documentation](https://docs.pypi.org/api/index-api/)
- [OpenAPI](openapi/pypi-index-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/pypi-index-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-index-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PyPI Integrity API

The PyPI Integrity API provides access to digital attestations and provenance information for Python package distribution files. It allows clients to retrieve cryptographic attestation bundles and Trusted Publishing metadata for individual release files, enabling verification of package authenticity and supply chain integrity. The API implements PEP 740 and returns provenance objects containing one or more Sigstore attestation bundles along with the identity that produced them. This endpoint is currently available in JSON format only.

- **Human URL:** [https://docs.pypi.org/api/integrity/](https://docs.pypi.org/api/integrity/)

#### Tags

- Attestations
- Provenance
- Python
- Security
- Supply Chain

#### Properties

- [Documentation](https://docs.pypi.org/api/integrity/)
- [OpenAPI](openapi/pypi-integrity-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/pypi-integrity-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-integrity-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PyPI Upload API

The PyPI Upload API is the endpoint used by tools like twine and build frontends to publish Python package distributions to the Python Package Index. Served at upload.pypi.org, it emulates the legacy PyPI upload interface and accepts source distributions and wheel files along with their metadata. The API also supports attaching PEP 740 digital attestations to uploads, which PyPI will verify before accepting. Authentication is handled via API tokens or Trusted Publishing workflows using OpenID Connect.

- **Human URL:** [https://docs.pypi.org/api/upload/](https://docs.pypi.org/api/upload/)

#### Tags

- Packages
- Publishing
- Python
- Upload

#### Properties

- [Documentation](https://docs.pypi.org/api/upload/)
- [OpenAPI](openapi/pypi-upload-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/pypi-upload-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-upload-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PyPI RSS Feeds

PyPI provides RSS feeds that allow developers and tools to monitor package activity on the Python Package Index. Three feeds are available: the Newest Packages feed for recently registered projects, the Latest Updates feed for the most recently updated projects, and per-project release feeds for tracking new versions of specific packages. These feeds enable integration with feed readers, monitoring tools, and automation workflows to stay informed about Python package ecosystem changes.

- **Human URL:** [https://docs.pypi.org/api/feeds/](https://docs.pypi.org/api/feeds/)

#### Tags

- Feeds
- Packages
- Python
- RSS
- Updates

#### Properties

- [Documentation](https://docs.pypi.org/api/feeds/)
- [Postman Collection](collections/pypi-index-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-index-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/pypi-integrity-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-integrity-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/pypi-json-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-json-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/pypi-stats-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-stats-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/pypi-upload-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-upload-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PyPI Stats API

The PyPI Stats API provides aggregate download statistics and time series data for Python packages hosted on PyPI. It offers JSON endpoints for querying download counts broken down by Python version, operating system, and time period. Time series data is retained for 180 days and all download statistics are updated once daily. The API is hosted at pypistats.org and serves as the primary programmatic interface for analyzing Python package adoption and download trends across the ecosystem.

- **Human URL:** [https://pypistats.org/api/](https://pypistats.org/api/)

#### Tags

- Analytics
- Downloads
- Packages
- Python
- Statistics

#### Properties

- [Documentation](https://pypistats.org/api/)
- [OpenAPI](openapi/pypi-stats-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/pypi-stats-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pypi-stats-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/pypi)
- [Portal](https://docs.pypi.org/)
- [Documentation](https://docs.pypi.org/api/)
- [Website](https://pypi.org/)
- [Privacy Policy](https://policies.python.org/pypi.org/Privacy-Policy/)
- [Terms of Service](https://policies.python.org/pypi.org/Terms-of-Use/)
- [Support](https://pypi.org/help/)
- [Blog](https://blog.pypi.org/)
- [Login](https://pypi.org/account/login/)

## Maintainers

**FN:** API Evangelist
**Email:** info@apievangelist.com
