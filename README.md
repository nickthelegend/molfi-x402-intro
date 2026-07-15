# Molfi X402 Intro

**A HyperFrames motion-graphics intro video for MOLFI.FUN — the agentic payments rail on Avalanche Fuji, powered by the x402 protocol.**

> Deep-space ground, neon-purple voltage, oversized Outfit type, and mono ledgers — a keynote-grade brand sting rendered from a single HTML timeline.

## Overview

This repository is a [HyperFrames](https://hyperframes.heygen.com) composition project: a self-contained, deterministic HTML/CSS/GSAP animation that renders to MP4. It is the launch intro for **MOLFI.FUN**, a crypto-payments product where AI agents settle in USDC (signed with EIP-3009 over the x402 protocol) and human users pay in attention by watching sponsor ads for signed JWT credits.

The whole video lives in one paused, seek-safe GSAP timeline inside `index.html`, driving eight scenes across a 33.6-second runtime. `design.md` is the accompanying "frame-scale" brand spec — a video-first design system (colors, typography ramps, components, and per-treatment frame recipes) built on top of the MOLFI.FUN product brand.

## Features

- **Eight-scene brand narrative** — cover lockup, "PAY PER PROMPT" oversized claim, a two-up rail comparison (agents pay in USDC vs. humans pay in attention), a glassmorphic composer card, a `402` glow-stat, an Avalanche Fuji transaction ledger, a settled-tx hash-block closer, and a brand sign-off.
- **Single deterministic timeline** — one paused `gsap.timeline` registered on `window.__timelines["main"]`, with no `Math.random`, `Date.now`, or network fetches, so every frame is reproducible for rendering.
- **Frame-native design system** (`design.md`) — brand tokens, two typography ramps (reading + display/hero), reusable components (pulse badge, gradient CTA, glass card, ledger row, hash block, glow ring), and eight documented frame treatments with a pre-render self-audit checklist.
- **Locally embedded fonts** — Outfit (latin + latin-ext `woff2`) is `@font-face`-embedded for render fidelity; JetBrains Mono and Inter carry hashes and prose.
- **Multi-aspect authoring intent** — the spec documents 16:9 (primary), 9:16, and 1:1 re-scale behavior per treatment.
- **Rendered outputs included** — 1080p60 16:9 MP4 renders plus extracted key frames live under `renders/`.

## Tech Stack

- **HyperFrames** `0.6.104` — composition, preview, lint/validate, render, and publish tooling (run via `npx`)
- **GSAP** `3.14.2` — timeline animation (loaded from CDN in the composition)
- **HTML / CSS** — a single `index.html` root timeline on a `1920 × 1080` canvas
- **Fonts** — Outfit (embedded `woff2`), Inter, JetBrains Mono

## Getting Started

```bash
# clone
git clone https://github.com/nickthelegend/molfi-x402-intro.git
cd molfi-x402-intro

# start the preview server (long-running)
npm run dev

# lint + validate + inspect the composition
npm run check

# render to MP4
npm run render

# publish and get a shareable link
npm run publish
```

> No `npm install` is required — the scripts invoke `hyperframes` on demand through `npx --yes hyperframes@0.6.104`.

## Project Structure

```
index.html         # main composition — the root GSAP timeline (8 scenes)
design.md          # frame.md — video-first brand / design system spec
hyperframes.json   # HyperFrames project config (registry + paths)
meta.json          # project metadata (id, name, createdAt)
package.json       # dev / check / render / publish scripts
assets/            # logo.png and other composition assets
fonts/             # embedded Outfit woff2 (latin + latin-ext)
renders/           # rendered MP4 outputs and extracted frames
AGENTS.md          # agent/authoring guidance for this project
CLAUDE.md          # authoring guidance (identical to AGENTS.md)
```

---

Built by [nickthelegend](https://github.com/nickthelegend) · [nickthelegend.tech](https://nickthelegend.tech)
