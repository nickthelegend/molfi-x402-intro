---
# MOLFI.FUN — frame.md (video-first companion to design.md)
# Atoms are sacred · composition is free · numbers come from the script.

colors:
  # Brand Gradients & Accents
  brand-purple: "#7c3aed"
  brand-purple-light: "#a855f7"
  brand-purple-dark: "#5b21b6"
  brand-purple-glow: "rgba(124, 58, 237, 0.35)"
  brand-purple-subtle: "rgba(124, 58, 237, 0.08)"

  # Background Shades
  bg-base: "#05050d"
  bg-surface: "#0d0d1a"
  bg-elevated: "#12122a"
  bg-card: "rgba(18, 18, 42, 0.7)"

  # Text
  text-primary: "#f0f0ff"
  text-secondary: "#a0a0c0"
  text-muted: "#606080"
  text-code: "#c4b5fd"

  # Borders & Dividers
  border-subtle: "rgba(124, 58, 237, 0.15)"
  border-strong: "rgba(124, 58, 237, 0.35)"

  # Semantics
  success: "#10b981"
  warning: "#f59e0b"
  danger: "#ef4444"
  info: "#3b82f6"

typography:
  # ── Reading ramp (carried from design.md, given cqw equivalents @ 1920) ──
  body-base:
    fontFamily: "Inter"
    fontWeight: 400
    fontSize: "16px"   # ≈0.83cqw — chrome floor only, never load-bearing
    lineHeight: 1.55
  body-lg:
    fontFamily: "Inter"
    fontWeight: 500
    fontSize: "20px"   # ≈1.04cqw
    lineHeight: 1.5
  label-eyebrow:
    fontFamily: "Outfit"
    fontWeight: 800
    fontSize: "22px"   # ≈1.15cqw
    letterSpacing: "0.22em"
    textTransform: "uppercase"
  caption-mono:
    fontFamily: "JetBrains Mono"
    fontWeight: 500
    fontSize: "18px"   # ≈0.94cqw
    letterSpacing: "0.04em"

  # ── Display / hero ramp (frame-native; sized in cqw) ──
  wordmark-mega:
    fontFamily: "Outfit"
    fontWeight: 900
    fontSize: "27cqw"      # MOLFI.FUN cover lockup
    lineHeight: 0.84
    letterSpacing: "-0.06em"
  display-hero:
    fontFamily: "Outfit"
    fontWeight: 900
    fontSize: "14cqw"      # ≤3-word oversized claims
    lineHeight: 0.86
    letterSpacing: "-0.045em"
  display-step-2:
    fontFamily: "Outfit"
    fontWeight: 800
    fontSize: "9.5cqw"     # 4–6 word claims
    lineHeight: 0.92
    letterSpacing: "-0.035em"
  display-step-3:
    fontFamily: "Outfit"
    fontWeight: 800
    fontSize: "6.2cqw"     # 7+ word claims / section heads
    lineHeight: 1.0
    letterSpacing: "-0.02em"
  stat-mega:
    fontFamily: "Outfit"
    fontWeight: 900
    fontSize: "16cqw"      # focal-artifact stat figure
    lineHeight: 0.88
    letterSpacing: "-0.05em"
  stat-ledger:
    fontFamily: "Outfit"
    fontWeight: 800
    fontSize: "2.6cqw"     # dense ledger cells
    lineHeight: 1.0
    letterSpacing: "-0.01em"
  hash-mono-hero:
    fontFamily: "JetBrains Mono"
    fontWeight: 500
    fontSize: "2.2cqw"     # hero hash printouts
    lineHeight: 1.2
    letterSpacing: "0.02em"
  pill-giant-label:
    fontFamily: "Outfit"
    fontWeight: 800
    fontSize: "1.6cqw"
    letterSpacing: "0.22em"
    textTransform: "uppercase"

rounded:
  pill: "999px"
  card: "16px"
  card-lg: "24px"
  chip: "8px"
  hairline: "2px"

spacing:
  hair: "2px"
  xs: "8px"
  sm: "12px"
  md: "20px"
  lg: "32px"
  xl: "56px"
  frame-pad: "5cqw"          # safe inset from frame edge
  frame-pad-tight: "3.2cqw"  # dense/ledger plates only

components:
  # ── Pulse badge (the brand-signature AVALANCHE FUJI · x402 marker) ──
  pulse-badge:
    backgroundColor: "{colors.brand-purple-subtle}"
    borderColor: "{colors.border-strong}"
    textColor: "{colors.text-primary}"
    accentDot: "{colors.brand-purple-light}"
    typography: "{typography.pill-giant-label}"
    rounded: "{rounded.pill}"
    padding: "0.9cqw 2.2cqw"
  pulse-badge-giant:
    extends: "{components.pulse-badge}"
    typography: "{typography.label-eyebrow}"
    padding: "1.4cqw 3cqw"

  # ── Primary CTAs ──
  button-primary:
    background: "linear-gradient(135deg, {colors.brand-purple-light} 0%, {colors.brand-purple} 55%, {colors.brand-purple-dark} 100%)"
    textColor: "{colors.text-primary}"
    typography: "{typography.label-eyebrow}"
    rounded: "{rounded.pill}"
    padding: "1.1cqw 2.6cqw"
    glow: "0 0 6cqw {colors.brand-purple-glow}"
  button-primary-giant:
    extends: "{components.button-primary}"
    padding: "1.8cqw 4.4cqw"
    typography:
      fontFamily: "Outfit"
      fontWeight: 900
      fontSize: "2.2cqw"
      letterSpacing: "0.16em"
      textTransform: "uppercase"
  button-ghost:
    backgroundColor: "transparent"
    borderColor: "{colors.border-strong}"
    textColor: "{colors.text-primary}"
    typography: "{typography.label-eyebrow}"
    rounded: "{rounded.pill}"
    padding: "1.1cqw 2.6cqw"

  # ── Surfaces ──
  card-glass:
    backgroundColor: "{colors.bg-card}"
    borderColor: "{colors.border-subtle}"
    backdropFilter: "blur(18px)"
    rounded: "{rounded.card-lg}"
    padding: "2.4cqw"
    glow: "inset 0 0 0 1px {colors.border-subtle}, 0 1.4cqw 4cqw rgba(0,0,0,0.55)"
  card-elevated:
    backgroundColor: "{colors.bg-elevated}"
    borderColor: "{colors.border-subtle}"
    rounded: "{rounded.card-lg}"
    padding: "2cqw"

  # ── Ledger / dashboard primitives ──
  ledger-row:
    backgroundColor: "transparent"
    borderColor: "{colors.border-subtle}"
    textColor: "{colors.text-secondary}"
    typography: "{typography.caption-mono}"
    padding: "1.1cqw 1.4cqw"
    rounded: "0"
  ledger-cell-figure:
    textColor: "{colors.text-primary}"
    typography: "{typography.stat-ledger}"
  ledger-cell-hash:
    textColor: "{colors.text-code}"
    typography: "{typography.hash-mono-hero}"

  # ── Status chips ──
  status-pill-success:
    backgroundColor: "rgba(16,185,129,0.12)"
    borderColor: "{colors.success}"
    textColor: "{colors.success}"
    typography: "{typography.pill-giant-label}"
    rounded: "{rounded.pill}"
    padding: "0.6cqw 1.4cqw"
  status-pill-pending:
    backgroundColor: "rgba(245,158,11,0.12)"
    borderColor: "{colors.warning}"
    textColor: "{colors.warning}"
    typography: "{typography.pill-giant-label}"
    rounded: "{rounded.pill}"
    padding: "0.6cqw 1.4cqw"
  status-pill-danger:
    backgroundColor: "rgba(239,68,68,0.12)"
    borderColor: "{colors.danger}"
    textColor: "{colors.danger}"
    typography: "{typography.pill-giant-label}"
    rounded: "{rounded.pill}"
    padding: "0.6cqw 1.4cqw"

  # ── Code / hash printout ──
  hash-block:
    backgroundColor: "{colors.bg-surface}"
    borderColor: "{colors.border-subtle}"
    textColor: "{colors.text-code}"
    typography: "{typography.hash-mono-hero}"
    rounded: "{rounded.chip}"
    padding: "1.6cqw 2cqw"

  # ── Catalog tile (model comparison) ──
  catalog-tile:
    backgroundColor: "{colors.bg-surface}"
    borderColor: "{colors.border-subtle}"
    textColor: "{colors.text-primary}"
    typography: "{typography.body-lg}"
    rounded: "{rounded.card-lg}"
    padding: "2.2cqw"

  # ── Dot-grid ground (the brand's signature background) ──
  dot-grid-ground:
    backgroundColor: "{colors.bg-base}"
    dotColor: "{colors.border-subtle}"
    dotSize: "2px"
    dotSpacing: "2.4cqw"

  # ── Glow ring (focal artifact halo) ──
  glow-ring:
    color: "{colors.brand-purple-glow}"
    blur: "10cqw"
    spread: "1.2cqw"
---

# frame.md — MOLFI.FUN at frame scale

> **Atoms are sacred · composition is free · numbers come from the script.**

This document sits beside `design.md`. The web spec stays authoritative for the product
surfaces; this layer reframes the same brand so the **frame** (1920×1080 by default) is the
unit. Atoms — every hex, weight, radius, font — are copied verbatim. Composition is reframed
for video: dark grounds, oversized Outfit display, a single glowing accent, mono ledgers and
hashes that read at frame scale.

## Overview

MOLFI.FUN is a near-black, neon-purple, glassmorphic crypto-payment brand. At product scale it
reads as a dense Web3 console; at **frame scale** it must read as a state-of-the-art keynote —
deep space ground, one screaming Outfit lockup or stat, one ration of purple voltage, with mono
hashes and ledger figures as the secondary register. The dot-grid is the brand's signature
ground; the gradient pill is the brand's signature CTA; the glowing pulse badge
(`AVALANCHE FUJI · x402`) is the brand's signature marker. Everything else is silence.

### Frame Craft Bar

- **Squint test** — one focal element dominates at **3–6×** its nearest neighbor. A glowing
  wordmark with a tiny pulse badge below. A `$1,284` figure with a hairline label rail. Never a
  ramp of similar weights.
- **Silence test** — sparse plates (cover, oversized-claim, focal-artifact, hash-closer) read
  **55–75% empty**. The deep `bg-base` ground IS the design. The **`data-ledger` plate is the
  one named density exception** — its job is to look like an audit.
- **Restraint test** — the brand's scarce element is the **gradient purple voltage** (the
  pill, the glow halo, the badge dot). It fires **once per frame**, full strength. A second
  purple element appears only as `border-subtle` or `text-code` — never as a second glow.
- **Reference bar** — aim at a **Stripe Sessions keynote frame** rendered in deep violet, or
  an **Arc / Linear launch plate**. Failure looks like a generic Web3 landing-page screenshot
  with stacked feature cards.

## Colors

Tokens are unchanged from `design.md`. At frame scale their roles harden:

- **Grounds.** Every frame opens on `{colors.bg-base} #05050d`. `{colors.bg-surface}` is the
  card / hash-block surface. `{colors.bg-elevated}` lifts a single focal artifact when a glass
  card isn't right. `{colors.bg-card}` is reserved for glassmorphic floats over a dot-grid.
- **The voltage.** `{colors.brand-purple}` and `{colors.brand-purple-light}` exist as the
  **single accent voltage per frame**, almost always as a gradient pill, a glow halo, or a
  one-word emphasis. `{colors.brand-purple-glow}` is the *halo*, never a fill.
  `{colors.brand-purple-subtle}` is allowed as a pulse-badge tint or a long divider wash.
- **Text.** `{colors.text-primary}` carries every load-bearing display line. `text-secondary`
  is the body register; `text-muted` is for timestamps and index chips only and **may never
  carry a beat's meaning** at frame scale. `{colors.text-code}` is reserved for hashes,
  addresses, contract IDs — never prose.
- **Semantics.** `success` / `warning` / `danger` / `info` appear only inside status pills or
  ledger figures. They never become a frame ground.
- **Accent rule.** Purple voltage and a semantic color may not share a frame at full strength.
  A `success` pill in a ledger frame forces the purple to demote to `border-subtle`.

## Typography

Two ramps live in the frontmatter. Use them as authored.

- **Reading ramp** — `body-base` / `body-lg` / `label-eyebrow` / `caption-mono`. These exist
  for the dense `data-ledger` plate and for chrome labels. `body-base` at 16px ≈ 0.83cqw is
  **below the legibility floor** and is chrome-only; nothing load-bearing lives there.
- **Display / hero ramp** — `wordmark-mega` (cover), `display-hero` (≤3 words),
  `display-step-2` (4–6 words), `display-step-3` (7+ words / section heads), `stat-mega`,
  `stat-ledger`, `hash-mono-hero`, `pill-giant-label`. **Fit-to-measure**: a headline's size
  is a function of its word count via the stepped ramp, never a fixed token across all frames.
- **Legibility floor** — any load-bearing line ≥ **1.4cqw (≈27px @ 1920)**.
- **Family discipline** — Outfit 800/900 for display and pills; Inter for prose; JetBrains
  Mono **only** for hashes, addresses, transaction IDs. A mono line of prose is a brand fail.
- **Headline measure** — text block ≤ **78cqw** wide; long lines step down the ramp.

## Layout — The Frame

- **Primary canvas** — `1920 × 1080` (16:9). Conversions: `px ÷ 1920 × 100 = cqw`.
- **Secondary canvases** — `1080 × 1920` (9:16) and `1080 × 1080` (1:1). See Aspect-Ratio
  Behavior.
- **Safe area** — inset every frame by `{spacing.frame-pad}` (5cqw) on all four sides. Dense
  ledger plates may use `{spacing.frame-pad-tight}` (3.2cqw).
- **The vw / cqw law.** In `frame.md` all frame-relative sizes are written in `cqw` (the spec
  treats this as a string-stored extension). In a showcase or contact sheet the same number
  resolves against the **frame container** (`container-type: size`), not the viewport — that
  is how frames stay calm at any display size. If a downstream renderer cannot do container
  queries, `vw` is the substitute and the frame must own the viewport.

## Elevation & Depth

The depth ceiling for video is shallower than the product. Allowed:

- a **glassmorphic float** (`card-glass`) over a dot-grid ground — one per frame max;
- a single **purple glow halo** behind a focal artifact (the `glow-ring` token);
- **`bg-elevated`** for a card lifted off `bg-surface`.

Banned at frame scale: drop shadows on text, layered cards (two glass cards stacked), inner
shadow chrome, fake bevels, more than one glow per frame.

## Shapes

- Pills are perfect capsules (`{rounded.pill}` 999px). Outfit weight 800/900 fits the capsule.
- Cards: `{rounded.card-lg}` 24px for hero artifacts, `{rounded.card}` 16px for catalog tiles.
- Chips / hash blocks: `{rounded.chip}` 8px.
- **Hairlines** are `{rounded.hairline}` 2px and only ever rendered in `border-subtle` or
  `border-strong`. No 1px chrome — at frame scale it vanishes.

## Components

The frontmatter `components:` block is the normative layer. Prose below is intent only.

- **`{components.pulse-badge}` / `{components.pulse-badge-giant}`** — the brand-signature
  marker (`AVALANCHE FUJI · x402` is the canonical example, but the badge is the *form*, the
  string varies). Use one per frame at most. The dot is `brand-purple-light` and is the only
  place the voltage appears at the chrome scale.
- **`{components.button-primary}` / `{components.button-primary-giant}`** — the gradient pill
  is the brand's CTA voice. The giant variant is for hero / closer plates where the CTA *is*
  the focal element. Never two CTAs side by side at frame scale — second action demotes to
  `{components.button-ghost}`.
- **`{components.card-glass}`** — glassmorphic float; requires a textured ground beneath (the
  dot-grid). On a flat `bg-base`, glass reads as a flat card and the effect is wasted.
- **`{components.card-elevated}`** — opaque lifted card; preferred for focal-artifact plates
  where the artifact must read crisp without glass blur.
- **`{components.ledger-row}` + `{components.ledger-cell-figure}` + `{components.ledger-cell-hash}`**
  — composed grid for the data-ledger plate. Rows are hairline-divided; the figure column uses
  `stat-ledger`, the hash column uses `hash-mono-hero` at `text-code`.
- **`{components.status-pill-success|pending|danger}`** — the only place the semantic colors
  reach a viewer at frame scale.
- **`{components.hash-block}`** — full-width contract / tx-hash printout. Used on the closer
  plate as proof.
- **`{components.catalog-tile}`** — model comparison tile. Two-up only; never three.
- **`{components.dot-grid-ground}`** — the signature ground for cover and brand-signature
  plates. Constructed as a CSS radial-gradient pattern (the property-token set cannot hold the
  background-image; the showcase CSS holds it).
- **`{components.glow-ring}`** — a halo placed *behind* a focal artifact via a large blurred
  box-shadow. Not a fill; not a border.

## Motion & Timing

Derived from the brand's "alive but premium" character. Cuts are the grammar; motion is the
seasoning.

- **Cut grammar** — straight cuts on the beat. Cross-dissolves only between two frames that
  share a ground (cover → oversized-claim, both on dot-grid).
- **May animate** — a single dasharray flow along a hairline (echoes the EIP-3009 diagram); a
  glow-halo opacity pulse (0.6 → 1.0) on a focal artifact; a status-pill dot pulse.
- **Must not animate** — wordmark scale-in, headline letter-spacing wobble, card kenburns, any
  parallax. The brand reads as *engineered*, not theatrical.
- **Dwell** — sparse plates hold longer than they feel they should; dense ledger plates need
  active reading time. Density drives pace through element count, not through prescribed
  seconds.
- **Export** — sRGB; deliver at native canvas resolution; never upscale.

## Frame Treatments

### 1 · MOLFI.FUN Cover Lockup  (identity/cover · move: wordmark-as-architecture)
**Ground** `{components.dot-grid-ground}`, padding: `{spacing.frame-pad}`.
**Container** flex column, items center, justify center, gap `2.4cqw`.
**Composes** `{components.pulse-badge-giant}`, `{components.dot-grid-ground}`.
**Focal** wordmark `MOLFI.FUN` typeset in `{typography.wordmark-mega}` at `{colors.text-primary}`, centered.
**Chrome** `{components.pulse-badge-giant}` placed `2.4cqw` below the wordmark baseline, centered.
**Accent** the gradient on the wordmark's `.FUN` suffix uses `{colors.brand-purple-light}` → `{colors.brand-purple}` clipped to text. Single voltage.
**Silence** ~65% empty above and below the lockup; dot-grid carries the rest.
**Fixed** wordmark glyph set; Outfit 900; centered anchor.  **Free** the badge string (network · protocol).
**Density** sparse.

### 2 · Oversized Claim  (editorial/oversized-claim · move: three-word screamer)
**Ground** `{colors.bg-base}` flat (no dot-grid — the claim is the texture), padding: `{spacing.frame-pad}`.
**Container** flex column, items flex-start, justify center; text block max-width `78cqw`.
**Composes** `{components.pulse-badge}` (small, top-left rail), display-hero text.
**Focal** ≤3-word headline at `{typography.display-hero}`, `{colors.text-primary}`, with **exactly one word** rendered in a `{colors.brand-purple-light}` → `{colors.brand-purple}` text-clip gradient.
**Chrome** `{components.pulse-badge}` at the top-left of the safe area as an eyebrow rail (used here because the headline is full-bleed and the kicker rations cleanly).
**Accent** one word, one gradient.
**Silence** ~58% empty; the bottom-right quadrant is intentionally dead space.
**Fixed** display-hero ramp; one-word gradient rule.  **Free** the three-word string.
**Density** sparse.

### 3 · Focal Artifact — Glow Stat  (focal-artifact · move: figure-on-halo)
**Ground** `{colors.bg-base}`, padding: `{spacing.frame-pad}`.
**Container** grid 1×1, center; one halo behind one figure.
**Composes** `{components.glow-ring}`, `{components.pulse-badge}` (label rail), `{components.status-pill-success}` (optional anchor).
**Focal** stat figure in `{typography.stat-mega}` at `{colors.text-primary}`, centered, sitting on a `{components.glow-ring}` halo (`brand-purple-glow`).
**Chrome** `{typography.label-eyebrow}` caption rail `2cqw` above the figure (`text-secondary`); `{components.status-pill-success}` `2cqw` below if the script names a confirmed state.
**Accent** the halo only.
**Silence** ~70% empty.
**Fixed** halo geometry; single figure.  **Free** the figure itself (from the script), the caption string, presence/absence of the status pill.
**Density** sparse.

### 4 · Avalanche Fuji Ledger  (data/ledger · move: audit-as-frame · DENSITY EXCEPTION)
**Ground** `{colors.bg-surface}`, padding: `{spacing.frame-pad-tight}`.
**Container** grid; left = section head + label rail (`28cqw` wide); right = `{components.ledger-row}` × 5–7, hairline-divided.
**Composes** `{components.ledger-row}`, `{components.ledger-cell-figure}`, `{components.ledger-cell-hash}`, `{components.status-pill-success}`, `{components.status-pill-pending}`.
**Focal** the whole table — there is no single hero element; the **density itself is the focal move**.
**Chrome** left rail: section title in `{typography.display-step-3}` (`text-primary`) + `{typography.caption-mono}` sublabel (`text-muted`).
**Accent** a single `{components.status-pill-success}` on the most recent row.
**Silence** tight by design — the named density exception.
**Fixed** hairline column geometry; mono in the hash column; Outfit-800 in the figure column.  **Free** every row value (from the script — never invent figures).
**Density** dense-exception.

### 5 · Two-Up Catalog  (chrome/catalog · move: side-by-side comparison)
**Ground** `{colors.bg-base}`, padding: `{spacing.frame-pad}`.
**Container** flex row, gap `3cqw`; two `{components.catalog-tile}` of equal width; section head spans both, anchored top-left.
**Composes** `{components.catalog-tile}` × 2, `{typography.display-step-3}` head.
**Focal** the **pair**, read as one composition. Each tile carries an Outfit-800 title (`display-step-3`) and 2–3 `body-lg` lines.
**Chrome** a thin `{colors.border-strong}` rule under the section head spanning both tiles.
**Accent** one tile carries a `{components.pulse-badge}` in the top-right corner marking the recommended option; the other does not.
**Silence** ~45% empty — the most populous sparse plate; never a third tile.
**Fixed** two tiles only; equal width; one badge between them.  **Free** the titles and the body lines.
**Density** standard.

### 6 · Pulse Badge Hero  (brand-signature · move: badge-as-monument)
**Ground** `{components.dot-grid-ground}`, padding: `{spacing.frame-pad}`.
**Container** flex column, items center, justify center.
**Composes** `{components.pulse-badge-giant}` scaled up, `{components.glow-ring}` behind it, single-line caption.
**Focal** a single `{components.pulse-badge-giant}` enlarged to ~`42cqw` wide, centered on a `{components.glow-ring}` halo. The dot pulses; the rest is still.
**Chrome** one caption line in `{typography.display-step-3}` (`text-primary`), `4cqw` below the badge, centered, ≤5 words.
**Accent** the dot.
**Silence** ~65% empty.
**Fixed** badge geometry + dot; halo color.  **Free** the badge string (network · protocol pair) and the caption.
**Density** sparse.

### 7 · Hash Block Closer  (focal-artifact/closer · move: proof-as-payoff)
**Ground** `{colors.bg-base}`, padding: `{spacing.frame-pad}`.
**Container** flex column, items center, justify center, gap `2cqw`.
**Composes** `{components.status-pill-success}`, `{components.hash-block}`, `{components.button-primary-giant}` (optional).
**Focal** `{components.hash-block}` centered, ~`68cqw` wide, carrying a single contract or tx hash in `{typography.hash-mono-hero}` (`text-code`).
**Chrome** `{components.status-pill-success}` `2cqw` above the hash block, label `SETTLED`. Optional CTA `{components.button-primary-giant}` `3cqw` below for a closer beat.
**Accent** the gradient pill IS the voltage when present; otherwise the green status pill carries it alone.
**Silence** ~60% empty.
**Fixed** mono in the hash; success pill above.  **Free** the hash string itself (from the script — never invent), CTA presence/copy.
**Density** sparse.

### 8 · Glass Composer  (focal-artifact · move: glass-on-grid)
**Ground** `{components.dot-grid-ground}`, padding: `{spacing.frame-pad}`.
**Container** grid 1×1, center; `{components.card-glass}` floats centered at ~`62cqw` wide × ~`38cqw` tall.
**Composes** `{components.card-glass}`, `{components.button-primary}`, `{components.button-ghost}`, `{components.pulse-badge}`.
**Focal** the glass card. Inside: top-left `{components.pulse-badge}`, a `display-step-3` headline (≤6 words), one `body-lg` line of explanation, and a button row (`{components.button-primary}` + `{components.button-ghost}`).
**Chrome** none outside the glass — the grid ground is the silence.
**Accent** the gradient on `{components.button-primary}`.
**Silence** ~50% empty around the card.
**Fixed** glassmorphic float on dot-grid; one primary + one ghost button.  **Free** badge string, headline, body line.
**Density** standard.

## Do's and Don'ts

- **Do** start every frame on `{colors.bg-base}` or `{components.dot-grid-ground}`.
- **Do** lean centered. Cover, oversized-claim, focal-artifact, pulse-badge-hero, hash-closer
  all center their focal element. Reserve left-anchor for the **ledger** and **catalog**
  plates only. No more than 2 consecutive frames share an anchor.
- **Do** vary composition axis between consecutive frames — never run two ledger plates in a
  row, never two oversized-claims back-to-back.
- **Do** keep one idea per frame, ≤ 2–3 distinct elements (focal + at most one kicker + one
  support). Two things → two frames.
- **Do** bleed the dot-grid ground edge-to-edge; never inset it inside a card.
- **Do** size headlines to the line via the stepped ramp (≤3 → hero, 4–6 → step-2, 7+ → step-3).
- **Don't** put two purple voltages on one frame. The pill and a glow halo never coexist at
  full strength.
- **Don't** wrap a hash. If it doesn't fit, truncate with `…` mid-string in mono.
- **Don't** use Outfit on prose, Inter on a hash, or Mono on a headline.
- **Don't** stack two glass cards; glass is solo.
- **Don't** let any decorative element overlap the headline bounding box or the eyebrow rail
  (≥ 2cqw keep-out).
- **Don't** drop a load-bearing line below 1.4cqw.
- **Don't** invent figures, hashes, addresses, network names, or product strings. Atoms are
  sacred; **numbers come from the script.**

## Aspect-Ratio Behavior

| Treatment              | 16:9 (primary)                          | 9:16                                                                          | 1:1                                                              |
|------------------------|-----------------------------------------|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1 · Cover Lockup       | wordmark at `wordmark-mega` 27cqw       | wordmark steps to `display-hero` 14cqw stacked over `MOLFI` / `.FUN` two-line | wordmark at `display-hero` 14cqw single line                     |
| 2 · Oversized Claim    | 3-word hero, left-anchored              | claim re-steps down (step-2 / step-3 by line count); reflows to 4–5 lines     | claim caps at 4–6 words; center-anchored                         |
| 3 · Glow Stat          | figure at `stat-mega` 16cqw centered    | figure at 22cqw; caption rail collapses to 2 lines below                      | figure at 18cqw; status pill drops if present                    |
| 4 · Fuji Ledger        | left rail + right table                 | rail collapses above table; rows show 4 cells, hash truncates                 | 4 rows; figure + hash columns only; status column drops          |
| 5 · Two-Up Catalog     | side-by-side                            | re-stacks vertically; recommended tile on top                                 | re-stacks vertically; section head shrinks to `display-step-3` 8cqw |
| 6 · Pulse Badge Hero   | badge ~42cqw wide, caption below        | badge ~62cqw wide; caption wraps to 2 lines                                   | badge ~58cqw wide; caption single line                           |
| 7 · Hash Block Closer  | hash block ~68cqw wide                  | hash block ~86cqw wide; hash truncates mid-string                             | hash block ~78cqw; CTA drops                                     |
| 8 · Glass Composer     | glass card ~62cqw × ~38cqw              | card re-stacks portrait, full safe-width; buttons stack                       | card ~78cqw square; ghost button drops                           |

A re-scale never drops a load-bearing line below the **1.4cqw** floor; if it would, the line
truncates or the element drops per the rules above.

## Approved Real Entities & Numerals

Only the following may appear as literal copy in any frame, drawn from `design.md`:

- Product / domain names: **MOLFI.FUN**, `molfi-frontend`, `molfi-marketers`, `molfi-landing`,
  `molfi-docs`.
- Network / protocol strings: **AVALANCHE FUJI**, **x402**, **EIP-3009**, **EIP-4361**,
  **SIWE**, **USDC**.
- Surface concept labels lifted verbatim: *Composer Window*, *Ad Playback Overlay*, *SIWE
  Login Screen*, *Dashboard Console*, *Billing Center*, *Public Verification Page*.
- Font names where typography is the subject: **Outfit**, **Inter**, **JetBrains Mono**.

**Never invented** in a frame: dollar amounts, USDC balances, viewer counts, transaction
hashes, wallet addresses, contract addresses, block numbers, timestamps, percentages. Every
such figure must come from the script. If a frame is being rendered without a script-supplied
value, use a typeset placeholder: `— figure —`, `0x…`, `{price}`.

## Pre-Render Self-Audit

Before declaring a frame final, run every line:

- [ ] **Squint** — one element dominates at 3–6× nearest neighbor.
- [ ] **Silence** — frame reads 55–75% empty (or is the named ledger exception).
- [ ] **Voltage restraint** — purple gradient appears exactly **once** at full strength.
- [ ] **Weight discipline** — Outfit 800/900 only on display + pills; Inter on prose; Mono only
      on hashes/addresses.
- [ ] **Depth ceiling** — at most one of {glass card, glow halo, elevated card} per frame.
- [ ] **Geometry** — pills are perfect capsules; cards use the named radii; hairlines are 2px.
- [ ] **Anchor** — centered by default; left only for ledger / catalog; not the same anchor as
      the prior frame (unless beat ≤ 2).
- [ ] **Element count** — ≤ 2–3 distinct elements (focal + kicker + at most one support).
- [ ] **Floor** — no load-bearing line below 1.4cqw.
- [ ] **Headline measure** — text block ≤ 78cqw; ramp step matches word count.
- [ ] **Fidelity** — every size resolves to a frontmatter token; no ad-hoc cqw value invented
      in this frame's prose.
- [ ] **No invented numerals** — figures, hashes, balances are from the script or placeholders.

## Known Gaps

- **`cqw` as token value.** The DESIGN.md spec treats unknown units as opaque strings —
  intentional. Downstream consumers that don't support container queries must substitute `vw`
  and accept that frames will then own the viewport.
- **Aspect re-scales are guidance**, not pixel-exact. A renderer may step a hero one notch up
  or down to satisfy the 1.4cqw floor; the ramp itself is normative, the step choice is not.
- **Dot-grid pattern** lives in showcase CSS (background-image), not in a frontmatter token —
  the property-token set has no image type. Pattern: radial-gradient dots, 2px,
  `{colors.border-subtle}`, 2.4cqw spacing.
- **Glass blur** depends on what's behind. Frame 8 assumes a dot-grid; on a flat ground glass
  collapses to a flat card — by design, not a bug.
- **Motion specs** are derived from brand character; the source design.md does not enumerate
  cut timings, dwell, or export targets — those sections are derived, not lifted.
