# Security Policy — VALIPRECISION ($VPX)

## Supported Versions

| Version | Status |
|---|---|
| `v0.0.0` (Genesis) | ✅ Actively supported |

## Reporting a Vulnerability

**CRITICAL: Do NOT open a public GitHub Issue for security vulnerabilities.**

The AXIOLEDGER ecosystem handles financial infrastructure and cryptographic systems. Public disclosure before a patch is deployed could put user funds and network integrity at risk.

### Responsible Disclosure Process

1. **Contact:** Send a private report to the maintainer via GitHub private security advisory:
   `https://github.com/valiprecision/.github/security/advisories/new`

2. **Include in your report:**
   - Affected component and version
   - Step-by-step reproduction instructions
   - Estimated severity (Critical / High / Medium / Low)
   - Suggested fix (if available)

3. **Response timeline:**
   - **Acknowledgement:** Within 48 hours
   - **Initial assessment:** Within 7 days
   - **Patch & disclosure:** Within 90 days (Critical: 30 days)

### What NOT to do

- Do not publicly disclose the vulnerability before a fix is released
- Do not test exploits on mainnet or testnet environments
- Do not access, modify, or exfiltrate data beyond what is needed to demonstrate the vulnerability

## Bug Bounty

Critical vulnerabilities that could compromise:
- The ZK-OBFT consensus mechanism (`$VPX`)
- Private key extraction from AXIO Vault
- Double-spending or fund theft on any Pillar
- ZK-DID nullifier collision enabling identity duplication

...are eligible for rewards from the **Treasury DAO Bug Bounty Fund**.

Reward levels are determined by the Security & FIM Auditor council based on CVSS score and potential impact.

## Security Architecture

VALIPRECISION is part of the AXIOLEDGER ecosystem which implements:

- **ZK-SNARKs** consensus proofs (284-byte π, O(1) verification)
- **Instant Slashing** — 100% stake burn on double-signing, same block
- **Post-Quantum Signatures** — CRYSTALS-Dilithium (NIST Level 5)
- **Supply Chain Scanner** — 24/7 npm/DApp auditing at Protocol level
- **ZK-DID** — anonymous KYC with Regulator Gateway (5/7 multisig)
- **TLS 1.3** on all API endpoints — cert rotation every 24h

## Contact

- **Security Email:** via GitHub private advisory (preferred)
- **Maintainer:** `315885655+davictran76@users.noreply.github.com`
- **PGP:** Available on request

---

*VALIPRECISION — AXIOLEDGER Ecosystem · Genesis v0.0.0*
*Node: `axioledger-devnode` · `192.168.0.47`*
