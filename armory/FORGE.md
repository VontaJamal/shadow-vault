# The Forge 🔥

**Where Armory tools are shaped before they ship.**

The Forge is the incubation space for concepts that may graduate into the Armory. Ideas stay here until they are validated through real usage and clear user value.

---

## Focus Areas

- **Weapons**: Direct CLI tools for daily engineering work
- **Spells**: Scheduled automations and recurring maintenance workflows
- **Summons**: Heavy operations and orchestration-level commands
- **Items**: Playbooks and operational guidance

Current emphasis is on improving automation coverage and operator guidance.

---

## Concepts in the Forge

*Updated from active development patterns and feedback.*

### Under Consideration

**⚔️ Weapon — Mega Phoenix**
*"What Phoenix Down does for one machine, Mega Phoenix does at ecosystem scale."*

A full account-level backup workflow for Git hosting data. It focuses on resilient mirroring, restorable history, and clear failure reporting so teams can recover quickly when upstream services are unavailable.

**Why it surfaced:** Repeated need for platform-independent backup ownership across multiple repositories.
**Shop:** Weapons
**Priority:** High

---

**🐉 Seven Shadow System Feature — Sentinel Eye**
*"Give agents actionable PR intelligence, not just pass/fail outcomes."*

Agent-friendly PR monitoring integrated into Seven Shadow System. Primary capabilities:

1. **Unresolved PR comments** in structured format with `file:line` references.
2. **Failing CI log extraction** focused on actionable error regions.
3. **Lint/test issue extraction** into machine-usable output.

**Why it surfaced:** Growing demand for governance systems that also provide repair guidance.
**Shop:** Seven Shadow System feature
**Priority:** High

---

**📜 Spell — Glamour**
*"Polish text for natural human readability before publication."*

A writing-finish workflow for public content. It targets repetitive AI-signature patterns and helps keep tone consistent across READMEs, social posts, and product copy.

**Why it surfaced:** Need for fast quality polish in public-facing writing workflows.
**Shop:** Spells
**Priority:** High

---

**⚔️ Weapon — Warp Gate**
*"Step through the portal. Land on any machine. No keys, no config, no hesitation."*

A connection manager for multi-machine setups. Stores SSH targets with aliases, auto-selects identity keys, and handles SCP transfers in both directions with a single command. Replaces manual `ssh -i ~/.ssh/id_ed25519 devon@192.168.1.188` calls.

**Why it surfaced:** Every session involves 3-5 manual SSH commands to Windows. Multi-machine orchestration is the #1 daily friction point across the entire ecosystem.
**Shop:** Weapons
**Priority:** High

---

**📜 Spell — Chronicle**
*"The kingdom remembers what the king forgets."*

An automated nightly git-log synthesizer that scans all repos, groups commits by theme, and produces a human-readable daily changelog. Feeds into the Forge, content pipeline, and weekly public output.

**Why it surfaced:** The nightly synthesis manually reconstructs git history every night. This should be a 1-command operation that outputs structured markdown.
**Shop:** Spells
**Priority:** High

---

**🛡️ Item — Rebrand Kit**
*"Change the name. Keep the soul."*

A playbook and script for coordinating renames across an entire ecosystem — repo names, package names, CLI commands, README references, submodule pointers, badge URLs. Tracks what was renamed, what still references the old name, and generates a completion checklist.

**Why it surfaced:** This week alone saw 4 rename waves (ck-flash→Grimoire, sss→7s, Monarch System→Shadowgate, rinshari-ui→rinshari-eye). Each required manual multi-repo grep-and-replace. This should be automated.
**Shop:** Items
**Priority:** Medium

---

**⚔️ Weapon — Deathblow**
*"One command. Every repo. Force aligned."*

A cross-repo enforcement tool that runs a single operation (lint rule, badge inject, submodule bump, config patch) across all Sovereign repositories in one pass. Dry-run mode shows what would change, `--execute` applies it. Generates a PR per repo or direct-pushes based on branch protection.

**Why it surfaced:** This week's "Protected by the Seven Shadows" badge rollout and "Shadow of Access" rebrand wave both required touching 10+ repos manually. Codex handled some via PRs, but the coordination was ad-hoc. A single `deathblow --apply badge` command would have done it in 30 seconds.
**Shop:** Weapons
**Priority:** High

---

**📜 Spell — Scryer**
*"The court watches the world so you don't have to."*

A scheduled web intelligence scraper that monitors specific sources (ANN for anime, CoinDesk/DexScreener for crypto, OpenClaw GitHub releases, Anthropic blog) and produces a structured daily digest. Replaces manual web searches during nightly synthesis and heartbeats. Outputs markdown with priority-tagged items.

**Why it surfaced:** Every nightly synthesis and every other heartbeat burns 3-5 web search calls that hit rate limits. Today's synthesis hit Brave API rate limits on 3 of 5 searches. A pre-cached scrape running at off-peak hours solves this completely.
**Shop:** Spells
**Priority:** High

---

**🛡️ Item — Garrison**
*"Know thy kingdom's borders."*

A repo health dashboard generator that scans all Sovereign repos and produces a single markdown report: uncommitted changes, behind-remote count, stale branches, missing badges, broken submodule pointers, CI status. Think `faye repos` but comprehensive and exportable.

**Why it surfaced:** Sherlock's tools (git-intel, cross-repo, dep-watch) each solve a piece of this but require separate invocations. A unified garrison report would feed into the nightly synthesis and Sherlock's 221B sweeps seamlessly.
**Shop:** Items
**Priority:** Medium

---

## Recently Shipped

**🎵 Spell — Fanfare**
Completion sound and notification options for long-running tasks.

**🔍 Item — 221B**
Repository diagnostics that surface configuration drift, stale paths, and structural issues with evidence-backed findings.

---

## Graduation Criteria

Concepts move from Forge to Armory when they meet all three criteria:

1. **Clear user problem** solved with repeatable value.
2. **Operational reliability** proven in real workflows.
3. **Usable documentation** that supports adoption without insider context.

---

*🏴‍☠️ [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.*
