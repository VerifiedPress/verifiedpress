# 🏛️ VerifiedPress Trust Registry Specification

This directory defines the data structures, governance policies, and interoperability interfaces for the VerifiedPress Trust Registry.  
The registry is the authoritative source for identity verification metadata, issuer approvals, and credential audit records.

---

## 📚 Purpose

The Trust Registry enables:

- 💠 Resolution of trusted issuers (e.g. credentialing authorities, publisher onboarding bodies)
- 🔍 Discovery of credential schemas, signature suites, and public verification keys
- 🔐 Revocation and suspension checks for Verifiable Credentials
- 🧭 Governance metadata for decentralized trust signals (e.g. reputation, endorsements)

---

## 🧱 Directory Structure
```sh
registry-spec/ 
├── README.md                     # Overview and goals 
├── issuer-record.schema.json     # Schema: registry entry for approved issuers 
├── registry-index.sample.json    # Sample: registry snapshot (for dev/testing) 
├── registry-governance.md        # VCIP-compatible rules for issuer inclusion, audit logs, and dispute resolution 
└── signature-policy.md           # Signature formats and validation constraints
```


---

## 📑 Key Concepts

| Spec Element           | Description |
|------------------------|-------------|
| `issuer-record.schema.json` | Defines each trusted party’s DID, domains, credential types, and revocation endpoints |
| `registry-index.json`       | Lists all active issuers with relevant metadata (fetchable by agent/verifier) |
| `governance`                | Documents how registry entries are proposed, approved, and revoked |
| `signature-policy.md`       | Defines allowed signature suites (e.g. Ed25519Signature2020) and proof constraints |

---

## 🔄 Interoperability Targets

- DID methods: `did:web`, `did:key`, `did:ion`
- Credential suites: JWT, LD+JSON (w/ JSON-LD @context)
- Verification tools: Veramo, DIDKit, DIDAuth agents
- Publishable over: DNS, IPNS/IPFS, GitHub Pages, and well-known URLs

---

## 💬 Contributing

Propose improvements via [VCIPs](../vcip/README.md), especially for:

- Schema extensions (e.g. registry endorsements, publisher tiering)
- Governance rules (e.g. quorum for removal, reputation attestation)
- API proposals for machine-readable registry endpoints

---

## 📜 License

All registry specifications are available under the [Apache 2.0 License](../LICENSE).
