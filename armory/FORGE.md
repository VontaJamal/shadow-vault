# The Forge 🔥

**Where Armory tools are born.**

These are concepts — weapons, spells, summons, and items being shaped before they hit the Armory. Some will ship. Some won't survive the forge. If you have thoughts on any of these, [open an Issue](https://github.com/VontaJamal/armory/issues).

---

## Current Inventory Balance

| Shop | Count | Target Range |
|------|-------|-------------|
| ⚔️ Weapons | 8 | 8–15 |
| 📜 Spells | 5 | 8–12 |
| 🐉 Summons | 6 | 6–10 |
| 🎒 Items | 6 | 8–12 |

**Priority fill:** Spells and Items are light. Next builds should lean there unless a weapon/summon concept is too good to wait.

---

## Concepts in the Forge

*Updated nightly from development activity.*

### Under Consideration

**⚔️ Weapon — Mega Phoenix**
*"What Phoenix Down does for one... Mega Phoenix does for everything."*

Full GitHub account backup to local/external drive. Mirror-clones every repo (public + private) with all branches, tags, and full history. Timestamped backup folders, summary report with file counts and sizes, failed repo detection. One command, entire codebase sovereignty — GitHub goes down, you don't.

**Why it surfaced:** Built `github-backup.ps1` during a session where the realization hit: GitHub is someone else's server. 23 repos, 220 MB, backed up to X: drive in under 60 seconds. Phoenix Down handles single-system backup — Mega Phoenix handles your entire code empire.

**Shop:** Weapons (Phoenix Down's big brother)
**Priority:** High — data sovereignty is non-negotiable

---

**🐉 Summon / Seven Shadow System Feature — Sentinel Eye**
*"The shadows see what CI won't tell you."*

Agent-friendly PR monitoring built into Seven Shadow System. Three capabilities Jarred Sumner (@jarredsumner, Bun creator) publicly requested for `gh` CLI — we build it into the Seven Shadows instead:

1. **Unresolved PR comments** — pull review comments as structured markdown with `file:line` references. Agents can read exactly what needs fixing and where.
2. **Failing CI logs** — extract GH Action failure logs, filtered to the actual error (not 500 lines of setup noise). Agent gets the error, the context, and the file.
3. **Lint errors from CI** — parse lint/test output from action runs into structured format agents can act on.

The Seven Shadow System guard already hooks into PRs and CI. This extends it from "detect and block" to "detect, block, AND tell the agent exactly how to fix it." The guard becomes a coach.

**Why it surfaced:** @jarredsumner tweet (182 likes, 8.8K views, Feb 21 2026) — validated demand for agent-friendly PR tooling. Nobody's built this yet.
**Shop:** Seven Shadow System feature (not standalone Armory tool)
**Priority:** High — this is differentiation. First governance tool that feeds fix instructions back to agents.

---

## Recently Shipped

*Tools that graduated from the Forge into the Armory.*

<!-- Moved here when a concept gets built and merged -->

---

## How This Works

Every night, development activity from the last 24–48 hours gets reviewed. Patterns emerge — a script that kept getting reused, a manual process that should be automated, a gap in the toolkit that slowed things down. Those patterns become forge concepts.

Concepts sit here for community input before being built. Once built and tested, they graduate to the Armory and move to "Recently Shipped."

The inventory balance table keeps the Armory from getting lopsided — if weapons are stacked but spells are thin, the next build prioritizes spells. Quality over quantity, but balance matters.

---

*🏴‍☠️ [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.*
