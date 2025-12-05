# LinkedIn Post

## Text

End-to-end encryption protects your messages. It doesn't protect who you're talking to.

Metadata—who communicates with whom, when, and how often—remains visible to network observers even with perfect encryption. This traffic analysis has proven effective for identifying sources, mapping organizations, and inferring sensitive relationships.

We've been working on VEIL, an anonymous communication protocol that provides information-theoretic guarantees for both sender anonymity and receiver privacy.

The approach:
→ DC-nets (Chaum '88) for unconditional sender anonymity
→ STARK-verified mix cascades for unlinkable message routing
→ Threshold PIR across jurisdictions for receiver privacy
→ Post-quantum ready (ML-KEM-1024 + X25519)

The V17 specification is complete. Now seeking cryptographic review and implementation collaborators.

Details: github.com/veil-protocol

#cryptography #privacy #security #anonymity #infosec

---

## Graphic Specification

**Format:** 1200x627px (LinkedIn recommended)
**Style:** Minimal, dark background (#0a0a0a), light text

```
┌────────────────────────────────────────────────────────────────────────┐
│                                                                        │
│                              V E I L                                   │
│                                                                        │
│         Information-Theoretic Anonymous Communication                  │
│                                                                        │
│  ┌─────────┐      ┌─────────┐      ┌─────────┐      ┌─────────┐       │
│  │         │      │         │      │         │      │         │       │
│  │ Sender  │ ───▶ │ DC-Net  │ ───▶ │  Mix    │ ───▶ │  PIR    │ ───▶ │
│  │         │      │         │      │         │      │         │       │
│  └─────────┘      └─────────┘      └─────────┘      └─────────┘       │
│                         │               │               │              │
│                   Info-Theoretic    128-bit ZK    Info-Theoretic      │
│                     Anonymity        Proofs         Privacy           │
│                                                                        │
│  ────────────────────────────────────────────────────────────────────  │
│                                                                        │
│   Content Protected     ✓                                              │
│   Sender Hidden         ✓  (unconditional)                             │
│   Receiver Hidden       ✓  (unconditional)                             │
│   Timing Hidden         ✓                                              │
│   Quantum Resistant     ✓                                              │
│                                                                        │
│                     github.com/veil-protocol                           │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

**Color scheme:**
- Background: #0a0a0a (near black)
- Primary text: #e0e0e0 (light gray)
- Accent: #4a9eff (blue) for arrows and checkmarks
- Secondary: #888888 (mid gray) for labels

**Fonts:**
- Title: Inter or SF Pro Display, 600 weight
- Body: Inter or SF Pro Text, 400 weight
- Monospace elements: JetBrains Mono or SF Mono

---

## Alternative: Simple Quote Graphic

```
┌────────────────────────────────────────────────────────────────────────┐
│                                                                        │
│                                                                        │
│                                                                        │
│        "Encryption protects your messages.                             │
│         It doesn't protect who you're talking to."                     │
│                                                                        │
│                                                                        │
│                              ─────                                     │
│                                                                        │
│                               VEIL                                     │
│              Information-Theoretic Anonymous Communication             │
│                                                                        │
│                       github.com/veil-protocol                         │
│                                                                        │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

---

## SVG Version (Copy to file, open in browser)

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 627">
  <rect width="1200" height="627" fill="#0a0a0a"/>

  <!-- Title -->
  <text x="600" y="80" text-anchor="middle" fill="#e0e0e0" font-family="Inter, system-ui" font-size="48" font-weight="600" letter-spacing="12">VEIL</text>
  <text x="600" y="120" text-anchor="middle" fill="#888888" font-family="Inter, system-ui" font-size="18">Information-Theoretic Anonymous Communication</text>

  <!-- Flow diagram -->
  <rect x="80" y="180" width="120" height="60" rx="4" fill="none" stroke="#4a9eff" stroke-width="2"/>
  <text x="140" y="215" text-anchor="middle" fill="#e0e0e0" font-family="Inter, system-ui" font-size="14">Sender</text>

  <line x1="200" y1="210" x2="280" y2="210" stroke="#4a9eff" stroke-width="2"/>
  <polygon points="280,205 290,210 280,215" fill="#4a9eff"/>

  <rect x="290" y="180" width="120" height="60" rx="4" fill="none" stroke="#4a9eff" stroke-width="2"/>
  <text x="350" y="215" text-anchor="middle" fill="#e0e0e0" font-family="Inter, system-ui" font-size="14">DC-Net</text>

  <line x1="410" y1="210" x2="490" y2="210" stroke="#4a9eff" stroke-width="2"/>
  <polygon points="490,205 500,210 490,215" fill="#4a9eff"/>

  <rect x="500" y="180" width="120" height="60" rx="4" fill="none" stroke="#4a9eff" stroke-width="2"/>
  <text x="560" y="215" text-anchor="middle" fill="#e0e0e0" font-family="Inter, system-ui" font-size="14">Mix Cascade</text>

  <line x1="620" y1="210" x2="700" y2="210" stroke="#4a9eff" stroke-width="2"/>
  <polygon points="700,205 710,210 700,215" fill="#4a9eff"/>

  <rect x="710" y="180" width="120" height="60" rx="4" fill="none" stroke="#4a9eff" stroke-width="2"/>
  <text x="770" y="215" text-anchor="middle" fill="#e0e0e0" font-family="Inter, system-ui" font-size="14">PIR</text>

  <line x1="830" y1="210" x2="910" y2="210" stroke="#4a9eff" stroke-width="2"/>
  <polygon points="910,205 920,210 910,215" fill="#4a9eff"/>

  <rect x="920" y="180" width="120" height="60" rx="4" fill="none" stroke="#4a9eff" stroke-width="2"/>
  <text x="980" y="215" text-anchor="middle" fill="#e0e0e0" font-family="Inter, system-ui" font-size="14">Receiver</text>

  <!-- Labels -->
  <text x="350" y="270" text-anchor="middle" fill="#888888" font-family="Inter, system-ui" font-size="12">IT Anonymity</text>
  <text x="560" y="270" text-anchor="middle" fill="#888888" font-family="Inter, system-ui" font-size="12">ZK Proofs</text>
  <text x="770" y="270" text-anchor="middle" fill="#888888" font-family="Inter, system-ui" font-size="12">IT Privacy</text>

  <!-- Divider -->
  <line x1="100" y1="310" x2="1100" y2="310" stroke="#333333" stroke-width="1"/>

  <!-- Properties -->
  <text x="140" y="360" fill="#4a9eff" font-family="Inter, system-ui" font-size="16">✓</text>
  <text x="170" y="360" fill="#e0e0e0" font-family="Inter, system-ui" font-size="16">Sender Anonymous</text>
  <text x="400" y="360" fill="#888888" font-family="Inter, system-ui" font-size="14">(unconditional)</text>

  <text x="140" y="400" fill="#4a9eff" font-family="Inter, system-ui" font-size="16">✓</text>
  <text x="170" y="400" fill="#e0e0e0" font-family="Inter, system-ui" font-size="16">Receiver Private</text>
  <text x="400" y="400" fill="#888888" font-family="Inter, system-ui" font-size="14">(unconditional)</text>

  <text x="140" y="440" fill="#4a9eff" font-family="Inter, system-ui" font-size="16">✓</text>
  <text x="170" y="440" fill="#e0e0e0" font-family="Inter, system-ui" font-size="16">Messages Unlinkable</text>
  <text x="400" y="440" fill="#888888" font-family="Inter, system-ui" font-size="14">(128-bit)</text>

  <text x="600" y="360" fill="#4a9eff" font-family="Inter, system-ui" font-size="16">✓</text>
  <text x="630" y="360" fill="#e0e0e0" font-family="Inter, system-ui" font-size="16">Traffic Undetectable</text>
  <text x="860" y="360" fill="#888888" font-family="Inter, system-ui" font-size="14">(Tier 3)</text>

  <text x="600" y="400" fill="#4a9eff" font-family="Inter, system-ui" font-size="16">✓</text>
  <text x="630" y="400" fill="#e0e0e0" font-family="Inter, system-ui" font-size="16">Post-Quantum Ready</text>
  <text x="860" y="400" fill="#888888" font-family="Inter, system-ui" font-size="14">(ML-KEM-1024)</text>

  <text x="600" y="440" fill="#4a9eff" font-family="Inter, system-ui" font-size="16">✓</text>
  <text x="630" y="440" fill="#e0e0e0" font-family="Inter, system-ui" font-size="16">Formally Verified</text>
  <text x="860" y="440" fill="#888888" font-family="Inter, system-ui" font-size="14">(5 theorems)</text>

  <!-- Footer -->
  <line x1="100" y1="500" x2="1100" y2="500" stroke="#333333" stroke-width="1"/>
  <text x="600" y="560" text-anchor="middle" fill="#888888" font-family="Inter, system-ui" font-size="20">github.com/veil-protocol</text>

</svg>
```

Save as `veil-linkedin-graphic.svg` and convert to PNG for upload.
