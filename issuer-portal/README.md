# 🛠️ VerifiedPress Issuer Portal

The Issuer Portal is the reference implementation for issuing Verifiable Credentials using the VerifiedPress trust framework.  
It supports signing and managing publisher credentials anchored to decentralized identifiers (DIDs) and the `VerifiedPublisherCredential` schema.

---

## 🎯 Features

- 🔐 DID-based credential issuance (DID:Web or DID:Key)
- 🧾 Supports `ld+json` (Ed25519Signature2020) and JWT VCs
- 🧩 Modular Veramo agent for signing, revocation, and registry integration
- 📤 CLI tool for issuing publisher credentials
- 🧑‍💻 Future UI: Web frontend for issuer onboarding and credential request flow

---

## 🧱 Structure
```sh
issuer-portal/ 
├── veramo-agent/           # Core VC engine and DID signer 
│   ├── src/ 
│   └── scripts/            # CLI tools for issuing credentials 
│   └── test/
├── public-ui/              # (Optional) React/Vue/HTML(js/w3.css) portal frontend (WIP) 
└── README.md
```

---

## 🚀 Usage (CLI)

1. Install dependencies:
   ```bash
   cd veramo-agent
   npm install
