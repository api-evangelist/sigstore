# Sigstore

Sigstore is a set of free-to-use open source tools for signing, verifying, and protecting software supply chain artifacts. It provides a transparent and auditable signing infrastructure that eliminates the need for managing signing keys, making software supply chain security more accessible. The Sigstore ecosystem includes Cosign for artifact signing, Fulcio as the certificate authority, and Rekor as the cryptographically secure transparency log.

**Website:** https://www.sigstore.dev/  
**Documentation:** https://docs.sigstore.dev/  
**Getting Started:** https://docs.sigstore.dev/quickstart/quickstart-cosign/  
**GitHub:** https://github.com/sigstore  
**Blog:** https://blog.sigstore.dev/  

## APIs

### Rekor Transparency Log API

Rekor is a cryptographically secure, immutable transparency log for signed software releases. The public-good instance runs at `rekor.sigstore.dev`.

**Base URL:** `https://rekor.sigstore.dev`

**Key Endpoints:**
- `POST /api/v1/log/entries` — Add a new entry to the transparency log
- `GET /api/v1/log/entries/{entryUUID}` — Get a log entry by UUID
- `POST /api/v1/log/entries/retrieve` — Retrieve multiple entries by UUID or log index
- `POST /api/v1/index/retrieve` — Search the log index by artifact hash or signer email
- `GET /api/v1/log` — Get log information (tree size, tree ID)
- `GET /api/v1/log/proof` — Get consistency proof between tree sizes

### Fulcio Certificate Authority API

Fulcio is Sigstore's free Root CA for code signing certificates. It issues short-lived certificates based on OIDC identity tokens. The public instance runs at `fulcio.sigstore.dev`.

**Base URL:** `https://fulcio.sigstore.dev`

**Key Endpoints:**
- `POST /api/v2/signingCert` — Request a short-lived signing certificate
- `GET /api/v2/trustBundle` — Get the CA trust bundle (root certificates)
- `GET /api/v2/configuration` — Get supported OIDC issuers and CA configuration

### Cosign

Cosign is the Sigstore tool for signing and verifying container images and other OCI artifacts. Supports keyless signing using OIDC + Fulcio + Rekor.

**Documentation:** https://docs.sigstore.dev/cosign/signing/overview/  
**GitHub:** https://github.com/sigstore/cosign  

## Artifacts

### OpenAPI

| Spec | Description |
|---|---|
| [rekor-openapi.yaml](openapi/rekor-openapi.yaml) | Rekor Transparency Log REST API |
| [fulcio-openapi.json](openapi/fulcio-openapi.json) | Fulcio Certificate Authority REST API |

### Rules

| Ruleset | Description |
|---|---|
| [sigstore-rules.yml](rules/sigstore-rules.yml) | Spectral ruleset enforcing Sigstore API conventions |

### Capabilities

| Capability | Description |
|---|---|
| [software-supply-chain-security.yaml](capabilities/software-supply-chain-security.yaml) | Unified supply chain security workflow — signing, transparency log, certificate issuance |

**Shared Definitions:**

| Shared File | Description |
|---|---|
| [shared/rekor.yaml](capabilities/shared/rekor.yaml) | Rekor transparency log API consumed definition |
| [shared/fulcio.yaml](capabilities/shared/fulcio.yaml) | Fulcio certificate authority API consumed definition |

### JSON Schema

| Schema | Description |
|---|---|
| [sigstore-log-entry-schema.json](json-schema/sigstore-log-entry-schema.json) | Rekor log entry schema |
| [sigstore-certificate-schema.json](json-schema/sigstore-certificate-schema.json) | Fulcio signing certificate schema |

### JSON Structure

| Structure | Description |
|---|---|
| [sigstore-log-entry-structure.json](json-structure/sigstore-log-entry-structure.json) | Rekor log entry field documentation |

### JSON-LD

| Context | Description |
|---|---|
| [sigstore-context.jsonld](json-ld/sigstore-context.jsonld) | Sigstore supply chain security vocabulary linked data context |

### Examples

| Example | Description |
|---|---|
| [sigstore-create-log-entry-example.json](examples/sigstore-create-log-entry-example.json) | Create a Rekor transparency log entry |
| [sigstore-get-signing-cert-example.json](examples/sigstore-get-signing-cert-example.json) | Request a Fulcio signing certificate |
| [sigstore-search-log-index-example.json](examples/sigstore-search-log-index-example.json) | Search the Rekor log index by artifact hash |

### Vocabulary

| Vocabulary | Description |
|---|---|
| [sigstore-vocabulary.yml](vocabulary/sigstore-vocabulary.yml) | Sigstore domain vocabulary covering transparency logs, certificate authority, artifact signing, and verification |

## Common Properties

| Property | URL |
|---|---|
| Website | https://www.sigstore.dev/ |
| Documentation | https://docs.sigstore.dev/ |
| Getting Started | https://docs.sigstore.dev/quickstart/quickstart-cosign/ |
| GitHub Organization | https://github.com/sigstore |
| Blog | https://blog.sigstore.dev/ |
| Policy Controller | https://docs.sigstore.dev/policy-controller/overview/ |
| Security | https://docs.sigstore.dev/about/security/ |

## Tags

Certificate Authority, Code Signing, Containers, Cryptography, Open Source, PKI, Security, Software Supply Chain, Transparency Log

## Maintainers

- Kin Lane (kin@apievangelist.com)
