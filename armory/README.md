# The Armory — Vault Gate ⛩️

**Status:** Public | [View Repo →](https://github.com/VontaJamal/armory)

A Final Fantasy-themed collection of standalone developer tools. Battle-tested scripts for backup, security, monitoring, deployment, and key management — built for real infrastructure, not portfolio filler.

---

## Where We Are

The Armory has 4 shops stocked:

- **Weapons** — CLI tools you wield directly (key swap, backup, health checks, security audit)
- **Spells** — Cron-powered automation (daily intel, backup verification, auto-audits, morning briefings)
- **Items** — Guides and setup playbooks (multi-machine SSH, cron scheduling, Telegram alerts, service management)
- **Summons** — Heavy scripts for big operations (full deployment, agent spawning, system cleanup, diagnostics, state snapshots)

Everything works standalone — no framework dependencies, no vendor lock-in.

## Where It's Going

- **Warp** — instant multi-machine file deployment (scp-based, config-driven)
- **Armory Init ("Awakening")** — one command to scaffold a new tool with README, tests, and CI wiring
- **More summons** — system tools keep expanding based on what we actually need in production
- **CI pipeline** — automated testing on every PR (Chronicle integration)

## Open Questions

Things I'm genuinely weighing — if you have thoughts, open an Issue:

- **Should spells ship with pre-built cron templates or stay config-your-own?** Right now they're templates. Could ship as one-command installs.
- **Cross-platform priority** — everything's PowerShell-first (Windows). Some tools have bash/zsh ports. How important is Mac/Linux parity?
- **Tool discovery** — the FF naming is fun but can make it hard to find what you need. Better search/index system?

## What's Been Interesting

- The 3-column naming format (FF Name | Flavor Text | Plain Description) was controversial internally. We kept it because it serves both audiences — FF fans get the vibe, everyone else gets the description.
- Every tool in here runs in production on real infrastructure. Nothing ships without being tested on live systems first.
- The summons category keeps growing because system-level operations are where scripts save the most time.

---

*Part of [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.*
