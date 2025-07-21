# Afterchain – The Inheritance Layer of Web3

Afterchain is a cryptographic protocol for verifiable, jurisdiction-agnostic post-mortem transfer of digital assets.

Unlike traditional smart contract inheritance models, Afterchain introduces a deterministic execution layer based on certified death events and zero-knowledge privacy — enabling secure, automated transfer without lawyers, custodians, or reliance on inactivity triggers.

---

## 🔒 Core Principles

- **Death Verification Oracle (DVO)**  
  Queries institutional endpoints for digitally signed death certificates (PKI).

- **zk-SNARK Heir Registry**  
  Enables privacy-preserving heir verification without disclosing identity.

- **Smart Contract Execution Engine**  
  Transfers digital assets automatically once verified death + proof is confirmed.

- **No Custody, No Trust Assumptions**  
  Afterchain never holds keys. Execution is cryptographically enforced.

- **Patent Protected**  
  Filed under PCT/IB2025/057151.

---

## 📌 Use Case: Exchanges & Custody Platforms

Afterchain helps platforms unlock new post-mortem monetization layers:

- 2% per-claim execution fee (end user)  
- 80% retained by the platform  
- Zero operational effort  

> Dormant wallets become revenue events — triggered only by certified death.

---

## 🧠 Technical Architecture (High-Level)

Afterchain integrates with national e-registries and institutional sources using:

- TLS-authenticated death certificate validation (X.509, OCSP, CRL)  
- zk-SNARKs (e.g. Groth16) to verify beneficiary eligibility  
- Merkle trees & nullifiers to avoid double-claims  
- Deterministic smart contract logic to execute on-chain  

All of this is designed to operate jurisdiction-neutral and privacy-preserving.

---

## 🚫 Source Code Disclaimer

This repository does **not** contain implementation code.
Instead, it provides architectural background and licensing context.

For integration inquiries or research access, visit:
👉 https://afterchain.io

---

© 2025 KOTIQ OÜ – All rights reserved.
