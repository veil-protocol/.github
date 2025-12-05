
<div align="center">

# VEIL Protocol

### Privacy You Can Prove

**The first communication protocol with mathematically proven anonymity guarantees**

---

[Specification](https://github.com/veil-protocol/veil-spec) ·
[Whitepaper](https://github.com/veil-protocol/veil-spec/blob/main/V17-WHITEPAPER-FULL.md) ·
[Technical Reference](https://github.com/veil-protocol/veil-spec/blob/main/V17-TECHNICAL-REFERENCE.md)

---

</div>

## The Problem

Every "private" messaging app leaks **metadata** — who you talk to, when, how often. This metadata is often more valuable than message content for surveillance.

| App | Content Protected | Metadata Protected |
|:---:|:-----------------:|:------------------:|
| Signal | Yes | No |
| WhatsApp | Yes | No |
| Telegram | Partial | No |
| **VEIL** | **Yes** | **Yes** |

## The Solution

VEIL provides **information-theoretic** security guarantees — meaning security is mathematically proven, not just computationally hard to break.

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   Sender  ──▶  DC-Net  ──▶  Mix Cascade  ──▶  PIR  ──▶  Receiver│
│                  │              │              │                │
│            Info-Theoretic   128-bit ZK   Info-Theoretic        │
│             Anonymity        Proofs        Privacy             │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

## Key Properties

| Property | Guarantee | Type |
|----------|-----------|------|
| Sender Anonymity | Hidden in 64-user group | Information-Theoretic |
| Receiver Privacy | Hidden via threshold PIR | Information-Theoretic |
| Unlinkability | Cannot correlate messages | 128-bit Computational |
| Undetectability | Indistinguishable from normal traffic | Information-Theoretic (Tier 3) |
| Quantum Resistance | ML-KEM-1024 + X25519 hybrid | Post-Quantum Ready |

## By The Numbers

<div align="center">

| 200ms | 100M | 5 | 50+ | 0% |
|:-----:|:----:|:-:|:---:|:--:|
| Latency | Users Supported | Security Theorems | Attack Vectors Analyzed | Detection Rate (Tier 3) |

</div>

## Repositories

| Repository | Description | Status |
|------------|-------------|--------|
| [veil-spec](https://github.com/veil-protocol/veil-spec) | Protocol specification & whitepapers | V17 Complete |
| veil-core | Rust implementation | Coming Soon |
| veil-client | Desktop & mobile clients | Planned |
| veil-node | Network infrastructure | Planned |

## Status

- [x] Protocol Design (V17)
- [x] Formal Security Proofs
- [x] Adversarial Analysis (50+ attack vectors)
- [x] Complete Specification
- [x] Academic Whitepaper
- [ ] Reference Implementation
- [ ] Security Audit
- [ ] Testnet Launch

## Contributing

We welcome contributions from cryptographers, security researchers, and developers.

See our [Contributing Guidelines](https://github.com/veil-protocol/veil-spec/blob/main/CONTRIBUTING.md).

---

<div align="center">

**VEIL: When privacy is a proof, not a promise.**

</div>
