# Security Policy

## Reporting Vulnerabilities

VEIL takes security seriously. If you discover a security vulnerability, please follow responsible disclosure:

### Do NOT

- Open a public GitHub issue
- Discuss the vulnerability publicly before it's fixed
- Exploit the vulnerability beyond what's necessary to demonstrate it

### Do

1. **Email**: Send details to [security contact to be added]
2. **Encrypt**: Use our PGP key if available
3. **Include**:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact assessment
   - Suggested fix (if any)

### Response Timeline

| Stage | Timeframe |
|-------|-----------|
| Initial acknowledgment | 24-48 hours |
| Preliminary assessment | 1 week |
| Fix development | Depends on severity |
| Public disclosure | After fix is deployed |

### Scope

In scope:
- Protocol specification flaws
- Cryptographic weaknesses
- Privacy leakage vectors
- Implementation vulnerabilities (when code is released)

Out of scope:
- Social engineering
- Physical attacks
- Attacks requiring user misconfiguration

## Security Design

VEIL is designed with defense in depth:

- **Information-theoretic** guarantees where possible
- **Post-quantum** cryptography (ML-KEM-1024)
- **Formally verified** security properties
- **Adversarial analysis** from nation-state threat models

See [V17-FINAL-COMPREHENSIVE-REVIEW.md](https://github.com/veil-protocol/veil-spec/blob/main/V17-FINAL-COMPREHENSIVE-REVIEW.md) for our threat model.
