# Seven Shadow System — Vault Gate ⛩️

**Status:** Public | [View Repo →](https://github.com/VontaJamal/seven-shadow-system)

A composable policy engine for AI-influenced pull request review detection and blocking. The governance layer that guards every Sovereign repo.

---

## What It Does

Detects when AI is doing your code reviews and enforces human oversight. Three decisions: **pass**, **warn**, or **block**.

- **Multi-provider** — GitHub, GitLab, Bitbucket Cloud all supported
- **NPM package** — `npm install @rinshari/sss` (currently RC3)
- **121 files** — conformance test suite, trust stores, policy governance, fuzzing profiles
- **CI workflows** — supply chain checks, release dry runs, RC soak gates
- **Keyless bundle verification** — trust stores with lifecycle controls
- **Agent-readable doctrine** — YAML contracts AI agents consume before writing PRs

## Where It's Going

- Civilian mode (`--civ`) — strips theming for enterprise adoption
- v1.0 stable release
- Provider adapter expansion
- Community policy bundles — share governance configs across orgs
- Trust rollout tooling for downstream adoption

## Open Questions

- How strict should default policies be out of the box? Permissive (warn-first) or strict (block by default)?
- Should the conformance suite be extractable as a standalone testing tool?
- Enterprise vs open-source policy defaults — same or separate tracks?

[Open an Issue →](https://github.com/VontaJamal/seven-shadow-system/issues)

---

🏴‍☠️ [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.
