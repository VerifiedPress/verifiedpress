# VCIP-0001: Publisher Credential Schema

## 📅 Date Proposed

2025-07-07

## 🧑‍💻 Author(s)

- Patrick Ingle (@patrickingle)

---

## 🧭 Summary

Defines a Verifiable Credential schema for identifying and verifying digital publishers within the VerifiedPress trust framework.

---

## 🎯 Motivation

To establish a standardized, interoperable credential that allows verifiers to confirm the legitimacy of a publisher, including metadata such as domain ownership, editorial policy, and DID linkage.

---

## 🔍 Specification

- Credential Type: `VerifiedPublisherCredential`
- Required Fields:
  - `id` (DID)
  - `domain`
  - `legalName`
  - `editorialPolicyURL`
  - `issuedBy`
  - `issuanceDate`
- Optional Fields:
  - `logo`
  - `jurisdiction`
  - `revocationMethod`

---

## 🔁 Compatibility / Migration

No breaking changes. This is a foundational schema.

---

## ✅ Acceptance Criteria

- Schema published in `trust-framework/schemas/`
- JSON-LD context defined and resolvable
- At least one test issuance via Veramo agent

---

## 💬 Discussion Points

- Should we include proof-of-domain via DNS or DID verification?
- Should editorial policy be a required field?

---

## 📜 License

This VCIP is available under the [Creative Commons CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.