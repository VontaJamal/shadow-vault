# The Armory — Vault Gate ⛩️

**Status:** Public | [View Repo →](https://github.com/VontaJamal/armory)

A Final Fantasy-themed collection of standalone developer tools. 36 scripts across 4 shops — battle-tested on real infrastructure, not portfolio demos.

---

## What's In Stock

### ⚔️ Weapons — CLI tools you wield directly

| Weapon | What It Does |
|--------|-------------|
| **Masamune** | API key hot-swap with encrypted vault. Named key profiles, instant rotation. |
| **Jutsu** | Key management across machines — add, list, remove, swap API keys with SSH-aware gateway restart. |
| **Phoenix Down** | Full system backup — encrypted, timestamped, one-command restore. |
| **Aegis** | Service health monitoring — checks running services, alerts on failures. |
| **Sentinel** | Continuous watchdog — monitors processes, auto-restarts on crash. |
| **Scan** | Security audit — checks for exposed secrets, open ports, vulnerable configs. |
| **Truesight** | Deep system scan — full environment analysis beyond surface-level checks. |
| **Warp** | Instant multi-machine file deployment — SCP-based, config-driven sync. |

### 📜 Spells — Cron-powered automation (set and forget)

| Spell | What It Does |
|-------|-------------|
| **Libra** | Daily intel briefing — system status, alerts, calendar, weather. Morning report. |
| **Cure** | Backup verification — automatically confirms your backups are valid and restorable. |
| **Protect** | Scheduled security audits — runs Scan on a timer, alerts on new findings. |
| **Regen** | Morning system refresh — clears caches, rotates logs, preps the environment. |
| **Chronicle** | Cross-repo git intelligence — commit history, branch status, PR tracking across all projects. |

### 🐉 Summons — Heavy operations (the big guns)

| Summon | What It Does |
|--------|-------------|
| **Ramuh** | System diagnostic — full hardware + software health report with benchmarks. |
| **Shiva** | System state snapshots — capture current state, diff against previous snapshots to catch drift. |
| **Odin** | System cleanup — finds and removes temp files, stale logs, orphaned processes. |
| **Bahamut** | Full empire deployment — orchestrates multi-service rollouts across machines. |
| **Ifrit** | Agent spawner — spin up autonomous agent instances with config and monitoring. |
| **Alexander** | Release gate — read-only preflight checks before any deployment goes live. |

### 🎒 Items — Guides and playbooks

| Item | What It Covers |
|------|---------------|
| **Teleport** | Multi-machine SSH setup — key generation, config, tunneling, file transfer. |
| **Cron Scheduling** | Cron job setup and management — templates, monitoring, common patterns. |
| **Telegram Setup** | Bot creation, channel config, alert routing — full Telegram integration. |
| **NSSM Services** | Windows service management — register scripts as services that survive reboots. |
| **Agent Comms** | Inter-agent messaging setup — session keys, routing, cross-agent coordination. |
| **Remedy** | One-command environment health check — catches common issues before they break things. |

---

## [The Forge 🔥](FORGE.md)

Where new tools are shaped before they ship. Concepts extracted from real development activity, sitting in the open for community input before they hit the Armory. [Check what's brewing →](FORGE.md)

---

## Where It's Going

- Civilian mode (`--civ`) — strips FF theming for people who just want the tools
- More summons as production needs grow
- CI pipeline with automated testing on every PR
- Cross-platform parity (PowerShell-first, bash/zsh ports expanding)

## Open Questions

Things I'm weighing — if you have thoughts, [open an Issue](https://github.com/VontaJamal/armory/issues):

- Should spells ship with pre-built cron templates or stay config-your-own?
- How important is Mac/Linux parity vs Windows-first?
- Better tool discovery beyond browsing folders?

---

*Part of [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.*
