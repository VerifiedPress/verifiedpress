# Registry Governance
Certainly! Here's the Markdown version of your VerifiedPress registry governance policy, formatted for clarity and inclusion in documentation, websites, or contributor portals:

---

### 📜 VerifiedPress Registry Governance Policy (v1.0.0)

This policy defines how trusted issuers are added, updated, suspended, or revoked in the VerifiedPress trust registry. All actions require quorum-based approval and transparent audit logging.

---

## 🧮 Quorum Requirements

- **Minimum Reviewers:** 3
- **Approval Threshold:** 75% (e.g., at least 3 out of 4 reviewers must approve)

---

## ⚙️ Governance Rules

### ✅ Adding an Issuer

> New issuers must submit a VCIP proposal with:
> - A valid DID (e.g., `did:web:example.com`)
> - Proof of domain ownership
> - Intent to issue credentials (e.g., `VerifiedPublisherCredential`)

Proposals must be reviewed by at least 3 registry stewards and approved by a 75% quorum.

---

### 🔁 Updating Issuer Metadata

> Issuer metadata—such as contact info, logos, or public key rotation—may be updated via a signed request from the issuer’s DID.  
Updates must be reviewed by at least 2 stewards before taking effect.

---

### ⛔ Suspending an Issuer

> Issuers may be temporarily suspended if:
> - Their domain or DID is compromised
> - Their credentials are deemed unverifiable or fraudulent

Suspension requires a majority vote and must be logged. It is reversible.

---

### ❌ Revoking an Issuer

> Issuers may be permanently removed if:
> - They engage in malicious behavior
> - They repeatedly violate credential policies
> - They are subject to legal takedown or cease to operate

Revocation must be unanimous among active registry stewards. A full audit trail will be published.

---

## 🤝 Dispute Resolution

- **Contact Email:** [presspage.entertainment@gmail.com](mailto:presspage.entertainment@gmail.com?subject=governance%30for%20verifiedpress.org)
- **Escalation Policy:**
  - Disputes are reviewed by a neutral group of 5 stewards within 14 days.
  - If no resolution is reached, an independent advisory board may be consulted.
  - Final decisions are logged publicly in the registry governance ledger.

---

_Last updated: 2025-07-07_
