# VEIL

VEIL is an anonymous communication protocol providing information-theoretic sender anonymity and receiver privacy against global adversaries. The design composes DC-nets, verifiable mix cascades, and private information retrieval to achieve metadata protection without trusted parties.

## Overview

Existing systems protect message content but leak communication patterns. VEIL addresses this gap by providing provable guarantees:

- **Sender anonymity**: Information-theoretic within DC-net cohorts (n=64), following Chaum's dining cryptographers construction
- **Receiver privacy**: Information-theoretic via Shamir-based PIR with 5-of-7 threshold across independent jurisdictions
- **Unlinkability**: Computational (128-bit) through STARK-verified shuffle with FRI-based proofs
- **Undetectability**: Tier 3 mode achieves information-theoretic undetectability using rejection-sampled steganography per Hopper et al.

The protocol targets 200ms end-to-end latency at scale (10^8 users) through hierarchical DC-net aggregation.

## Technical Approach

```
Sender → DC-Net (IT anonymity) → Mix Cascade (ZK shuffle) → PIR (IT privacy) → Receiver
```

**Cryptographic primitives**:
- ML-KEM-1024 + X25519 hybrid KEM (post-quantum, defense in depth)
- ChaCha20-Poly1305 AEAD
- STARK proofs over Goldilocks field (2^64 - 2^32 + 1)
- BLAKE3 for hashing and key derivation

**Threat model**: Global passive adversary with active capabilities on up to k-1 nodes in each threshold system. We do not defend against endpoint compromise or traffic analysis at the application layer.

## Documentation

[Protocol Specification](https://github.com/veil-protocol/veil-spec/blob/main/V17-PRODUCTION-SPEC.md) — Implementation-ready specification with message formats, state machines, and parameter choices.

[Technical Whitepaper](https://github.com/veil-protocol/veil-spec/blob/main/V17-WHITEPAPER-FULL.md) — Security model, formal reductions, and performance analysis.

[Security Proofs](https://github.com/veil-protocol/veil-spec/blob/main/V15-FORMAL-VERIFICATION-CYCLE.md) — Theorem statements and proof sketches for composition security.

## Project Status

The V17 specification is complete. Implementation has not begun.

Open areas for contribution:
- Formal verification in Coq/Lean
- Constant-time Rust implementation
- Side-channel analysis
- Protocol review and attack finding

## References

D. Chaum, "The Dining Cryptographers Problem: Unconditional Sender and Recipient Untraceability," *Journal of Cryptology*, 1988.

B. Chor, O. Goldreich, E. Kushilevitz, M. Sudan, "Private Information Retrieval," *FOCS*, 1995.

N. Hopper, J. Langford, L. von Ahn, "Provably Secure Steganography," *CRYPTO*, 2002.

E. Ben-Sasson et al., "Scalable, transparent, and post-quantum secure computational integrity," *IACR ePrint*, 2018.

NIST FIPS 203 (ML-KEM), FIPS 204 (ML-DSA), 2024.

## License

MIT
