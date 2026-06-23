# Agentic Research

Tools for working with code and agents. Mostly experimental — take what's useful.

## Code intelligence

**[mache](https://github.com/agentic-research/mache)** — Treats source code as a graph instead of text. Tree-sitter parsing, community detection, caller/callee tracing, impact analysis. Mounts as a filesystem (`cd`, `ls`, `cat`) or serves MCP with 15+ tools.

**[ley-line-open](https://github.com/agentic-research/ley-line-open)** — Open-source data plane primitives. Arena-backed SQLite graph (zero-copy), tree-sitter AST projection with bidirectional splice, LSP client. Powers mache's enriched tools (LSP type info, semantic search) and ships a C FFI for embedding.

## Identity

**[signet](https://github.com/agentic-research/signet)** — Proof-of-possession identity that replaces bearer tokens with cryptographic proof. Ephemeral X.509 certs (5-min TTL), Ed25519 + ML-DSA-44 (post-quantum ready), OS keyring. Signs git commits, authenticates HTTP, bridges GHA OIDC to short-lived certs — all offline-capable.

**[notme](https://github.com/agentic-research/notme)** — Self-sovereign identity for agents. Cap'n Proto schemas, Cloudflare Worker authority, ley-line-sign WASM. Demo at [notme.bot](https://notme.bot).

## Agents & runtime

**[rosary](https://github.com/agentic-research/rosary)** — Cross-repo work orchestrator. Tracks atoms of work as "beads" (Dolt-backed SQL in each repo), dispatches Claude/Gemini agents in isolated worktrees, syncs to Linear for human review.

**[x-ray](https://github.com/agentic-research/x-ray)** — Voice-driven browser agent. Topology-based web navigation — projects pages into a deterministic VFS instead of guessing CSS selectors.

**[cloister](https://github.com/agentic-research/cloister)** — Workerd-based hypervisor with a declarative Cap'n Proto manifest. Substrate-level identity, audit, and per-bundle credential scoping; today it hosts MCP servers behind one HTTP face.

## Libraries & tooling

| Repo | What |
|------|------|
| [go-cms](https://github.com/agentic-research/go-cms) | CMS/PKCS#7 for Go with Ed25519. |
| [go-platform-signers](https://github.com/agentic-research/go-platform-signers) | `crypto.Signer` — macOS Keychain, Linux PKCS#11. |
