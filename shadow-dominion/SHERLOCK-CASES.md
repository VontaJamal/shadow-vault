# Sherlock's Case Files 🔍

Every weapon in the Armory was forged because something went wrong. Sherlock narrates the investigation. The case IS the tutorial. The weapon is the solution.

## Quick Summary

- Each case documents a real operational failure and the tool or guide forged from it.
- Case narratives are intentionally thematic, but they map to practical engineering lessons.
- This file doubles as both lore and troubleshooting catalog.

Format: Short-form video (60-90s for Shorts, 3-5 min for full), Sherlock narrates with evidence floating around him, ends with the weapon reveal.

---

## Weapons

### Case #001: "A Study in Credentials" — Jutsu
**The crime:** API keys scattered across plaintext files. One wrong `git push` away from disaster. Multiple scripts had a GitHub token baked in — discovered during a midnight audit.
**The investigation:** Sherlock traces the token through every file it touched. Shows how one leaked key cascades into full account compromise.
**The weapon forged:** Jutsu — encrypted vault for API keys. Named swap profiles. One command to rotate. Never touches plaintext again.
**Holmes homage:** "A Study in Scarlet" — the first case, the one that started it all.

### Case #002: "The Hound of the Hard Stop" — Sentinel
**The crime:** A production service went down at 3 AM. Nobody knew until morning. 6 hours of silence while the kingdom burned.
**The investigation:** Sherlock reconstructs the timeline. Shows what failed, what should have caught it, and why nobody was watching.
**The weapon forged:** Sentinel — file watcher with instant alerts. The guard dog that never sleeps.
**Holmes homage:** "The Hound of the Baskervilles"

### Case #003: "The Adventure of the Missing Backup" — Phoenix Down
**The crime:** A catastrophic file loss. Work gone. No backup existed. The kingdom learned the hard way that recovery isn't optional.
**The investigation:** Sherlock walks through what was lost, how it happened, and the exact sequence that left the system unprotected.
**The weapon forged:** Phoenix Down — automated backup with resurrection capability. Rise from the ashes. Every time.
**Holmes homage:** "The Adventure of the Missing Three-Quarter"

### Case #004: "The Sign of the Four Services" — Scan
**The crime:** Four Windows services running — but were they ACTUALLY healthy? Status said "running." Reality said otherwise. Zombie services eating resources, returning stale data.
**The investigation:** Sherlock checks each service one by one. Shows the gap between "running" and "working." The lies a status check can tell.
**The weapon forged:** Scan — deep health check that goes beyond "is it on?" to "is it actually doing its job?"
**Holmes homage:** "The Sign of the Four"

### Case #005: "A Scandal in the Vault" — Aegis
**The crime:** Sensitive files sitting unencrypted on disk. One compromised machine = everything exposed. The kingdom's secrets weren't secret.
**The investigation:** Sherlock catalogs every exposed file. Shows the blast radius of a single breach. Makes the audience uncomfortable on purpose.
**The weapon forged:** Aegis — encryption shield for workspace files. What's locked stays locked.
**Holmes homage:** "A Scandal in Bohemia"

### Case #006: "The Curious Incident of the Silent Gateway" — Warp
**The crime:** The gateway died. No error. No log. Just... silence. The entire Court went dark. 45 minutes of nothing.
**The investigation:** Sherlock traces the failure back to a config change that seemed harmless. One setting, one cascade, total blackout.
**The weapon forged:** Warp — SSH-aware gateway management. Jump between machines, restart services, never go dark again.
**Holmes homage:** "Silver Blaze" ("the curious incident of the dog in the night-time")

### Case #007: "The Red-Headed Leak" — Truesight
**The crime:** Environment variables leaking into logs. Secrets appearing where they shouldn't. The system was bleeding information without knowing it.
**The investigation:** Sherlock follows the data trail. Shows exactly how env vars propagate through processes and end up in places nobody expected.
**The weapon forged:** Truesight — environment audit that reveals what's exposed and where.
**Holmes homage:** "The Red-Headed League"

### Case #008: "The Final Deploy" — Masamune
**The crime:** A deployment went sideways. Partial rollout. Half the system on the new version, half on the old. Frankenstack.
**The investigation:** Sherlock dissects the deployment pipeline. Shows every point where it could've been caught, where it wasn't, and why.
**The weapon forged:** Masamune — the precision deployment blade. Clean cuts only. No partial rollouts. No Frankenstacks.
**Holmes homage:** "The Final Problem"

---

## Spells

### Case #009: "The Musgrave Diagnostic" — Libra
**The crime:** System performance degrading slowly. Nobody could pinpoint when it started or why. Death by a thousand cuts.
**The investigation:** Sherlock runs the full diagnostic ritual. Memory, CPU, disk, network — layer by layer until the culprit surfaces.
**The spell learned:** Libra — system diagnostic that weighs every component and finds the imbalance.
**Holmes homage:** "The Musgrave Ritual"

### Case #010: "The Speckled Bandwidth" — Cure
**The crime:** Network issues. Intermittent. Maddening. Sometimes fine, sometimes crawling. No pattern visible to the naked eye.
**The investigation:** Sherlock monitors the network over time, spots the pattern everyone missed. The speckled bandwidth — it was regular all along.
**The spell learned:** Cure — network healing and diagnostics. Find the sickness, apply the fix.
**Holmes homage:** "The Adventure of the Speckled Band"

### Case #011: "The Crooked Config" — Protect
**The crime:** A malformed config file. One wrong character. The whole system reading defaults instead of real values, and nobody noticed for days.
**The investigation:** Sherlock diffs the config against what it should be. Shows how a single typo can cascade into system-wide wrong behavior.
**The spell learned:** Protect — config validation and backup. Never let a crooked config go unnoticed.
**Holmes homage:** "The Adventure of the Crooked Man"

### Case #012: "The Dancing Daemons" — Regen
**The crime:** Services dying and restarting in a pattern. Like a dance — up, down, up, down. Memory leak causing cyclical crashes.
**The investigation:** Sherlock charts the restart pattern. It's not random — it's rhythmic. The daemons are dancing to the beat of a memory leak.
**The spell learned:** Regen — service regeneration and health restoration. Stop the dance. Heal the daemon.
**Holmes homage:** "The Adventure of the Dancing Men"

### Case #013: "The Solitary Cyclist" — Chronicle
**The crime:** Nobody knows what happened last Tuesday. No logs. No history. The kingdom has amnesia.
**The investigation:** Sherlock pieces together what happened from git history, timestamps, and file modifications. Forensic reconstruction.
**The spell learned:** Chronicle — automated activity logging. The kingdom never forgets again.
**Holmes homage:** "The Adventure of the Solitary Cyclist"

### Case #014: "The Noble Victory" — Fanfare
**The crime:** Not a crime — a celebration. The Court achieved something massive and... nothing happened. No acknowledgment. No fanfare. Wins need to be felt.
**The investigation:** Sherlock argues that morale is infrastructure. Unacknowledged wins erode motivation as surely as bugs erode code.
**The spell learned:** Fanfare — victory sounds, notifications, celebrations. The kingdom hears when something great happens.
**Holmes homage:** "The Adventure of the Noble Bachelor"

---

## Summons

### Case #015: "The Valley of Fear" — Bahamut
**The crime:** A deployment so massive, so critical, that no single weapon could handle it. The kingdom needed overwhelming force.
**The investigation:** Sherlock reviews past deployment failures. Shows why incremental approaches fail at scale. Sometimes you need the nuclear option.
**The summon unlocked:** Bahamut — full-scale deployment. Megaflare. Everything at once. Total overwhelming force.
**Holmes homage:** "The Valley of Fear"

### Case #016-020: Remaining Summons
- **Ifrit** (Odin, Ramuh, Shiva, Alexander) — each tied to a Holmes case. Infrastructure fire, precision strikes, electrical/network, ice-cold rollbacks, divine protection.

---

## Items (Guides)

### Case #021: "The Copper Beeches Connection" — Telegram Setup
**The crime:** The Court had no communication channel. Agents running blind, no way to report, no way to alert.
**The investigation:** Sherlock demonstrates what happens when agents can't communicate. Missed alerts, duplicate work, zero coordination.
**The guide delivered:** Telegram Setup — connecting the Court's communication backbone.
**Holmes homage:** "The Adventure of the Copper Beeches"

### Case #022: "The Bruce-Partington Plans" — Agent Comms
**The crime:** Agents could talk to Indra but not to each other. Siloed intelligence. Left hand doesn't know what right hand is doing.
**The investigation:** Sherlock shows sensitive operational information (agent sessions) being duplicated because systems were isolated. The result was avoidable waste and coordination drag.
**The guide delivered:** Agent Comms — cross-agent communication wiring.
**Holmes homage:** "The Adventure of the Bruce-Partington Plans" (sensitive government plans)

### Case #023: "The Empty Service" — NSSM Services
**The crime:** A Windows service that should be running... isn't. The slot is empty. Nobody registered it properly.
**The investigation:** Sherlock walks through Windows service architecture. What NSSM does, why it matters, how services disappear.
**The guide delivered:** NSSM Services — proper service registration that sticks.
**Holmes homage:** "The Adventure of the Empty House"

---

*Every weapon was forged from a real problem. Every case is a real story. Sherlock just tells it better than anyone else could.* 🔍🏴‍☠️
