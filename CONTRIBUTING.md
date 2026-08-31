# Contributing to VALIPRECISION

Thank you for your interest in contributing to **VALIPRECISION ($VPX)** — part of the [AXIOLEDGER](https://github.com/axioledger) ecosystem.

> **Immutable Principle (Article VI):** All core source code of AXIOLEDGER — including consensus engine, ZK circuits, and core smart contracts — shall always be public and auditable. There are no "black boxes" in public financial infrastructure.

## Getting Started

### Prerequisites

- **Rust 1.78+** (for consensus / node components)
- **Node.js v20+** (for SDK / API components)
- **Git** with GPG signing configured

### Fork & Clone

```bash
# Fork via GitHub UI, then:
git clone https://github.com/<your-username>/<repo>.git
cd <repo>
git remote add upstream https://github.com/valiprecision/<repo>.git
```

### Branch Naming

Always branch from `dev`:

```bash
git checkout dev
git pull upstream dev
git checkout -b feat/your-feature-name
```

| Prefix | Use |
|---|---|
| `feat/` | New feature |
| `fix/` | Bug fix |
| `docs/` | Documentation |
| `security/` | Security patch |
| `chore/` | Build/tooling |

## Development Standards

### Rust Components

```bash
cargo build --release
cargo test --all
cargo clippy -- -D warnings
cargo fmt --check
```

### TypeScript / Node.js Components

```bash
npm install
npm test
npx eslint . --ext .ts,.tsx
npx tsc --noEmit
```

## Commit Convention

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat(vpx): add epoch rotation logic for ZK-OBFT
fix(sqx): resolve AF_XDP buffer overflow on high load
docs(api): update endpoint schema for /vp/validators/reputation
security(vrq): patch nullifier collision in ZK-DID circuit
```

## Pull Request Process

1. Ensure all tests pass: `cargo test --all` / `npm test`
2. Run linter: `cargo clippy -- -D warnings` / `eslint`
3. Update documentation if behavior changes
4. Reference related issues in the PR description
5. Await review from **≥ 2 core maintainers** before merge
6. PRs to `main`/`ledger` branches require **≥ 1 Security & FIM Auditor** approval for any cryptographic or consensus changes

## Security Contributions

For security vulnerabilities, **do NOT open a public issue**. Follow the [Security Policy](SECURITY.md) for responsible disclosure.

## Design System

All UI contributions **must** use:
- Icons from `asset/icon/` — no external icon sources
- Design tokens from `design-system/tokens/` — no hardcoded color values
- See [`design-system/README.md`](https://github.com/axioledger/design-system) for full guidelines

## Code of Conduct

By contributing, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).

---

*VALIPRECISION — AXIOLEDGER Ecosystem · Genesis v0.0.0*
