# 🔐 VerifiedPress Trust Framework

The VerifiedPress Trust Framework defines the technical and ethical infrastructure for issuing, verifying, and governing Verifiable Credentials (VCs) in the digital publishing ecosystem.

It provides credential schemas, signature policies, DID usage patterns, and registry interfaces for trust-based identity in editorial, journalistic, and content distribution systems.

---

## 🧭 Guiding Principles

- **Verifiability > Virality**  
  Truth deserves cryptographic backing, not just amplification.

- **Editorial trust is earned**  
  The framework models legitimacy through transparent credential issuance—not popularity.

- **Interoperable by design**  
  All schemas, DIDs, and credential flows follow W3C and DIF standards for cross-platform compatibility.

---

## 📦 Components

| Section | Description |
|--------|-------------|
| [`schemas/`](./schemas/) | JSON Schemas for Verifiable Credentials (e.g. `VerifiedPublisherCredential`) |
| [`contexts/`](../public-ui/contexts/) | JSON-LD Contexts for semantic integrity (hosted at `verifiedpress.org`) |
| [`signature-policy.md`](../registry-spec/signature-policy.md) | Allowed signature formats, algorithms, and constraints |
| [`vcip/`](../vcip/) | Community proposals for evolving the framework (VCIPs) |

---

## 📜 Core Credential Types

- `VerifiedPublisherCredential`  
  Proof of ownership and editorial responsibility for a domain or publishing entity

- *(Planned)* `VerifiedAuthorCredential`  
  Link individual contributors to verifiable publisher records and reputation metadata

- *(Planned)* `FactCheckEndorsement`  
  Signed cross-references between fact-checkers, publishers, and claims

---

## 🧱 DID Architecture

- ✅ Default issuer: `did:web:verifiedpress.org`
- 🪪 Subject identifiers: `did:web:{publisher-domain}` (e.g. `did:web:presspage.news`)
- 🔧 Designed for future support of `did:key`, `did:ion`, and other DID methods

---

## 🔄 Verification Flow

1. Load VC + linked data context
2. Validate schema + signature (Ed25519, etc)
3. Resolve issuer DID and check against registry
4. Trust outcome: ✅ (trusted issuer + valid VC) or ❌ (unknown or revoked)

---

## 🤝 Contribute

We welcome community proposals, schema extensions, and tooling integrations.

- Start with [`vcip/template.md`](../vcip/template.md)
- Review open proposals in [`vcip/`](../vcip/)
- Join discussions on data model evolution and registry onboarding

---

## 📜 License

All framework components are open-source and available under the [Apache 2.0 License](../LICENSE).
