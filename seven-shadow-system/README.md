# Seven Shadow System — Vault Gate ⛩️

**Status:** Public | [View Repo →](https://github.com/VontaJamal/seven-shadow-system)

Seven Shadow System is a composable policy engine that detects and governs AI-influenced pull request review activity.

---

## What It Does

Detects when AI is doing your code reviews and enforces human oversight. Three decisions: **pass**, **warn**, or **block**.

- **Multi-provider** — GitHub, GitLab, Bitbucket Cloud all supported
- **NPM package** — `npm install @rinshari/sss` (currently RC3)
- **CI workflows** — supply chain checks, release dry runs, RC soak gates
- **Keyless bundle verification** — trust stores with lifecycle controls
- **Agent-readable doctrine** — YAML contracts AI agents consume before writing PRs

## Who It's For

- Maintainers who want explicit governance for AI-assisted review flows
- Teams that need policy-based merge controls across providers
- Security-conscious projects that want trust-chain and supply-chain checks

## Current State

- Public package available as `@rinshari/sss`
- Core guard decisions (`pass`, `warn`, `block`) are production-oriented
- Provider and policy workflows are documented and test-backed

## Roadmap

- Civilian mode (`--civ`) — strips theming for enterprise adoption
- v1.0 stable release
- Provider adapter expansion
- Community policy bundles — share governance configs across orgs
- Trust rollout tooling for downstream adoption

## Feedback

Input is most useful on default policy strictness, downstream adoption workflows, and cross-provider behavior consistency.

[Open an Issue →](https://github.com/VontaJamal/seven-shadow-system/issues)

---

🏴‍☠️ [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.
