# SOVEREIGN CIV MODE — Ecosystem Spec

## Overview

Every tool in the Sovereign ecosystem speaks two languages. Civ mode strips all theming — FF names, Solo Leveling references, shadow terminology — and presents clean, professional output that any developer or enterprise team can use without context.

One convention. Every tool respects it.

---

## The Convention: `SOVEREIGN_MODE`

### Priority Chain (highest wins)

1. **CLI flag:** `--civ` (per-command)
2. **Repo config:** `.sovereign.json` → `{ "mode": "civ" }` (per-project)
3. **Env var:** `SOVEREIGN_MODE=civ` (per-shell/machine)
4. **Global config:** `~/.sovereign/config.json` → `{ "mode": "civ" }` (per-user)
5. **Default:** lore mode

### Values

- `lore` — full theming, FF names, shadow terminology, emoji, personality (default)
- `civ` — plain English, professional, no references, minimal emoji

---

## Per-Tool Mappings

### The Armory

| Lore | Civ | What It Does |
|------|-----|-------------|
| `ramuh` / `armory ramuh` | `diagnostics` / `armory diagnostics` | System health check |
| `odin` / `armory odin` | `cleanup` / `armory cleanup` | Kill zombie processes |
| `shiva` / `armory shiva` | `snapshot` / `armory snapshot` | System state capture + diff |
| `jutsu` / `armory jutsu` | `keys` / `armory keys` | API key vault + hot-swap |
| `scan` / `armory scan` | `audit` / `armory audit` | Security scan for leaked secrets |
| `phoenix-down` | `backup` | Encrypted backup + restore |
| `masamune` | `keyswap` | Quick API key rotation |
| `sentinel` / `aegis` | `healthcheck` | Service monitoring |
| `cure` | `verify-backup` | Backup integrity check |
| `libra` | `daily-intel` | Daily briefing generator |
| `protect` | `auto-audit` | Scheduled security audit |
| `regen` | `morning-brief` | Morning briefing |
| `bahamut` | `deploy` | Full empire deployment |
| `ifrit` | `spawn-agents` | Agent spawner |
| `warp` | `ssh` | Quick SSH jumps |
| `armory civs` | N/A (already in civ mode) | Show civilian name mappings |
| ⚡ Judgment Bolt | System Diagnostic | Ramuh's banner text |
| ❄️ Diamond Dust | State Snapshot | Shiva's banner text |
| ⚔️ Zantetsuken | Process Cleanup | Odin's banner text |

#### Armory Implementation

The Armory already has `armory civs` — a command that shows the mapping table. With `SOVEREIGN_MODE=civ`:

- All script banners use plain names instead of FF names
- `--help` output shows plain descriptions
- Tab completion suggests civilian names
- The `armory` command itself stays (it's not themed, it's the tool name)

```powershell
# In every Armory script, add at the top:
$civMode = ($env:SOVEREIGN_MODE -eq 'civ') -or (Test-Path '.sovereign.json' -and (Get-Content '.sovereign.json' | ConvertFrom-Json).mode -eq 'civ')

if ($civMode) {
    $banner = "System Diagnostic"
} else {
    $banner = "Judgment Bolt"
}
```

---

### Seven Shadow System

| Lore | Civ |
|------|-----|
| "Seven Shadow System — Gauntlet Results" | "PR Quality Gate — Results" |
| "Shadow 1: Security" | "1. Security" |
| "Doctrine" | "Policy" |
| "shadow violated" | "check failed" |
| "ALL SHADOWS SATISFIED" | "ALL CHECKS PASSED" |
| 🛡️ ⚔️ emoji | ✅ ❌ ⚠️ only |
| "Protected by the Seven Shadows" | "PR quality enforced" |

*Full spec: `seven-shadow-system/BUILD-SPEC-CIV-MODE.md`*

---

### Shadow Gate

| Lore | Civ |
|------|-----|
| "Quest log" | "Activity log" |
| "XP" | "Points" |
| "Rank: S-Class Hunter" | "Level: Advanced" |
| "Streak" | "Streak" (stays — it's already plain) |
| "Gate" | "Challenge" |
| "Arise" | "Start" |
| "Shadow Army" | "Team" |
| "Penalty" | "Penalty" (stays) |
| Solo Leveling rank names | Numbered tiers (1-10) |

---

### Faye (Voice AI)

| Lore | Civ |
|------|-----|
| "Arise" (activation) | "Activate" |
| "Faye" (wake word) | User-configured name |
| Personality/sass in responses | Neutral/professional responses |

Note: Faye's personality IS the product for most users. Civ mode here mainly affects documentation and setup output, not the voice interaction itself.

---

### Dojo

| Lore | Civ |
|------|-----|
| "White Belt → Black Belt" | "Beginner → Advanced" |
| "Training Arc" | "Learning Path" |
| "Hyperbolic Time Chamber" | Removed |
| "Kata" | "Exercise" |
| "Sensei" | "Instructor" |

---

### README Badges

Every Sovereign repo provides two badge options:

**Lore:**
```markdown
## Protected by the [Seven Shadows](https://github.com/VontaJamal/seven-shadow-system)

Part of [Sovereign](https://github.com/VontaJamal) — The Shadow Dominion.
```

**Civ:**
```markdown
## PR Quality · [Seven Shadow System](https://github.com/VontaJamal/seven-shadow-system)

Part of [Sovereign](https://github.com/VontaJamal).
```

---

## Shared `getMode()` Utility

Every Sovereign tool uses the same mode detection logic. This will eventually be extracted into a shared package (`@sovereign/config` or similar), but for now each tool implements it:

### JavaScript/Node

```js
const fs = require('fs');
const path = require('path');

function getMode(cliArgs = {}) {
  // 1. CLI flag
  if (cliArgs.civ) return 'civ';
  
  // 2. Repo config (walk up from cwd)
  let dir = process.cwd();
  while (dir !== path.dirname(dir)) {
    const configPath = path.join(dir, '.sovereign.json');
    if (fs.existsSync(configPath)) {
      try {
        const config = JSON.parse(fs.readFileSync(configPath, 'utf8'));
        if (config.mode) return config.mode;
      } catch {}
    }
    dir = path.dirname(dir);
  }
  
  // 3. Env var
  if (process.env.SOVEREIGN_MODE) return process.env.SOVEREIGN_MODE;
  
  // 4. Global config
  const globalConfig = path.join(process.env.HOME || process.env.USERPROFILE, '.sovereign', 'config.json');
  if (fs.existsSync(globalConfig)) {
    try {
      const config = JSON.parse(fs.readFileSync(globalConfig, 'utf8'));
      if (config.mode) return config.mode;
    } catch {}
  }
  
  // 5. Default
  return 'lore';
}

module.exports = { getMode };
```

### PowerShell

```powershell
function Get-SovereignMode {
    param([switch]$Civ)
    
    # 1. CLI flag
    if ($Civ) { return 'civ' }
    
    # 2. Repo config
    $dir = Get-Location
    while ($dir) {
        $config = Join-Path $dir '.sovereign.json'
        if (Test-Path $config) {
            $json = Get-Content $config | ConvertFrom-Json
            if ($json.mode) { return $json.mode }
        }
        $parent = Split-Path $dir -Parent
        if ($parent -eq $dir) { break }
        $dir = $parent
    }
    
    # 3. Env var
    if ($env:SOVEREIGN_MODE) { return $env:SOVEREIGN_MODE }
    
    # 4. Global config
    $global = Join-Path $env:USERPROFILE '.sovereign\config.json'
    if (Test-Path $global) {
        $json = Get-Content $global | ConvertFrom-Json
        if ($json.mode) { return $json.mode }
    }
    
    # 5. Default
    return 'lore'
}
```

### Bash/Zsh

```bash
get_sovereign_mode() {
    # 1. CLI flag handled by caller
    
    # 2. Repo config (walk up)
    local dir="$PWD"
    while [ "$dir" != "/" ]; do
        if [ -f "$dir/.sovereign.json" ]; then
            local mode=$(cat "$dir/.sovereign.json" | grep -o '"mode"[[:space:]]*:[[:space:]]*"[^"]*"' | cut -d'"' -f4)
            [ -n "$mode" ] && echo "$mode" && return
        fi
        dir=$(dirname "$dir")
    done
    
    # 3. Env var
    [ -n "$SOVEREIGN_MODE" ] && echo "$SOVEREIGN_MODE" && return
    
    # 4. Global config
    if [ -f "$HOME/.sovereign/config.json" ]; then
        local mode=$(cat "$HOME/.sovereign/config.json" | grep -o '"mode"[[:space:]]*:[[:space:]]*"[^"]*"' | cut -d'"' -f4)
        [ -n "$mode" ] && echo "$mode" && return
    fi
    
    # 5. Default
    echo "lore"
}
```

---

## .sovereign.json Schema

```json
{
  "mode": "civ",
  "version": 1
}
```

Minimal. Future fields can include tool-specific overrides, but mode is the only one that matters now.

---

## Implementation Priority

1. **Seven Shadow System** — already specced, pass to agent
2. **Armory** — already has `civs` command, extend to `--civ` flag + mode detection
3. **Shadow Gate** — when it ships
4. **Faye** — lowest priority (personality is the product)
5. **Dojo** — when it materializes

---

## Success Criteria

1. `SOVEREIGN_MODE=civ` set once → every Sovereign tool on the machine outputs plain English
2. `.sovereign.json` in a repo → any Sovereign tool in that repo runs civ without per-user setup
3. `--civ` on any command → immediate override, no config needed
4. Zero functionality difference between modes
5. A team unfamiliar with anime/FF/Solo Leveling can use every tool without confusion

---

*Two faces. One system. The civilians see professional tools. The Court sees weapons.*
