---
name: The Gathered Table
description: Full-service catering, Central Oregon — refined black, gold, and cream
colors:
  black: "#0c0b0a"
  black-2: "#141210"
  char: "#1c1916"
  gold: "#c9a24b"
  gold-bright: "#e0bd72"
  gold-soft: "#d9bf8a"
  cream: "#f3ead6"
  cream-dim: "#cdc3ad"
typography:
  display:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "clamp(2.8rem, 7vw, 5.4rem)"
    fontWeight: 600
    lineHeight: 1.08
  headline:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "clamp(2rem, 4.6vw, 3.2rem)"
    fontWeight: 600
    lineHeight: 1.08
  title:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "1.5rem"
    fontWeight: 600
    lineHeight: 1.2
  body:
    fontFamily: "Jost, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.7
    letterSpacing: "0.02em"
  label:
    fontFamily: "Jost, system-ui, sans-serif"
    fontSize: "0.78rem"
    fontWeight: 400
    letterSpacing: "0.38em"
rounded:
  sm: "10px"
  md: "16px"
  lg: "24px"
  button: "2px"
spacing:
  sm: "16px"
  md: "26px"
  lg: "48px"
  section: "clamp(4rem, 8vw, 7rem)"
components:
  button-gold:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.black}"
    rounded: "{rounded.button}"
    padding: "0.95rem 1.9rem"
  button-gold-hover:
    backgroundColor: "{colors.gold-bright}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.gold}"
    rounded: "{rounded.button}"
    padding: "0.95rem 1.9rem"
  card-offering:
    backgroundColor: "{colors.char}"
    textColor: "{colors.cream}"
    rounded: "{rounded.sm}"
    padding: "2rem 1.7rem"
---

# Design System: The Gathered Table

## Overview

**Creative North Star: "The Gathered Table"**

The brand name is the metaphor — gathering as ritual, warmth in darkness, gold light catching on cream. This design system works entirely in candlelit dramatic contrast: near-black surfaces that recede into shadow while gold accents concentrate the eye. Every screen is a table set for something worth attending.

Cormorant Garamond carries the voice: tall, classical, confident without posture. It earns its weight at display sizes — nearly 5.4rem at full stretch — and pairs with Jost's clean utility for body text that never competes. Tangerine script decorates sparingly, like a handwritten flourish on a menu card. Borders are gold and translucent, so even the dividers feel warm rather than structural.

Motion is slow and deliberate. Cards take 400ms to settle on hover; reveals stagger at 100ms per step. Nothing snaps. Luxury is patience.

**Key Characteristics:**
- Dark-ground system — cream text on near-black throughout
- Translucent gold borders (`rgba(201,162,75,.22)`) unify without heaviness
- Near-square buttons with uppercase labels — formal and unhurried
- Cormorant Garamond at up to 5.4rem for display — large type earns gravitas
- Eyebrow ornament variant with flanking gold dashes reinforces the fine-dining register

## Colors

A candlelit palette: three near-blacks, three golds, two creams. Nothing outside this range.

### Primary
- **Antique Gold** (`#c9a24b`): The action color. Button backgrounds, icon accents, all border treatments, hover text. The warmth source of the entire system.
- **Bright Champagne** (`#e0bd72`): Button hover state, headline `em` spans, script text. Lighter and more luminous than the base gold.
- **Soft Dusk Gold** (`#d9bf8a`): Decorative elements, `.script` ornament highlights. Warmer and less saturated.

### Neutral (dark)
- **Blackwood** (`#0c0b0a`): Page background. The deepest surface.
- **Char-Dark** (`#141210`): Section gradient origin, hero layer beneath the radial tint.
- **Ember** (`#1c1916`): Card surfaces, info blocks, family card backgrounds. Warm near-black with a brown undertone.

### Neutral (light)
- **Aged Cream** (`#f3ead6`): Primary text on all dark surfaces. Warm — feels like quality paper, not a screen.
- **Dimmed Cream** (`#cdc3ad`): Supporting copy, card descriptors, footer link color.
- **Gold Line** (`rgba(201,162,75,.22)`): All borders and dividers. Translucent gold rather than grey.

### Named Rules
**The Dark-Ground Rule.** Cream on near-black is the resting state of this system. Do not introduce white-background sections. Light surfaces appear only inside individual card elements where contrast against the dark card is required.

**The One Gold Rule.** Antique Gold is the action accent; Bright Champagne is hover only. Using both simultaneously on a single element — e.g., gold text over champagne background — collapses the palette.

## Typography

**Display Font:** Cormorant Garamond (Georgia, serif)
**Body Font:** Jost (system-ui fallback)
**Script Accent:** Tangerine (cursive) — hero pre-copy and inline `em` spans only

**Character:** Cormorant Garamond's high-contrast strokes carry luxury without affectation. Jost's geometric neutrality serves body text that recedes correctly — it never competes with the serifs. Tangerine adds one flourish per hero, like a personal signature on a menu.

### Hierarchy
- **Display** (600, clamp 2.8–5.4rem, lh 1.08): Hero h1. Includes Tangerine `em` spans at 1.35em for named items or the brand tagline word.
- **Headline** (600, clamp 2–3.2rem, lh 1.08): Section h2. Cream; gold `em` spans for one emphatic word.
- **Title** (600, 1.5rem, lh 1.2): Card h3, numbered list heads. Cream.
- **Body** (400, 1rem, lh 1.7, ls 0.02em): Jost. Card descriptors, prose. Cream-dim. ~50ch max.
- **Label** (400, 0.78rem, ls 0.38em, uppercase): Eyebrow, nav links, button text. Gold. The `.eyebrow.lined` variant flanks with 28px horizontal gold rules.

### Named Rules
**The Serif Heading Rule.** Every h1, h2, and h3 uses Cormorant Garamond. Jost handles labels, eyebrows, nav, and body — never headings. Never mix at the same hierarchy level.

## Layout

Container max-width 1160px, 26px horizontal padding. Hero is centered single-column with the inner content constrained to 820px — the near-black background bleeds edge-to-edge while copy centers. Section vertical rhythm: `clamp(4rem, 8vw, 7rem)` — more generous than the flagship, befitting the slower pace. Offerings grid: three-column (two at 920px, one at 600px). Experience/about split: 50/50 (stacks at 920px). Gallery: four-column with a tall-spanning first image (two at 920px). Scroll-reveal: 800ms ease, 26px translateY, 100ms stagger.

Breakpoints: 920px (tablet), 600px (mobile — hamburger, single column, ghost button hidden).

## Elevation & Depth

No ambient shadow tokens. Depth is achieved through tonal layering: near-black surfaces stack from Blackwood (`#0c0b0a`) → Char-Dark (`#141210`) → Ember (`#1c1916`) card surfaces. Cards appear lighter than their background — the inverse of the standard model. Hover lift uses `translateY(-7px)` and a pure-black box-shadow (`rgba(0,0,0,.5)`) that recedes into the background rather than drawing attention to itself.

### Named Rules
**The Tonal Depth Rule.** Depth is expressed by tone, not shadow. The only shadow appears on hover, and it uses pure `rgba(0,0,0)` — not gold, not navy — so it disappears into the surrounding darkness rather than calling attention.

## Shapes

Near-square buttons (2px radius) — almost a right angle, like the corner of a pressed linen napkin. Cards use gentle rounding: 10px small (offering cards, info blocks), 16px medium (about and interior cards), 24px large (CTA container). The gold ornamental divider — two fading horizontal lines flanking a 6px square rotated 45° in gold — appears after the hero and between major sections as pacing punctuation. The cloche SVG icon (96px × 56px) in the hero is the brand's one bespoke illustration; it floats gently above the headline.

## Components

### Buttons
- **Shape:** Near-square (2px radius), Jost 500, 0.82rem, ls 0.16em, uppercase
- **Gold Primary:** Antique Gold (`#c9a24b`) background, blackwood text, 0.95rem×1.9rem padding
- **Hover:** Bright Champagne background, –2px translateY, gold shadow (`rgba(201,162,75,.25)`)
- **Ghost:** Transparent, 1px gold border, gold text → subtle gold-tint background on hover

### Cards / Containers
- **Offering Card:** `linear-gradient(180deg, #1c1916, #141210)` background, 10px radius, 1px gold-translucent border, 2rem×1.7rem padding. Hover: –7px lift, border brightens, 2px gold gradient bar fades in at the bottom.
- **Family Cards:** Ember background, gold-translucent border, same radius. Hover: border intensifies.
- **CTA Block:** Radial gold glow (subtle) at top center on near-black, 1px gold border, 24px radius.

### Inputs / Fields
- **Style:** `rgba(0,0,0,.3)` background, 1px gold-translucent border, 10px radius
- **Focus:** Gold border, 3px gold glow (`rgba(201,162,75,.15)`)
- **Label:** Jost 400, 0.72rem, ls 0.12em, uppercase, gold
- **Placeholder:** `#8a7f68` — warm mid-tone

### Navigation
- **Style:** Frosted dark glass (82% black-2, 12px blur), 84px height, 1px gold-translucent bottom border
- **Links:** Jost 400, 0.82rem, ls 0.14em, uppercase, cream-dim → cream on hover; 1px gold underline from left
- **Logo:** Cormorant Garamond 1.25rem cream; micro Jost gold label below
- **Mobile:** Hamburger at 600px

### Gold Divider (Signature Component)
Three-element ornament centered on the page: a left SVG line that fades from gold to transparent, a 6px square rotated 45° (filled gold), a right SVG line fading transparent to gold. Appears after the hero headline and between alternating content sections.

## Do's and Don'ts

### Do:
- **Do** keep all section backgrounds dark. No white-background breaks anywhere in the site.
- **Do** use Cormorant Garamond for every h1, h2, and h3 — without exception.
- **Do** include the gold divider ornament between the hero and the first content section on every page.
- **Do** allow 400ms for card hover transitions — the slower pace is intentional.
- **Do** use the `.eyebrow.lined` variant (with flanking dashes) when eyebrows appear centered above a section heading.

### Don't:
- **Don't** use white-background sections inside the site — there are no light surface breaks.
- **Don't** use Tangerine as a heading font or in body text. It's one inline span per hero only.
- **Don't** apply more than two gold shades simultaneously on a single element.
- **Don't** swap the hero background for anything other than a gold radial gradient on near-black.
- **Don't** round buttons beyond 2px. The near-square formality is load-bearing.
