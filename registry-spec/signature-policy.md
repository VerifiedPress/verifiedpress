# ✍️ Signature Policy for VerifiedPress Credentials

This document outlines the approved cryptographic signature suites, proof formats, and verification constraints used in the VerifiedPress trust framework. These rules govern how Verifiable Credentials (VCs) are signed, verified, and deemed valid within the registry and downstream tools.

---

## ✅ Approved Signature Formats

| Format       | Suite                      | Canonical Use                   | Status |
|--------------|----------------------------|----------------------------------|--------|
| `ld+json`    | Ed25519Signature2020       | Publisher / Author credentials   | ✅ Primary |
| `jwt`        | EdDSA via detached JWS     | Lightweight/verifier-agnostic    | ✅ Supported |

---

## 🔍 Proof Requirements

### For `ld+json` Credentials

- ✅ Signature suite: `Ed25519Signature2020`
- ✅ Canonicalization: `URDNA2015`
- ✅ `proofPurpose`: `assertionMethod`
- ✅ `verificationMethod`: MUST be resolvable via issuer’s DID Document

### For `jwt` Credentials

- ✅ `alg`: MUST be `EdDSA`
- ✅ `iss`: MUST match `issuer` field in VC
- ✅ Detached signature using compact JWS
- 🔐 Expiry recommended via `exp` claim (optional)

---

## 🔐 Verification Flow

1. Extract VC and signature proof
2. Canonicalize input if `ld+json`
3. Resolve `verificationMethod` DID URL
4. Verify signature using Ed25519 public key
5. Check issuer against [registry](../registry-spec/registry-index.sample.json) for status and permission

---

## 🚫 Disallowed Signatures

| Reason | Disallowed |
|--------|------------|
| RSA-based proofs | ❌ Not forward-compatible |
| `secp256k1` (EcdsaSecp256k1) | ❌ Not supported in base resolver |
| Self-signed without registry approval | ❌ Must be explicitly registered |

---

## 📦 Subject DIDs

- ✅ All issued credentials must have subject IDs in the form of a DID
- Preferred: `did:web:{publisher-domain}`  
  _(e.g. `did:web:presspage.news`)_

---

## 📜 Proof Canonical Reference

- [W3C Verifiable Credentials Data Model](https://www.w3.org/TR/vc-data-model/)
- [Ed25519Signature2020 Suite](https://w3c-ccg.github.io/lds-ed25519-2020/)
- [JSON Web Signature (JWS)](https://datatracker.ietf.org/doc/html/rfc7515)

---

## 🧬 Future Support (Planned)

- 🔮 BBS+ signatures for selective disclosure
- 🧾 VC status lists (revocation and suspension)
- 🔀 DIDComm credential exchange with signature receipt receipts

---

This policy ensures all credentials in the VerifiedPress ecosystem are **interoperable**, **cryptographically verifiable**, and **registry-checkable**, laying the foundation for scalable trust.
