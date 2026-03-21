# PyPI (pypi)
PyPI (Python Package Index) is the official third-party software repository for Python, serving as the central hub where developers publish and distribute Python packages. Their developer platform provides a suite of APIs for querying package metadata, downloading distributions, publishing packages, verifying supply chain integrity, and tracking download statistics across the Python ecosystem.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Packages, Python, Open Source, Package Management, Developer Tools

## Timestamps

- **Created:** 2025-03-01
- **Modified:** 2026-03-20

## APIs

### PyPI JSON API
The PyPI JSON API provides metadata about individual Python packages hosted on the Python Package Index. It returns project-level information including the latest version, all available releases, download URLs, and hash digests for MD5, SHA256, and BLAKE2b-256. Developers can query endpoints like /pypi/{project}/json for the latest release metadata or /pypi/{project}/{version}/json for a specific version. Responses are cached by CDN and support ETag headers for conditional requests.

**Human URL:** [https://docs.pypi.org/api/json/](https://docs.pypi.org/api/json/)


#### Tags:

 - Packages, Python, Metadata, Open Source

#### Properties

- [Documentation](https://docs.pypi.org/api/json/)
- [OpenAPI](openapi/pypi-json-api-openapi.yml)

### PyPI Index API
The PyPI Index API implements the PEP 503 (HTML) and PEP 691 (JSON) simple repository standards for discovering and downloading Python packages. It provides a machine-readable index of all registered projects and their available distribution files. The API is available in both HTML and JSON formats, with JSON recommended for new integrations. This is the primary API that package installers like pip use to resolve and download dependencies from the Python Package Index.

**Human URL:** [https://docs.pypi.org/api/index-api/](https://docs.pypi.org/api/index-api/)


#### Tags:

 - Packages, Python, Index, PEP 503, PEP 691

#### Properties

- [Documentation](https://docs.pypi.org/api/index-api/)
- [OpenAPI](openapi/pypi-index-api-openapi.yml)

### PyPI Integrity API
The PyPI Integrity API provides access to digital attestations and provenance information for Python package distribution files. It allows clients to retrieve cryptographic attestation bundles and Trusted Publishing metadata for individual release files, enabling verification of package authenticity and supply chain integrity. The API implements PEP 740 and returns provenance objects containing one or more Sigstore attestation bundles along with the identity that produced them. This endpoint is currently available in JSON format only.

**Human URL:** [https://docs.pypi.org/api/integrity/](https://docs.pypi.org/api/integrity/)


#### Tags:

 - Security, Attestations, Provenance, Supply Chain, Python

#### Properties

- [Documentation](https://docs.pypi.org/api/integrity/)
- [OpenAPI](openapi/pypi-integrity-api-openapi.yml)

### PyPI Upload API
The PyPI Upload API is the endpoint used by tools like twine and build frontends to publish Python package distributions to the Python Package Index. Served at upload.pypi.org, it emulates the legacy PyPI upload interface and accepts source distributions and wheel files along with their metadata. The API also supports attaching PEP 740 digital attestations to uploads, which PyPI will verify before accepting. Authentication is handled via API tokens or Trusted Publishing workflows using OpenID Connect.

**Human URL:** [https://docs.pypi.org/api/upload/](https://docs.pypi.org/api/upload/)


#### Tags:

 - Packages, Python, Publishing, Upload

#### Properties

- [Documentation](https://docs.pypi.org/api/upload/)
- [OpenAPI](openapi/pypi-upload-api-openapi.yml)

### PyPI RSS Feeds
PyPI provides RSS feeds that allow developers and tools to monitor package activity on the Python Package Index. Three feeds are available: the Newest Packages feed for recently registered projects, the Latest Updates feed for the most recently updated projects, and per-project release feeds for tracking new versions of specific packages. These feeds enable integration with feed readers, monitoring tools, and automation workflows to stay informed about Python package ecosystem changes.

**Human URL:** [https://docs.pypi.org/api/feeds/](https://docs.pypi.org/api/feeds/)


#### Tags:

 - Packages, Python, RSS, Feeds, Updates

#### Properties

- [Documentation](https://docs.pypi.org/api/feeds/)

### PyPI Stats API
The PyPI Stats API provides aggregate download statistics and time series data for Python packages hosted on PyPI. It offers JSON endpoints for querying download counts broken down by Python version, operating system, and time period. Time series data is retained for 180 days and all download statistics are updated once daily. The API is hosted at pypistats.org and serves as the primary programmatic interface for analyzing Python package adoption and download trends across the ecosystem.

**Human URL:** [https://pypistats.org/api/](https://pypistats.org/api/)


#### Tags:

 - Packages, Python, Statistics, Downloads, Analytics

#### Properties

- [Documentation](https://pypistats.org/api/)
- [OpenAPI](openapi/pypi-stats-api-openapi.yml)

## Common Properties

- [Portal](https://docs.pypi.org/)
- [Documentation](https://docs.pypi.org/api/)
- [Website](https://pypi.org/)
- [PrivacyPolicy](https://policies.python.org/pypi.org/Privacy-Policy/)
- [TermsOfService](https://policies.python.org/pypi.org/Terms-of-Use/)
- [Support](https://pypi.org/help/)
- [Blog](https://blog.pypi.org/)
- [Login](https://pypi.org/account/login/)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
