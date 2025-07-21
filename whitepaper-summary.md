# Afterchain – Protocol Summary (Non-Confidential)

## Overview
Afterchain is a protocol designed for secure, automated post-mortem transfer of digital assets across jurisdictions. It eliminates the need for human executors, centralized custodians, or legal systems by using verifiable cryptographic inputs to trigger on-chain execution.

The protocol is engineered for integration with crypto exchanges, custodial wallets, and Web3 infrastructure.

---

## Key Components

### 🔐 Transfer Vault (TV)
- Smart contract where assets are held reversibly
- Execution only allowed upon verified death event
- Immutable logic ensures tamper-proof conditions

### 🧾 Death Verification Oracle (DVO)
- Queries national/institutional APIs for signed death certificates
- Uses X.509 trust chains, OCSP/CRL checks, and mutual TLS
- Requires **dual-source confirmation** to emit a trigger

### 🧬 zk-SNARK Beneficiary Registry (BRM)
- Privacy-preserving Merkle-based registry of eligible heirs
- Heirs prove eligibility via zk-SNARKs (Groth16)
- Prevents double-claims using nullifier hashes

### ⚙️ Execution Engine
- Listens for valid DVO signals and verified zk-proofs
- Executes irreversible transfer of assets to rightful heir(s)

---

## Workflow Summary

1. **Setup Phase**  
   - User links wallet + registers heirs (or explicit waiver)
   - Vault accepts crypto deposits (ETH, tokens, etc.)

2. **Death Event**  
   - DVO retrieves and verifies signed certificate(s)
   - Once two sources confirm, vault transitions to active

3. **Heir Proof**  
   - Registered heir submits zk-SNARK proof of inclusion
   - Smart contract verifies proof and checks nullifier

4. **Transfer**  
   - Vault executes on-chain distribution to heir wallet(s)
   - All actions logged for audit via ETSI-compliant hash trail

---

## Differentiators

- ✅ No inactivity reliance
- ✅ No human intervention
- ✅ Fully cryptographic & deterministic
- ✅ Zero-knowledge privacy for heirs
- ✅ Patent-protected

---

## Patent
Filed under international application PCT/IB2025/057151.  
Architecture, logic flow, registry model, and oracle interaction are covered.

For commercial licensing or collaboration, visit: [https://afterchain.io](https://afterchain.io)
