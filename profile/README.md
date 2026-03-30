# Agentic Research

Tools and infrastructure for human-AI collaborative research.

## Projects

### Core

**[mache](https://github.com/agentic-research/mache)** — Structural code intelligence engine. Mache treats source code as a graph, not text — mounting it as a navigable filesystem backed by SQL. Tree-sitter parsing, community detection, caller/callee tracing, impact analysis. Ships as an MCP server with 15+ tools or a FUSE mount for `cd`/`ls`/`cat` traversal. Used by agents to understand codebases the way a staff engineer would: by structure, not by grep.

**[signet](https://github.com/agentic-research/signet)** — Proof-of-possession identity that replaces bearer tokens with cryptographic proof. Ephemeral X.509 certificates (5-minute TTL), Ed25519 + ML-DSA-44 (post-quantum ready), OS keyring storage. Signs git commits, authenticates HTTP requests, and bridges GHA OIDC tokens to short-lived certs — all offline-capable, no network required for key operations.

| Repo | What |
|------|------|
| [kiln](https://github.com/agentic-research/kiln) | Single binary packaging for mache + leyline. Homebrew, distroless OCI images. |
| [x-ray](https://github.com/agentic-research/x-ray) | Voice-driven browser agent — topology-based web navigation for agents. |

### Supply Chain

| Repo | What |
|------|------|
| [venturi](https://github.com/agentic-research/venturi) | High-velocity vulnerability ingestion from NVD, GHSA, Wolfi. |
| [smelt](https://github.com/agentic-research/smelt) | Vulnerability DB comparison and validation. |

### Libraries

| Repo | What |
|------|------|
| [go-cms](https://github.com/agentic-research/go-cms) | CMS/PKCS#7 for Go with Ed25519 support. |
| [go-platform-signers](https://github.com/agentic-research/go-platform-signers) | Platform-native `crypto.Signer` — macOS Keychain, Linux PKCS#11. |

### Identity

[notme.bot](https://notme.bot) — identity platform. Passkey auth, Ed25519 CA, epoch-based cert rotation.
