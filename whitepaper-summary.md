# Afterchain — Protocol Summary (Non-Confidential)

## Overview

Afterchain is a proprietary cryptographic execution protocol designed to enable deterministic, automated post-mortem transfer of digital assets across jurisdictions.

The protocol replaces human executors, custodial fallback mechanisms, and legal inactivity triggers with verifiable cryptographic inputs that autonomously initiate irreversible on-chain execution.

Afterchain is engineered as an infrastructure layer for crypto exchanges, custodial wallets, and Web3 platforms.

---

## Architectural Components

### Transfer Vault (TV)

A smart-contract-based container governing asset custody and execution.

- Assets are held in a reversible pre-death state  
- Execution logic is immutably defined  
- Transfers are enabled only after verified death confirmation  
- No discretionary or manual override exists  

---

### Death Verification Oracle (DVO)

A cryptographic oracle responsible for confirming death events.

- Queries institutional or national registries  
- Validates digitally signed death certificates  
- Enforces PKI trust chains (X.509), OCSP/CRL checks, and mutual TLS  
- Requires dual-source confirmation before emitting a trigger  

The oracle supports jurisdiction-aware fallback logic while remaining jurisdiction-neutral by design.

---

### Zero-Knowledge Beneficiary Registry (BRM)

A privacy-preserving registry for heir eligibility.

- Beneficiaries are registered via Merkle commitments  
- Eligibility is proven using zk-SNARKs (e.g. Groth16)  
- Nullifier hashes prevent double-claims  
- No beneficiary identities are disclosed on-chain  

---

### Execution Engine

The execution layer coordinating final settlement.

- Listens for valid oracle triggers  
- Verifies zero-knowledge beneficiary proofs  
- Executes irreversible on-chain asset transfers  
- Enforces one-time execution guarantees  

All execution events are cryptographically logged for auditability.

---

## High-Level Operational Flow

1. **Configuration Phase**  
   Wallet is linked, beneficiaries registered or explicitly waived, assets deposited.

2. **Death Event Verification**  
   Oracle retrieves and validates certified death data from institutional sources.

3. **Claim Phase**  
   Eligible beneficiary submits a zero-knowledge proof of inclusion.

4. **Execution**  
   Vault performs deterministic and irreversible asset distribution.

---

## Key Properties

- No inactivity reliance  
- No human executors  
- No custody of keys or assets  
- Cryptographic finality  
- Zero-knowledge privacy  
- Deterministic execution  
- Patent-protected architecture  

---

## Legal & Commercial Positioning

Afterchain does not constitute a legal testament or custodial service.

It is a cryptographic execution protocol licensed to infrastructure providers under commercial terms.

---

## Patent Protection

Protected under international patent application  
**PCT/IB2025/057151**, covering oracle design, registry model, and execution logic.

---

For licensing, integration, or institutional collaboration:
👉 https://afterchain.io
