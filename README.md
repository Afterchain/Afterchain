# Afterchain — The Inheritance Layer of Web3

Afterchain is a deterministic, non-custodial, privacy-preserving protocol
for post-mortem digital asset execution. A `TransferVault` transitions
through a strict on-chain state machine — `ACTIVE → ATTESTED → CLAIMABLE
→ EXECUTED` — gated by cryptographic attestations, zero-knowledge proofs,
and a multi-signature oracle layer. No custodians. No inactivity
assumptions. No human executors.

---

## Project Status

| Field | Value |
|---|---|
| Status | Active development |
| Distribution model | Closed-core, licensing-only |
| Patent | PCT/IB2025/057151 |
| Public shell | [afterchain-protocol-public](https://github.com/Afterchain/afterchain-protocol-public) |

---

## Public Audit Surface

The on-chain execution rail is publicly available for security review:

**[github.com/Afterchain/afterchain-protocol-public](https://github.com/Afterchain/afterchain-protocol-public)**

The public shell contains:
- 20 Solidity contract source files
- 174 Foundry regression tests (all passing)
- Public security model documentation
- Groth16 ZK verifier artifacts
- Business Source License 1.1 (Change Date: 2035-01-01)

The off-chain orchestration layer (oracle attestation, evidence package
assembly, deployment infrastructure) is closed-core and not included.

---

## What Afterchain Is

- A cryptographic execution layer for post-mortem digital asset transfer
- Designed for exchanges, custodians, and Web3 infrastructure
- Zero-custody by design — no contract ever holds funds as collateral or bond
- Deterministic and irreversible — mathematical liveness guarantee, not economic
- Privacy-preserving through Groth16 zero-knowledge proofs
- Multi-signature oracle layer with 3-of-5 threshold and 24h on-chain timelock
- Cross-chain replay protected at three independent enforcement layers

## What Afterchain Is Not

- Not a consumer wallet or application
- Not a legal testament
- Not a custodial or trust-based service
- Not dependent on inactivity timers or human judgment

---

## Intellectual Property

The Afterchain protocol is protected under international patent application
**PCT/IB2025/057151**.

The public shell is distributed under the Business Source License 1.1.
Non-commercial review, academic research, and security audits are permitted
without a separate agreement. Production use requires a commercial license.

---

## Contact

For licensing, integration, or institutional due diligence inquiries:

👉 https://afterchain.io

---

© 2026 KOTIQ OÜ — All rights reserved.
