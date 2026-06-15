# Sigstore (sigstore)

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
