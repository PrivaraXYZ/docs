# ReineiraOS Architecture

**Programmable Infrastructure for Stablecoins**

---

## Overview

ReineiraOS combines three core components into a unified protocol stack:

- **Confidential Stablecoin** — FHE-encrypted wrapper around USDC/USDT via Fhenix
- **Escrow Engine** — Conditional holding and release as a protocol primitive
- **Cross-chain Deposits** — Multi-chain deposit routing to Arbitrum

---

## Confidential Stablecoin

Users deposit standard stablecoins (USDC, USDT) and receive Reineira tokens. Balances and transaction amounts are encrypted using Fully Homomorphic Encryption via Fhenix — computations execute on encrypted data without exposing values.

| Property | Detail |
|----------|--------|
| Backing | 1:1 with deposited stablecoins |
| Unwrap | To USDC/USDT at any time |
| Privacy | Balances and amounts encrypted by default |
| Compliance | AML screening on deposits |

### Privacy Guarantees

| Data | Standard Stablecoins | ReineiraOS |
|------|---------------------|------------|
| Balances | Visible to all | Encrypted |
| Transfer amounts | Visible to all | Encrypted |
| Transaction graph | Fully analyzable | Protected |

---

## Escrow Engine

Every payment can be held, conditioned, or reversed. Escrow operates as a protocol primitive that other components build on.

### Modes

| Mode | Mechanism |
|------|-----------|
| Standard | Deposit → Hold → Release |
| Conditional | Rule-based or oracle-triggered release |
| Asset DVP | Atomic delivery-vs-payment for ERC-721 |

### Condition Types

- **Time-based** — Release after a specific date or duration
- **Signature-based** — Release on multi-party approval
- **Oracle-based** — Release on external data feed

---

## Cross-chain Deposits

Users can fund their accounts from multiple chains. Deposits are automatically routed to the Reineira stablecoin on Arbitrum — no manual bridging required.

### Flow

1. User initiates deposit from any supported chain
2. Funds are routed cross-chain to Arbitrum
3. Stablecoins are wrapped into confidential Reineira tokens
4. Balance available in user's account

---

## Technology Stack

| Layer | Technology |
|-------|------------|
| Settlement | Arbitrum (Ethereum L2) |
| Privacy | Fhenix FHE Coprocessor |
| Cross-chain | Multi-chain deposit routing |
| Smart Contracts | Solidity + FHE extensions |

---

## Security Model

### Cryptographic Foundation

- **FHE Security** — Based on Learning With Errors (LWE) hardness assumption
- **No Hardware Trust** — Cryptographic guarantees, no TEE dependency

### Trust Assumptions

| Component | Assumption |
|-----------|------------|
| Fhenix FHE | Correct FHE computation and key management |
| Arbitrum | Network consensus integrity |
| Cross-chain routing | Bridge operator integrity |

---

*For the consumer application, see [Privara](../app/overview.md). For the full protocol overview, see the [Litepaper](../lightpaper.md).*
