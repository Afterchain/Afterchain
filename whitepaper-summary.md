# Afterchain — Protocol Summary (Non-Confidential)

## Overview

Afterchain is a proprietary cryptographic execution protocol for
deterministic, automated post-mortem transfer of digital assets across
jurisdictions.

The protocol replaces human executors, custodial fallback mechanisms,
and legal inactivity triggers with verifiable cryptographic inputs that
autonomously initiate irreversible on-chain execution.

Afterchain is engineered as an infrastructure layer for crypto exchanges,
custodial wallets, and Web3 platforms.

---

## Architectural Components

### Transfer Vault (TV)

A smart-contract state machine governing execution rights.

- Non-custodial by design — no contract ever holds assets as collateral,
  bond, or escrow
- Transitions deterministically through `ACTIVE → ATTESTED → CLAIMABLE
  → EXECUTED`
- Execution is enabled only after cryptographic attestation of a death
  event
- A mathematical challenge-window cap (MAX_CHALLENGES = 3) prevents
  infinite delay without economic bonds or custodial risk
- No discretionary or manual override exists

### Death Verification Oracle (DVO)

A multi-signature cryptographic oracle responsible for confirming death
events.

- Validates certified death events via institutional PKI trust chains
- Enforces a 3-of-5 signing threshold — no single oracle key can
  produce a valid attestation
- All oracle roster mutations are gated by a 24-hour on-chain timelock
- Jurisdiction-aware while remaining jurisdiction-neutral by design

### Zero-Knowledge Beneficiary Registry (BRM)

A privacy-preserving registry for heir eligibility.

- Beneficiaries are registered via Merkle commitments
- Eligibility is proven using Groth16 zk-SNARKs
- Nullifier hashes prevent double-claims
- No beneficiary identities are disclosed on-chain

### Execution Engine

The execution layer coordinating final settlement.

- Verifies zero-knowledge beneficiary proofs on-chain
- Validates EIP-712 fee-terms payload signed by the oracle multisig
- Executes irreversible on-chain asset transfers
- Enforces one-time execution via spent-nullifier registry
- Cross-chain replay protected at three independent enforcement layers

All execution events are cryptographically logged on-chain for
auditability.

---

## High-Level Operational Flow

1. **Configuration Phase**
   Vault is configured, beneficiaries registered via Merkle commitments,
   execution parameters defined.

2. **Death Event Verification**
   Oracle multisig validates certified death data and emits a signed
   attestation.

3. **Claim Phase**
   Eligible beneficiary submits a Groth16 zero-knowledge proof of
   inclusion.

4. **Execution**
   Vault performs deterministic and irreversible asset distribution
   after validating the proof, the oracle attestation, and the
   fee-terms payload.

---

## Key Properties

- Non-custodial — no contract holds assets as collateral or bond
- No inactivity reliance
- No human executors
- Cryptographic finality
- Zero-knowledge privacy
- Deterministic and irreversible execution
- 3-of-5 multi-signature oracle with on-chain governance timelock
- Patent-protected architecture

---

## Legal & Commercial Positioning

Afterchain does not constitute a legal testament or custodial service.
It is a cryptographic execution protocol licensed to infrastructure
providers under commercial terms.

---

## Patent Protection

Protected under international patent application **PCT/IB2025/057151**,
covering oracle design, registry model, and execution logic.

---

## Public Audit Surface

The on-chain execution rail is publicly available for independent
security review:

**[github.com/Afterchain/afterchain-protocol-public](https://github.com/Afterchain/afterchain-protocol-public)**

The public shell contains 20 Solidity contract source files, 174
Foundry regression tests, and a public security model document.
The off-chain orchestration layer is closed-core and not included.
