# AIX Design System — NYHIMA 2026
**SUNY Poly AIX Center · Steve Schneider**
Last updated: June 2026

---

## FIRST: Ask the user which typography option to use

Before generating any output using this system, ask:

> "Which typography option — **B (IBM Plex Serif)** for a precise, technical-academic feel, or **E (EB Garamond)** for a classic university-press feel with a beautiful italic? Or should I show you both?"

Do not proceed until the user answers. Apply the chosen option consistently throughout all output in the session.

---

## Identity Overview

Two events. One design family. Distinguished by color temperature, not structure.

| | Workshop | Talk |
|---|---|---|
| **Event** | Reading and Writing with AI | Why Universal AI Literacy Matters |
| **Date** | Sunday, June 7, 2026 | Tuesday, June 9, 2026 |
| **Duration** | 3 hours | 1 hour |
| **Surface** | Navy dominant | AIX Ink dominant |
| **Accent** | Gold (decorative) | Signal blue |
| **Energy** | Practitioner, hands-on, activating | Argumentative, conceptual, editorial |

Both share: same type stack, same structural components, same dimensional palette, same SUNY Poly logo.

---

## Color System

### Core Palette

| Token | Hex | Usage | Notes |
|---|---|---|---|
| `--poly-navy` | `#002C73` | Workshop bg · logo | SUNY Poly brand primary |
| `--poly-gold` | `#EDA900` | **Decorative only** | NEVER as text — borders, rules, logo only |
| `--aix-ink` | `#0D1B2A` | Talk bg · deep surface | Deeper/cooler than Navy |
| `--aix-signal` | `#00B4D8` | Talk accent · key terms | 7.2:1 on Ink — AAA |
| `--aix-warm` | `#F4A261` | Human accent · judgment moments | 6.8:1 on Ink — AAA |
| `--cream` | `#FAF8F3` | Light surface · handouts | 12.0:1 Navy on cream — AAA |

### Critical Rule: Gold
`#EDA900` fails contrast against both Navy and Cream. It is **decorative only**:
- Horizontal rules / divider lines
- Border accents on cards
- Geometric shapes (not filled with text)
- The logo mark itself

Never use gold as a text color on any surface.

### Verified Contrast Pairs

| Foreground | Background | Ratio | Level |
|---|---|---|---|
| White `#FFFFFF` | Navy `#002C73` | 12.6:1 | AAA ✓ |
| Navy `#002C73` | Cream `#FAF8F3` | 12.0:1 | AAA ✓ |
| Signal `#00B4D8` | AIX Ink `#0D1B2A` | 7.2:1 | AAA ✓ |
| Warm `#F4A261` | AIX Ink `#0D1B2A` | 6.8:1 | AAA ✓ |
| Cyan D1 `#4CC9F0` | Navy `#002C73` | 7.8:1 | AAA ✓ |
| Mint D2 `#7BF1A8` | Navy `#002C73` | 9.1:1 | AAA ✓ |
| Gold-L D3 `#FFE380` | Navy `#002C73` | 7.4:1 | AAA ✓ |
| Amber D4 `#FFB347` | Navy `#002C73` | 6.2:1 | AAA ✓ |
| Rose D5 `#FF7096` | Navy `#002C73` | 5.3:1 | AA ✓ |
| Gold `#EDA900` | Navy `#002C73` | 3.88:1 | FAIL ✗ |
| Gold `#EDA900` | Cream `#FAF8F3` | 1.9:1 | FAIL ✗ |

### Dimensional Palette (Voxel Framework — 5 dimensions)

Chromatic arc: cool → warm. Used for framework visualizations, scenario bucket labels, voxel diagrams.

| Slot | Name | Dark (on Navy) | Light bg | Light border | Light text | Dimension |
|---|---|---|---|---|---|---|
| D1 | Cyan | `#4CC9F0` | `#E8F8FD` | `#4CC9F0` | `#0A5C73` | cognitive_mode |
| D2 | Mint | `#7BF1A8` | `#E8FDF2` | `#7BF1A8` | `#0A5C2A` | failure_mode |
| D3 | Gold-L | `#FFE380` | `#FFF9E0` | `#EDA900` | `#5C4200` | ai_visibility |
| D4 | Amber | `#FFB347` | `#FFF3E0` | `#FFB347` | `#5C3600` | output_type |
| D5 | Rose | `#FF7096` | `#FFF0F3` | `#FF7096` | `#5C0020` | stakes |

On dark (Navy/Ink) surfaces: use dark hex directly as text/fill color, text in `#002C73` (Navy) for D1–D4, `#5C0020` for D5.
On light surfaces: use light bg + border combination; text uses the light text value.

---

## Typography

### Option B — IBM Plex Serif + IBM Plex Sans + IBM Plex Mono
Google Fonts import:
```
https://fonts.googleapis.com/css2?family=IBM+Plex+Serif:ital,wght@0,400;0,600;1,400;1,600&family=IBM+Plex+Sans:wght@300;400;500&family=IBM+Plex+Mono:wght@400;500&display=swap
```
**Character:** Precise, technical-academic, institutional technology. No AI product associations.

### Option E — EB Garamond + IBM Plex Sans + IBM Plex Mono
Google Fonts import:
```
https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,600;1,400;1,600&family=IBM+Plex+Sans:wght@300;400;500&family=IBM+Plex+Mono:wght@400;500&display=swap
```
**Character:** Classic university press, brand-adjacent (Garamond is in SUNY Poly brand guide), beautiful italic. Closest to institutional compliance.

### CSS Variables (apply after user chooses)

```css
/* Option B */
--font-display: 'IBM Plex Serif', serif;

/* Option E */
--font-display: 'EB Garamond', serif;

/* Both options share: */
--font-body: 'IBM Plex Sans', sans-serif;
--font-mono: 'IBM Plex Mono', monospace;
```

### Type Scale

| Role | Font | Size (dark) | Size (light) | Weight | Color |
|---|---|---|---|---|---|
| H1 — title | `--font-display` | 26px (B) / 28px (E) | 22px (B) / 24px (E) | 600 | white / Navy |
| H2 — subtitle | `--font-display` | 18px (B) / 20px (E) | 15px (B) / 17px (E) | 600 | white 85% / Navy |
| Provocation / quote | `--font-display` italic | 15px (B) / 16px (E) | 13px (B) / 14px (E) | 400 italic | white 75% / Ink 75% |
| Body | `--font-body` | 13px | 12px | 300 | white 65% / text-secondary |
| Label / metadata | `--font-mono` | 10px | 10px | 400 | white 40% / text-secondary |

### Gold Rule
Every dark-surface title block opens with a 2px × 28–32px horizontal rule:
- Workshop (Navy bg): `background: #EDA900`
- Talk (Ink bg): `background: #00B4D8` (Signal, not gold)
- Handouts (Cream bg): `background: #EDA900`

This is the primary use of gold as a decorative element.

---

## Components

### Slide Title Block (dark surface)

```html
<div style="background: var(--poly-navy); padding: 2rem 2.5rem;">
  <!-- Workshop: gold rule. Talk: swap navy for --aix-ink, rule for signal -->
  <div style="width:32px; height:2px; background:#EDA900; margin-bottom:0.75rem;"></div>
  <h1 style="font-family:var(--font-display); font-size:26px; font-weight:600; color:white; line-height:1.15;">
    Slide Title Here
  </h1>
  <h2 style="font-family:var(--font-display); font-size:18px; font-weight:600; color:rgba(255,255,255,0.85); line-height:1.2; margin-top:0.5rem;">
    Subtitle or framing line
  </h2>
  <p style="font-family:var(--font-display); font-size:15px; font-style:italic; color:rgba(255,255,255,0.75); line-height:1.4; margin-top:0.4rem;">
    Provocation or key quote
  </p>
</div>
```

### Scenario Card (light surface)

```html
<div style="border:0.5px solid #e0ddd6; border-radius:10px; overflow:hidden; background:#FAF8F3;">
  <!-- Bucket color bar: D1 hex for data, D3 for policy, D5 for judgment -->
  <div style="height:4px; background:#4CC9F0;"></div>
  <div style="padding:1rem 1.25rem;">
    <div style="font-family:var(--font-mono); font-size:9px; letter-spacing:0.12em; text-transform:uppercase; color:#0A5C73; margin-bottom:0.4rem;">D1 · Data</div>
    <div style="font-family:var(--font-display); font-size:16px; font-weight:600; color:#002C73; line-height:1.2;">The Discharge Data</div>
    <div style="font-family:var(--font-body); font-size:12px; font-weight:300; color:#555; line-height:1.5; margin-top:0.35rem;">
      Situation summary goes here. 2–3 sentences max.
    </div>
  </div>
</div>
```

### Identity Pill

```html
<!-- Workshop -->
<span style="display:inline-block; padding:3px 10px; border-radius:12px; font-size:10px; font-weight:500; background:#EDA900; color:#002C73; font-family:var(--font-body);">Workshop · June 7</span>

<!-- Talk -->
<span style="display:inline-block; padding:3px 10px; border-radius:12px; font-size:10px; font-weight:500; background:#00B4D8; color:#0D1B2A; font-family:var(--font-body);">Talk · June 9</span>

<!-- AIX Center -->
<span style="display:inline-block; padding:3px 10px; border-radius:12px; font-size:10px; font-weight:500; background:transparent; color:#002C73; border:1.5px solid #002C73; font-family:var(--font-body);">SUNY Poly AIX Center</span>

<!-- Metadata -->
<span style="display:inline-block; padding:3px 10px; border-radius:12px; font-size:10px; font-weight:400; background:#FAF8F3; color:#0D1B2A; border:0.5px solid #ccc; font-family:var(--font-mono);">NYHIMA 2026</span>
```

### Dimensional Chip (dark surface, e.g. on Navy)

```html
<!-- Replace D1 values with appropriate dimension -->
<div style="background:#4CC9F0; border-radius:6px; padding:8px 10px; display:inline-block;">
  <div style="font-family:var(--font-body); font-size:11px; font-weight:500; color:#002C73; line-height:1.2;">cognitive_mode</div>
  <div style="font-family:var(--font-mono); font-size:9px; color:#002C73; opacity:0.7; margin-top:1px;">D1 · #4CC9F0</div>
</div>
```

### Contrast note block

```html
<div style="font-size:11px; line-height:1.5; padding:0.6rem 0.9rem; border-radius:6px; background:#FFF9E0; color:#5C4200; border-left:3px solid #EDA900;">
  Note text here. Used for system annotations, facilitator cues, compliance notes.
</div>
```

---

## CSS Custom Properties — Full Set

Paste at the top of any HTML output using this system:

```css
:root {
  /* Core palette */
  --poly-navy: #002C73;
  --poly-gold: #EDA900;       /* decorative only */
  --aix-ink: #0D1B2A;
  --aix-signal: #00B4D8;
  --aix-warm: #F4A261;
  --cream: #FAF8F3;

  /* Dimensional palette */
  --d1: #4CC9F0;  --d1-bg: #E8F8FD;  --d1-border: #4CC9F0;  --d1-text: #0A5C73;
  --d2: #7BF1A8;  --d2-bg: #E8FDF2;  --d2-border: #7BF1A8;  --d2-text: #0A5C2A;
  --d3: #FFE380;  --d3-bg: #FFF9E0;  --d3-border: #EDA900;  --d3-text: #5C4200;
  --d4: #FFB347;  --d4-bg: #FFF3E0;  --d4-border: #FFB347;  --d4-text: #5C3600;
  --d5: #FF7096;  --d5-bg: #FFF0F3;  --d5-border: #FF7096;  --d5-text: #5C0020;

  /* Typography — SET AFTER USER CHOOSES OPTION */
  /* Option B: */ --font-display: 'IBM Plex Serif', serif;
  /* Option E: */ /* --font-display: 'EB Garamond', serif; */
  --font-body: 'IBM Plex Sans', sans-serif;
  --font-mono: 'IBM Plex Mono', monospace;
}
```

---

## Design Rules (enforce these in all output)

1. **Gold is never text.** On any surface. Ever. Borders and rules only.
2. **White headings on dark.** H1 and H2 are white on Navy or Ink. No exceptions.
3. **The rule marks the identity.** Every title block opens with a 2px horizontal rule — gold for Workshop/handouts, Signal for Talk.
4. **Mono for metadata.** Dates, IDs, URLs, scenario codes, sprint labels — always IBM Plex Mono.
5. **Body weight is 300.** IBM Plex Sans Light (300) for body text. 400 for UI labels. 500 for emphasis only.
6. **Provocation lines are italic serif.** The load-bearing rhetorical lines ("Who prompted that?", "The model won't own it.") — always italic display font, never sans.
7. **Dimensional colors encode meaning.** D1–D5 are not decorative. They map to the voxel framework dimensions consistently across all materials.
8. **AIX Ink ≠ Navy.** Talk uses `#0D1B2A`, Workshop uses `#002C73`. Do not substitute one for the other.
9. **Signal accent for Talk, Gold accent for Workshop.** The rule color is the fastest identity signal — get it right.
10. **WCAG AA minimum on everything.** Check all text combinations before finalizing. The verified pairs table above covers all standard cases.

---

## File Naming Convention

```
[event]-[type]-[descriptor]
nyhima-workshop-slide-opening
nyhima-talk-slide-directive-ai
nyhima-shared-handout-reference-card
nyhima-shared-scenario-D1
nyhima-shared-scenario-J3
```

---

## Fonts — Google Fonts Import (both options, trim after user chooses)

```html
<!-- Option B — IBM Plex family -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Serif:ital,wght@0,400;0,600;1,400;1,600&family=IBM+Plex+Sans:wght@300;400;500&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">

<!-- Option E — EB Garamond + IBM Plex Sans/Mono -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,600;1,400;1,600&family=IBM+Plex+Sans:wght@300;400;500&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
```

---

*SUNY Poly AIX Center · sunypolyaix.github.io · steve@sunypoly.edu*
