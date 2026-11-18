---
name: Kese
description: A deep green-black expense ledger with a faint grid, a coral glow, pill-shaped chrome, and one coral accent.
colors:
  coral: "#ff8f6b"
  coral-hover: "#ffa488"
  on-coral: "#2a0f06"
  ground: "#0a1412"
  panel: "#10201c"
  raised: "#17302a"
  line: "rgba(230,242,238,.13)"
  text: "#e6f2ee"
  muted: "#93aea6"
  ok: "#4fd1a1"
  warn: "#f2c14e"
  bad: "#ff7a7a"
  light-panel: "#eaf3ef"
  light-raised: "#dcebe5"
  light-field: "#ffffff"
  light-ink: "#0e1f1b"
  light-muted: "#4d6a62"
  light-line: "#c6dcd3"
typography:
  display:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "clamp(40px, 6vw, 84px)"
    fontWeight: 750
    lineHeight: 0.98
    letterSpacing: "-0.05em"
  headline:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "clamp(36px, 5vw, 58px)"
    fontWeight: 750
    lineHeight: 1
    letterSpacing: "-0.045em"
  figure:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "32px"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.035em"
  title:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontSize: "20px"
    fontWeight: 650
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Geist, system-ui, sans-serif"
    fontSize: "16.5px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "Geist, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 500
    lineHeight: 1.55
  data-caption:
    fontFamily: "Geist Mono, ui-monospace, monospace"
    fontSize: "11.5px"
    fontWeight: 500
    lineHeight: 1.55
    letterSpacing: "0.08em"
  accent-serif:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "1.08em"
    fontWeight: 400
    letterSpacing: "-0.02em"
rounded:
  bar: "3px"
  month-bar: "8px"
  control: "12px"
  panel: "20px"
  auth-card: "28px"
  pill: "999px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "16px"
  lg: "22px"
  xl: "56px"
components:
  button-default:
    backgroundColor: "{colors.raised}"
    textColor: "{colors.text}"
    rounded: "{rounded.pill}"
    padding: "10px 14px"
    height: "44px"
  button-primary:
    backgroundColor: "{colors.coral}"
    textColor: "{colors.on-coral}"
    rounded: "{rounded.pill}"
    padding: "10px 14px"
    height: "44px"
  button-primary-hover:
    backgroundColor: "{colors.coral-hover}"
  button-destructive:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    rounded: "{rounded.pill}"
    padding: "4px 14px"
    height: "34px"
  button-destructive-hover:
    textColor: "{colors.bad}"
  input:
    backgroundColor: "{colors.ground}"
    textColor: "{colors.text}"
    rounded: "{rounded.control}"
    padding: "10px 14px"
    height: "44px"
  input-light:
    backgroundColor: "{colors.light-field}"
    textColor: "{colors.light-ink}"
    rounded: "{rounded.control}"
    padding: "10px 14px"
    height: "44px"
  panel:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.text}"
    rounded: "{rounded.panel}"
    padding: "22px"
  panel-light:
    backgroundColor: "{colors.light-panel}"
    textColor: "{colors.light-ink}"
    rounded: "{rounded.panel}"
    padding: "22px"
  auth-card:
    backgroundColor: "{colors.light-panel}"
    textColor: "{colors.light-ink}"
    rounded: "{rounded.auth-card}"
    padding: "30px"
  pill-bar:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.text}"
    rounded: "{rounded.pill}"
    padding: "8px 10px 8px 16px"
  stat-card:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.text}"
    rounded: "{rounded.panel}"
    padding: "20px 22px"
  stat-card-lead:
    backgroundColor: "{colors.light-panel}"
    textColor: "{colors.light-ink}"
    rounded: "{rounded.panel}"
    padding: "20px 22px"
---

# Design System: Kese

## Overview

**Creative North Star: "The Night Ledger Under Coral Light"**

Kese is a personal expense book set on a deep green-black ground that carries a faint 64px grid and one soft coral glow from the top right, like a ledger page lit from a single lamp. Panels step lighter than the ground, controls and chrome are pills or softly rounded, and the one warm accent (coral) does all the calling to action. The language was chosen by the user as a "Kesene-style" direction; the build shows it consistently across the sign-in and app screens.

The system has two surface worlds. The default is dark: ground, panel, raised. A `.light` scope flips the same custom properties to a pale mint paper with white fields and green-black ink; it is used where the user writes or decides (the sign-in card, the add-expense panel) and for the lead stat card. Because the scope reassigns tokens rather than restyling components, any component works in either.

Colour is functional: coral for action, focus, the current month and the avatar; green/amber/red for status; and per-category hue, which the user's data produces, for dots, bars and pills. Money figures use tabular numerals and Bricolage Grotesque.

**Key Characteristics:**
- Green-black ground with a 64px hairline grid and one coral radial glow (fixed to the viewport).
- Surface ladder ground, panel, raised; a `.light` token scope for input surfaces.
- Pill geometry for chrome and buttons, 20px panels, 12px controls, 28px auth card.
- One accent (coral), with a dark on-accent (#2a0f06) for text on it.
- Destructive buttons stay quiet until hover or keyboard focus.
- Bricolage Grotesque display, one Instrument Serif italic accent word in the hero, Geist body, Geist Mono for table headers and small data captions.

## Colors

A cool green-black field with mint-tinted text, warmed by a single coral accent.

### Primary
- **Lamp Coral** ({colors.coral}): primary buttons, focus ring and input focus border, avatar, current-month bar, hero list bullets, the italic hero word, and the dashed underline on the lead stat figure. Hover lifts to {colors.coral-hover}. Text on coral is **Burnt Umber** ({colors.on-coral}).

### Neutral
- **Deep Green-Black** ({colors.ground}): page ground and dark input fill.
- **Pine Panel** ({colors.panel}): panels, stat cards, select option lists, and the pill bar at 72% opacity.
- **Raised Pine** ({colors.raised}): default buttons, tab track, table row hover, month bars and progress tracks.
- **Mint Mist** ({colors.text}): body text; **Sage Muted** ({colors.muted}): labels, secondary text, quiet buttons.
- **Mint Hairline** ({colors.line}): every 1px border on dark surfaces.
- **Light scope**: **Mint Paper** ({colors.light-panel}) panel, {colors.light-raised} raised, {colors.light-field} fields, **Green Ink** ({colors.light-ink}) text, {colors.light-muted} muted, {colors.light-line} hairline. The selected auth tab inverts to ink on {colors.light-ink} with {colors.text} text.

### Status
- **Mint OK** ({colors.ok}), **Amber Warn** ({colors.warn}), **Coral Red Bad** ({colors.bad}). Bad is used for over-budget amounts and bars and for delete hover.

### Named Rules
**The One Lamp Rule.** Coral is the only accent. It means act, focus, or "now". It is never a category colour and never a status.

**The Colour-Is-Data Rule.** Beyond the accent and the status trio, hue appears only as a category colour or income-class colour that the data supplies. Category pills are the hue at 20% over transparent with normal text colour; the hue identifies, it never carries the text.

**The Light-Scope Rule.** Switch to light by adding the `.light` scope, never by hard-coding pale colours on a dark component. Reserve it for input surfaces and the single lead stat.

## Typography

**Display Font:** Bricolage Grotesque (with system-ui, sans-serif)
**Body Font:** Geist (with system-ui, sans-serif)
**Label/Mono Font:** Geist Mono (with ui-monospace, monospace)
**Accent Font:** Instrument Serif italic (with Georgia, serif)

**Character:** A tight, heavy grotesque for headings and figures against a neutral workmanlike body, with one literary italic word as a moment of voice.

### Hierarchy
- **Display** (750, clamp(40px, 6vw, 84px), 0.98, -0.05em): auth hero headline only.
- **Headline** (750, clamp(36px, 5vw, 58px), 1, -0.045em): the app screen title.
- **Figure** (700, 32px, 1.1, -0.035em): stat values; tabular numerals.
- **Title** (650, 20px, -0.02em): panel headings; the brand name is 750 at 20px with -0.03em.
- **Body** (400, 16.5px, 1.55): default text; hero paragraph 17px at max 470px; secondary text 14px in Sage Muted.
- **Label** (500, 14px): field labels above inputs, in Sage Muted; buttons are 600.
- **Data caption** (Geist Mono 500, 11.5px, 0.08em, uppercase): table column headers and stat captions. Month-bar labels are Geist Mono 12px, not uppercase.

### Named Rules
**The One Italic Rule.** Instrument Serif italic appears once per screen, on the single accent word of the hero headline, at 1.08em in coral. It is not used for body, labels, or other headings.

**The Tabular Rule.** Every amount, count and percentage uses tabular numerals and right-aligns in tables.

## Layout

A centered column, max 1180px for the app (1240px for auth) with 20px side padding. The app is a pill bar, a title row, a responsive stat strip (auto-fit, minimum 200px, 12px gap), then a two-column workspace: a 300-390px form column and a flexible data column, 16px gap, stacking below 900px. Auth is a 1.1fr/1fr split with a 56px gap that stacks below 900px. Rhythm is 8/12/16/22px; panel padding 22px, form gap 14px, field label gap 6px. The page background (grid plus glow) is fixed to the viewport.

## Elevation & Depth

Tonal layering with hairlines: depth comes from the ground, panel, raised steps and the 1px Mint Hairline, plus the faint grid and one radial coral glow in the page background. There are no box shadows on surfaces. The only glow is the input focus ring (`0 0 0 3px rgba(255,143,107,.25)`).

### Named Rules
**The Flat-Surface Rule.** Panels and cards carry no shadow. Hover is a border or fill change; the primary button also lifts 1px.

## Shapes

Pills for anything you tap in the chrome: buttons, tabs, language select, month input, user chip, toast, category pill, pill bar (999px). Controls such as inputs and selects are 12px; panels and stat cards 20px; the sign-in card 28px. Small data forms are 3px progress tracks, 8px month bars, and a 16px fully rounded segmented income bar. Borders are always 1px hairlines; the lead stat uses a 2px dashed coral underline on its figure.

## Components

### Buttons
- **Shape:** full pill (999px), 44px minimum height, 10px 14px padding, weight 600.
- **Primary:** coral fill, Burnt Umber text, weight 700, full width; one per form. Hover lightens and lifts 1px.
- **Default:** Raised Pine fill, hairline border; hover turns the border coral.
- **Destructive:** transparent, Sage Muted, 34px tall, 14px text; hover and focus-visible turn text and border Coral Red Bad.
- **Focus:** 2px coral outline with 2px offset on every `:focus-visible`.

### Inputs / Fields
- **Style:** 12px radius, hairline border, 44px tall. On dark panels the fill is the ground; inside `.light` it is white with green ink.
- **Focus:** coral border plus the 3px coral 25% halo.

### Cards / Containers
- **Panel:** Pine Panel, hairline, 20px radius, 22px padding, h2 title at 20px. The add-expense panel is `.light`.
- **Sign-in card:** `.light`, 28px radius, 30px padding, max 460px, right-aligned in the split.
- **Stat strip:** panel-coloured cards with a Geist Mono caption and a Figure value. The first card is `.light`-coloured with a 2px dashed coral underline on its figure.

### Navigation
- **Pill bar:** full pill, hairline, Pine at 72%, 8px 10px 8px 16px padding; holds logo and name on the left, tools (language select, CSV, user chip, sign out) on the right. Used identically on auth and app screens.
- **Tabs:** two-segment pill track on Raised; the selected tab fills Green Ink with Mint Mist text.

### Category pill and progress
- **Pill:** hue at 20% tint, 2px 12px padding, 14px text. **Dot:** 10px circle. **Progress:** 6px track on Raised, fill in category hue or Coral Red Bad when over budget.

### Income class box
- 12px-radius box with a 1px border and a bold Bricolage 20px heading, both in the class colour. Class colours are data-driven values set in the script (extreme `#ff7b72`, poor `#e3b341`, lower-middle `#58a6ff`, middle `#7ee787`, upper-middle `#56d4dd`, affluent `#d2a8ff`); the segmented income bar reuses the first four.

### Category palette
- Defaults assigned to new accounts: `#7cc4ff`, `#4fd1a1`, `#f2c14e`, `#5ad6e0`, `#ff8f6b`, `#f58ac0`, `#b9a3ff`, `#93aea6`. The user can choose any colour.

## Do's and Don'ts

### Do:
- **Do** step surfaces ground, panel, raised and edge everything with the 1px Mint Hairline.
- **Do** use the `.light` scope for fields the user writes into and for one lead stat.
- **Do** keep chrome and buttons fully pill-shaped, panels at 20px, controls at 12px.
- **Do** keep destructive buttons quiet until hover or keyboard focus.
- **Do** use tabular numerals and right alignment for amounts, formatted by the user's locale and currency.
- **Do** keep a 44px minimum control height and the coral focus treatment on every interactive element.

### Don't:
- **Don't** use coral for status or category decoration; it means act, focus, or now.
- **Don't** put coloured text on a category tint; pill text stays normal.
- **Don't** add surface drop shadows; depth is tonal.
- **Don't** use Instrument Serif or Geist Mono outside their recorded roles.
- **Don't** hard-code pale surfaces on dark components; use the `.light` scope.
