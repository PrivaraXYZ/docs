# Privara

**Confidential Invoice Settlement Protocol**

Extending Fhenix CoFHE with cross-chain confidential payments.

**Testnet: January 20, 2026**

---

## Overview

Privara enables privacy-preserving commercial payments on public blockchains. Using Fully Homomorphic Encryption, invoice amounts and recipient addresses remain encrypted throughout the entire settlement lifecycle — from creation through payment verification to redemption.

By integrating Circle CCTP V2, Privara extends FHE beyond single-chain limitations. Confidential transactions can originate from Ethereum Sepolia while settling privately on Base Sepolia via Fhenix CoFHE. This positions CoFHE as cross-chain privacy infrastructure for the broader EVM ecosystem.

## The Problem

Commercial transactions on public blockchains expose sensitive business data:

- **Invoice amounts** reveal pricing strategies and contract values
- **Payment flows** expose customer relationships and business volumes
- **Transaction patterns** enable competitor analysis and front-running
- **Recipient addresses** can be linked to business identities

Existing privacy solutions either sacrifice composability, require trusted hardware, or demand complex circuit design for each operation.

## Why FHE

Fully Homomorphic Encryption enables arbitrary computation on encrypted data without decryption:

| Approach | Limitation | FHE Advantage |
|----------|------------|---------------|
| Zero-Knowledge Proofs | Predefined circuits required | Flexible logic without redesign |
| Trusted Execution Environments | Hardware trust assumption | Cryptographic security guarantees |
| Partial Homomorphic Encryption | Limited operation types | Full computation support |

## Documentation

- [Lightpaper](./lightpaper.md) — Executive summary and technical overview
- [App Overview](./app/overview.md) — Consumer application and user experience
- [Architecture](./protocol/architecture.md) — Protocol design and components

## Technology

| Layer | Technology |
|-------|------------|
| Confidential Computation | [Fhenix CoFHE](https://www.fhenix.io/) with FHE scheme |
| Token Standard | [ERC-7984](https://eips.ethereum.org/EIPS/eip-7984) Confidential Tokens |
| Cross-Chain | [Circle CCTP V2](https://www.circle.com/en/cross-chain-transfer-protocol) |
| Settlement Asset | USDC |

## Status

| Component | Status |
|-----------|--------|
| Protocol Contracts | Testnet Ready |
| Relayer Network | Testnet Ready |
| Web Application | Testnet Ready |
| iOS Application | Testnet Ready |
| Public Launch | January 20, 2026 |

## Links

- Website: https://privara.xyz/
- Twitter: https://x.com/PrivaraXYZ
- GitHub: https://github.com/PrivaraXYZ

## Post-Launch (January 20, 2026)

- Whitepaper with full technical specification
- Getting Started Guide
- Integration Documentation
- Contract Addresses

---

**Extending CoFHE to cross-chain commerce**
