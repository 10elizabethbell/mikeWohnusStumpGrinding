---
name: Stump Grinding
description: The owner's yard sign, standing in the visitor's lawn. Send a picture of your stump, get a free quote.
colors:
  ground: "#173d28"
  ground-deep: "#11301f"
  cream: "#f2ecd9"
  cream-ink: "#173d28"
  ink-soft: "#c9d8c4"
  ink-soft-cream: "#3f5a46"
  sawdust: "#e3a95b"
  error: "#ffb4a2"
typography:
  display:
    fontFamily: "\"Arial Narrow\", \"Helvetica Neue\", \"sans-serif-condensed\", \"Roboto Condensed\", -apple-system, BlinkMacSystemFont, \"Segoe UI\", Arial, sans-serif"
    fontSize: "clamp(42px, 12.5vw, 96px)"
    fontWeight: 900
    lineHeight: 0.93
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "\"Arial Narrow\", \"Helvetica Neue\", \"sans-serif-condensed\", \"Roboto Condensed\", -apple-system, BlinkMacSystemFont, \"Segoe UI\", Arial, sans-serif"
    fontSize: "clamp(32px, 8.6vw, 56px)"
    fontWeight: 900
    lineHeight: 0.98
    letterSpacing: "-0.005em"
  phone:
    fontFamily: "\"Arial Narrow\", \"Helvetica Neue\", \"sans-serif-condensed\", \"Roboto Condensed\", -apple-system, BlinkMacSystemFont, \"Segoe UI\", Arial, sans-serif"
    fontSize: "clamp(40px, 11vw, 76px)"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: "0.01em"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "21px"
    fontWeight: 800
    lineHeight: 1.2
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 700
    lineHeight: 1.3
  small:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.45
rounded:
  field: "12px"
  pill: "999px"
  disc: "50%"
spacing:
  gutter-sm: "16px"
  gutter: "20px"
  gutter-lg: "40px"
components:
  button-solid:
    backgroundColor: "{colors.cream}"
    textColor: "{colors.cream-ink}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
    height: "58px"
  button-solid-hover:
    backgroundColor: "{colors.sawdust}"
    textColor: "{colors.cream-ink}"
  button-solid-on-cream:
    backgroundColor: "{colors.ground}"
    textColor: "{colors.cream}"
    rounded: "{rounded.pill}"
    height: "58px"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.cream}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
    height: "58px"
  button-line-hover:
    textColor: "{colors.sawdust}"
  input-field:
    backgroundColor: "{colors.cream}"
    textColor: "{colors.cream-ink}"
    rounded: "{rounded.field}"
    padding: "14px"
    height: "54px"
  chip:
    backgroundColor: "transparent"
    textColor: "{colors.cream}"
    rounded: "{rounded.field}"
    padding: "0 18px"
    height: "50px"
  chip-selected:
    backgroundColor: "{colors.cream}"
    textColor: "{colors.cream-ink}"
  step-numeral:
    backgroundColor: "{colors.cream-ink}"
    textColor: "{colors.cream}"
    rounded: "{rounded.disc}"
    size: "52px"
  sign-board:
    backgroundColor: "{colors.cream}"
    textColor: "{colors.cream-ink}"
---

# Design System: Stump Grinding

## Overview

**Creative North Star: "The Yard Sign in Your Lawn"**

The system is the owner's own corrugated yard sign (src-assets/post.jpg) translated to a phone: forest green and cream, heavy condensed uppercase lettering, the stump-with-rings mark, thin rule lines, and the phone number set as large as the headline. Green surfaces are lawn; cream surfaces are sign boards planted in it. Where a board meets the lawn, grass grows up over its bottom edge.

Density is low and plain-spoken. One column on phones, generous tap targets (44px minimum, 50-58px for primary controls), no ornament that the sign itself does not carry. Motion is confined to two places: the hero stump being ground and the grass edges. Everything else is still.

The direction contract lives as a comment at the top of `<body>` in index.html (THESIS, OWN-WORLD, STORY, FIRST VIEWPORT, FORM). Future surfaces read it before adding anything.

**Key Characteristics:**
- Two-color world taken from the sign: forest green ground, cream boards.
- Condensed uppercase display type from the system stack; no web fonts.
- Rule lines frame headings on boards, as on the sign.
- The phone number is a display element, not a footnote.
- One signature hero animation plus ambient grass; nothing else moves.

## Colors

A sign-derived two-color world with a single warm accent borrowed from fresh-cut wood.

### Primary
- **Sign Green** (ground): the page ground and the ink on cream boards (same value as cream-ink). Also the theme-color and favicon field.
- **Board Cream** (cream): sign-board sections, solid buttons and form fields on green, and all primary text on green.

### Secondary
- **Sawdust** (sawdust): the only accent. Hover, focus outlines on green, field focus border with a 3px 35% glow, text selection. Never a fill at rest.

### Neutral
- **Deep Lawn** (ground-deep): recessed panel on green (the "text is ready" confirmation box).
- **Sage** (ink-soft): secondary text, optional-label text and unselected chip borders on green.
- **Board Moss** (ink-soft-cream): secondary paragraph text on cream boards.
- **Clay Pink** (error): validation messages and invalid field borders on green.

### Named Rules
**The Sign Colors Rule.** Green and cream carry every surface. The page ground is never black (PRODUCT.md brand commitment).

**The Sawdust Only Moves Rule.** Sawdust appears only in response to the visitor: hover, focus, selection. A surface at rest is green and cream.

## Typography

**Display Font:** system condensed stack (Arial Narrow, Helvetica Neue, sans-serif-condensed for Android, Roboto Condensed, then platform sans), with `font-stretch: condensed`.
**Body Font:** platform system sans (-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial).

**Character:** Sign-painter bluntness. The display face is whatever condensed sans the device already has, set heavy and uppercase; the body is the phone's own UI face so it reads like a text message.

### Hierarchy
- **Display** (900, clamp(42px, 12.5vw, 96px) on phones, clamp(56px, 6.2vw, 84px) at 860px+, 0.93, uppercase): the hero headline only. `text-wrap: balance`.
- **Headline** (900, clamp(32px, 8.6vw, 56px), 0.98, uppercase): section headings on boards and on the quote section.
- **Phone** (900, clamp(40px, 11vw, 76px), 1): the footer number, set between rule lines.
- **Wordmark / header number** (800, 17px, 15px under 380px, 21px at 860px+, display stack; wordmark uppercase with 0.04em tracking).
- **Title** (800, 21px, 1.2, body stack): step titles.
- **Body** (400, 17px, 1.55): all running text; measure held at 30-44ch.
- **Label** (700, 17px, 1.3): form labels, legends, chips, text links.
- **Small** (15px, 1.45): helper text, errors, the composed message preview.

### Named Rules
**The House Stack Rule.** The display face is a system condensed stack, including Android's `sans-serif-condensed`. This is the owner's house rule: no web fonts, no downloads. Do not "fix" it with a hosted face.

**The Uppercase Is for Display Rule.** Uppercase belongs to the condensed display face (headline, wordmark). Body, labels and buttons stay sentence case.

## Layout

Phone first, single column, gutter 20px (16px under 380px, 40px at 860px+), content capped at 1180px. One breakpoint does the real work at 860px: the hero splits into copy (1.15fr) and yard (0.95fr) with the yard bleeding to the right edge; steps go three across; the quote section becomes a sticky intro column (0.8fr) beside the form (1fr); the closing board puts copy and button side by side. Action pairs stack on phones and sit two-up on desktop, capped at 440-520px. Forms cap at 560px.

Sections alternate green lawn and cream boards: hero (green), how-it-works board (cream), quote (green), closing board (cream), footer (green). Boards carry 44px top / 92px bottom padding on phones (72 / 112 on desktop); the extra bottom room is where the grass edge grows.

## Elevation & Depth

Flat. No box shadows on surfaces. Depth exists only inside the canvases (the stump's cast shadow, chip shadows) and as the edge-fade masks on the yard canvas, which dissolve it into the green ground instead of boxing it. The single non-canvas shadow is the 3px sawdust focus glow (`0 0 0 3px rgba(227,169,91,.35)`), a state, not elevation.

### Named Rules
**The Planted Not Floating Rule.** Boards sit in the lawn; they are never lifted with shadows. Separation comes from the green/cream change and the grass edge.

## Shapes

Three shapes only: full pills for buttons (999px), gently rounded 12px rectangles for fields, chips and the confirmation panel, and full circles for step numerals. Boards themselves are full-bleed with square edges. Rule lines are 3px solid bars: cream-ink on boards, cream at 85% in the footer band. The stump-with-rings mark (inline SVG symbol) is the only icon-like brand shape; the message icon is a stroked inline SVG at 22px.

## Components

### Buttons
Big, thumb-sized, and direct.
- **Shape:** full pill (999px), 58px tall, 2px border, 800 weight 17px body stack, 22px icon gap 10px.
- **Solid (on green):** cream fill, green text. Hover goes sawdust fill and border.
- **Line (on green):** transparent with cream border and text. Hover turns border and text sawdust.
- **Solid on cream:** green fill, cream text.
- **Press:** scales to 0.98 (disabled under reduced motion). Focus: 3px sawdust outline offset 3px (green outline inside boards).
- **Text link button:** underlined 700 17px, 4px underline offset, 44px min height, sawdust on hover.

### Chips
- **Style:** radio chips, 50px tall, min 64px wide, 12px radius, 2px sage border, 700 17px.
- **State:** selected fills cream with green text; hover and keyboard focus show a sawdust border (focus adds the sawdust glow).

### Cards / Containers
- **Sign board:** full-bleed cream section, green ink, opened by a 3px rule; on the how-it-works board the headline sits between two rules, exactly like the sign's name panel.
- **Confirmation panel:** deep-lawn fill, 12px radius, 16px padding.
- **Step:** 52px green disc with a 900-weight 26px display numeral, beside a title and a body line in board moss.

### Inputs / Fields
- **Style:** cream fill, green text, 2px cream border, 12px radius, 14px padding, 54px min height (textarea 96px, vertical resize). Labels sit above in label style; "(optional)" in sage at 400.
- **Focus:** border turns sawdust plus 3px sawdust glow. Hover: sawdust border.
- **Error:** clay-pink border and a clay-pink 15px message beneath.

### Navigation
A bare header: wordmark (mark plus condensed uppercase name) left, the phone number right, both 44px tap targets. The number gains a 2px sawdust underline on hover. No menu.

### Footer Phone Band
The sign's bottom panel on the page: wordmark, the sign's own "Thank you for your business!" line (italic Georgia, 600, 21px, standing in for the sign's script), then the phone number in phone type flanked by two 3px cream rule bars (85% opacity) across up to 760px. Hover adds a 3px sawdust underline.

### Grass Edge (signature)
A 58px canvas that overlaps the bottom of every sign board by -58px, drawing blades with a 3px green base line. About 45% are darker back blades. Two sine winds at different speeds sway them; the pointer or finger within 70px parts them with spring physics (stiffness 38, damping 6.5, clamp 1.1). Tunables at the top of the script: `SWAY` (wind speed) and `PUSH` (how far a finger parts the grass).

### The Stump in the Lawn (signature hero)
A top-down canvas: a grass field of thousands of short blades, a stump with bark-collar root flares, growth rings, drying checks and a soft cast shadow. A spinning steel cutter wheel with carbide teeth and a yellow guard and boom follows the pointer (finger while pressed) and grinds the stump into soil through a cell mask, throwing wood chips that arc, land, and fade. When less than 15% of the stump is left, the lawn fades back over the spot, holds, and a fresh stump fades in. A half-ground stump settles back after a quiet spell, and after 6 idle seconds the grinder sweeps the stump by itself. A centred hint ("Drag across the stump" / "Move across the stump") fades on first touch. Tunables at the top of the script: `CELL`, `GRIND`, `REGROW_AFTER`, `REGROW`, `AUTO_AFTER`, `LAWN_AT`, `MAX_CHIPS_PHONE`, `MAX_CHIPS_DESK`.

### Motion Switch
Both scripts share one requestAnimationFrame loop that runs only while a canvas is on screen. `STILL = true` at the top of the shared loop (the older-audience switch) or `prefers-reduced-motion` freezes everything: one still frame of the whole stump and upright grass, no chips, no cutter, no auto-grind.

## Do's and Don'ts

### Do:
- **Do** build every surface from green and cream; reserve sawdust for hover, focus and selection.
- **Do** frame board headings with 3px rule lines, and set the phone number between rules at display size.
- **Do** end every cream board with a grass edge where it meets green.
- **Do** keep the display face on the system condensed stack, including `sans-serif-condensed`.
- **Do** keep primary controls at least 50px tall and every tap target at least 44px.
- **Do** expose new motion parameters as named constants at the top of the script, and honour `STILL` and reduced motion.

### Don't:
- **Don't** use a black or near-black page ground.
- **Don't** add web fonts or a hosted display face.
- **Don't** add motion beyond the hero stump and the grass edges.
- **Don't** lift boards or buttons with drop shadows.
- **Don't** set body, labels or buttons in uppercase.
