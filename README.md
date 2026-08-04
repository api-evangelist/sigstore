# Sigstore (sigstore)

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

Sigstore is a set of free-to-use open source tools for signing, verifying, and protecting software supply chain artifacts. It provides a transparent and auditable signing infrastructure that eliminates the need for managing signing keys, making software supply chain security more accessible. The Sigstore ecosystem includes Cosign for artifact signing, Fulcio as the certificate authority, and Rekor as the cryptographically secure transparency log.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Certificate Authority
- Code Signing
- Containers
- Cryptography
- Open Source
- PKI
- Security
- Software Supply Chain
- Transparency Log

## Timestamps

- **Created:** 2026-03-26
- **Modified:** 2026-05-19

## APIs

### Rekor Transparency Log API

Rekor is a cryptographically secure, immutable transparency log for signed software releases. The Rekor API enables searching the transparency log, retrieving log entries, checking proofs, and querying the log's public key. The public-good instance runs at rekor.sigstore.dev.

- **Human URL:** [https://docs.sigstore.dev/logging/overview/](https://docs.sigstore.dev/logging/overview/)
- **Base URL:** `https://rekor.sigstore.dev`

#### Tags

- Cryptography
- Security
- Software Supply Chain
- Transparency Log

#### Properties

- [Documentation](https://docs.sigstore.dev/logging/overview/)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/openapi/rekor-openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub Repository](https://github.com/sigstore/rekor)
- [Rules](https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/rules/sigstore-rules.yml)
- [Postman Collection](collections/fulcio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fulcio.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fulcio Certificate Authority API

Fulcio is Sigstore's free Root Certificate Authority for code signing certificates. It issues short-lived signing certificates to software producers based on OIDC authentication. The API provides endpoints for obtaining signing certificates, retrieving trust bundles, and querying CA configuration. The public instance runs at fulcio.sigstore.dev.

- **Human URL:** [https://docs.sigstore.dev/certificate_authority/overview/](https://docs.sigstore.dev/certificate_authority/overview/)
- **Base URL:** `https://fulcio.sigstore.dev`

#### Tags

- Certificate Authority
- Code Signing
- Cryptography
- OIDC
- PKI
- Security

#### Properties

- [Documentation](https://docs.sigstore.dev/certificate_authority/overview/)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/openapi/fulcio-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub Repository](https://github.com/sigstore/fulcio)
- [Postman Collection](collections/fulcio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fulcio.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cosign

Cosign is the Sigstore tool for signing and verifying container images and other OCI artifacts. It enables keyless signing using OIDC identity, hardware token signing, and policy enforcement for container supply chain security.

- **Human URL:** [https://docs.sigstore.dev/cosign/signing/overview/](https://docs.sigstore.dev/cosign/signing/overview/)

#### Tags

- Code Signing
- Containers
- OCI
- Security
- Software Supply Chain

#### Properties

- [Documentation](https://docs.sigstore.dev/cosign/signing/overview/)
- [GitHub Repository](https://github.com/sigstore/cosign)
- [Postman Collection](collections/fulcio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fulcio.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/sigstore)
- [Website](https://www.sigstore.dev/)
- [Documentation](https://docs.sigstore.dev/)
- [Getting Started](https://docs.sigstore.dev/quickstart/quickstart-cosign/)
- [GitHub Organization](https://github.com/sigstore)
- [Blog](https://blog.sigstore.dev/)
- [Community](https://sigstore.dev/community/)
- [Policy  Controller](https://docs.sigstore.dev/policy-controller/overview/)
- [Security](https://docs.sigstore.dev/about/security/)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/vocabulary/sigstore-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
