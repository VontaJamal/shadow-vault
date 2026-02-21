# Website Color Spec — Exact Directives

Pass this to the AI building the site. Every element, exact hex. No interpretation needed.

## The Palette (ONLY these colors)

| Token | Hex | Use |
|-------|-----|-----|
| `--black` | `#0A0A0F` | Page background |
| `--surface` | `#121217` | Card backgrounds, containers |
| `--surface-2` | `#1A1A22` | Nested cards, secondary surfaces |
| `--crimson` | `#B3122C` | Primary accent, CTAs, brand color |
| `--crimson-dark` | `#7A0D21` | Hover states, deeper red accents |
| `--crimson-glow` | `rgba(179,18,44,0.18)` | Controlled atmospheric glow behind key elements |
| `--gunmetal` | `#32343B` | Borders, dividers |
| `--ash` | `#24242D` | Subtle backgrounds, depth layers |
| `--bone` | `#E7E2DA` | Primary text |
| `--bone-dim` | `#AAA39A` | Secondary/muted text |
| `--bone-faint` | `#7A746D` | Tertiary text, labels |
| `--ember` | `#E14A22` | Sparingly — event-level heat accents only |
| `--white` | `#FFFFFF` | Stats numbers, bold callouts only |

## BANNED Colors
- **NO gold/amber/yellow as base accents** (#D4A843, #C8A84E, etc.) — ember token is explicitly allowed for sparse heat accents only
- **NO pink/salmon/rose** (#D4707A, #CC7080, etc.) — not in the palette
- **NO purple/lavender** — AI company color
- **NO bright blue** (#3B82F6) — the pagination dot, nav items, anything
- **NO teal/green**
- **NO gradient profile rings** — if there's a ring, it's solid crimson

---

## Element-by-Element Spec

### Page Background
- `--black` (#0A0A0F) everywhere. No exceptions.

### Top Navigation
- **Nav bar background:** `--surface` with 90% opacity (slight transparency is fine)
- **Nav border:** `--gunmetal`
- **Logo "DJ" monogram:** Replace gold circle with `--crimson` circle, white initials
- **"Shadow Dominion" text:** `--bone`
- **Active nav item (Home):** Background pill = `--crimson-dark`, text = `--white`
- **Inactive nav items:** Text = `--bone-dim`, icons = `--bone-faint`
- **All nav icons:** `--bone-faint` (no gold, no colored icons)
- **Notification badge:** Border = `--gunmetal`, text = `--bone-dim`

### Hero — Left Side

#### "SHADOW DOMINION" Badge
- Background: `--surface`
- Border: `--crimson-dark`
- Text: `--crimson` (uppercase, letterspaced)

#### "DEVONTA JOHNSON"
- Text: `--bone`

#### "EXECUTE ⚔️"
- "EXECUTE" text: `--crimson` (#B3122C)
- Swords icon: `--crimson` (NOT gold — this is the most important element on the page)

#### Subtitle
- Text: `--bone-dim`

#### Typing/Terminal Card
- Background: `--surface`
- Border: `--gunmetal`
- Bullet dot: `--crimson` (NOT gold)
- "AI Systems" text: `--bone-dim`
- "Architect" text: `--crimson` (the active/typed word highlights in red)
- Cursor: `--crimson`

#### Civilian Translation Card
- Background: `--surface-2`
- Border: `--gunmetal`
- "Civilian translation:" label: `--bone`
- Body text: `--bone-dim`

#### Skill/Tag Badges
- Background: transparent
- Border: `--gunmetal`
- Text: `--bone-dim`

#### Target Audience Text
- Text: `--bone-faint`

#### CTA Buttons
- **"Connect on LinkedIn":** Background = `--crimson`, text = `--white`. Hover = `--crimson-dark`
- **"Watch RenderATL Talk":** Background = transparent, border = `--crimson-dark`, text = `--crimson`. Hover = `--crimson-glow` background

### Profile Card — Right Side

#### Card Container
- Background: `--surface`
- Border: `--gunmetal`

#### "MONARCH MODE" Badge
- Background: `--surface-2`
- Border: `--crimson-dark`
- Text: `--crimson` (NOT gold — this is a rank, not a prize)

#### Profile Photo Ring
- Solid `--crimson` ring. No gradient. No gold. No pink. Just red.

#### Stats Row
- Numbers ("10+", "24/7", "150+"): `--white`
- Labels: `--bone-faint`

#### Description Box
- Background: `--surface-2`
- Text primary: `--bone`
- Text secondary (civilian translation): `--bone-dim`

#### "Connect on LinkedIn" Button
- Background: `--crimson`, text: `--white`

#### "View GitHub" Button
- Background: `--surface-2`, border: `--gunmetal`, text: `--bone`

#### RenderATL Floating Badge
- Background: `--surface`
- Border: `--crimson-dark`
- "RenderATL" text: `--white`
- "Watch talk" text: `--crimson`

#### "Systems + People" Floating Card
- Background: `--surface`
- Border: `--gunmetal`
- Title: `--bone`
- Subtitle: `--bone-dim`

### Footer / Pagination
- "Explore more" text: `--bone-faint`
- Active dot: `--crimson` (NOT blue)
- Inactive bar: `--gunmetal`

---

## General Rules

1. **Crimson red is the primary accent color.** Nothing else competes with it in recurring UI emphasis.
2. **White (#FFFFFF) is reserved for stats/numbers and bold callouts.** Regular text uses bone (#E7E2DA).
3. **All borders are gunmetal.** No warm-tinted borders, no rose/burgundy borders.
4. **No color variety in the nav icons.** They're all the same muted gray.
5. **The page should feel like you're looking at a dark terminal with blood-red highlights.** Not a SaaS landing page.
6. **Hover states:** crimson elements get slightly darker (crimson-dark), ghost buttons get a subtle crimson glow.
7. **No element should be gold, amber, yellow, pink, salmon, purple, blue, teal, or green as a base accent.** The only recurring colors are black, shades of gray, bone white, and crimson red; ember is allowed only for sparse heat moments.

## Intensity Guardrails

- Crimson usage target: **8–14%** of visible UI area.
- Ember usage target: **<=2%** of visible UI area.
- At least **60%** of text should be `--bone`/`--bone-dim`, not pure white.
