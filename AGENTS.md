# Slideshow Presentations Plugin

This plugin sets up a [Slidev](https://sli.dev/) presentation environment in `Plugins/slideshow/`
and provides commands to generate slide decks from any Forge artifact.

## What This Plugin Provides

**Commands:**
- `/forge-slideshow-generate` — Read a Forge artifact (Proposal, Decision, Exploration, etc.) and
  generate a Slidev presentation from it. Output goes to `Plugins/slideshow/decks/<slug>.md`.
- `/forge-slideshow-start` — List available decks and start the Slidev dev server.

**Templates:**
- `Slideshow-Presentation.md` — Slidev Markdown skeleton for manually crafting a presentation.

## Setup

After installing this plugin, run once inside `Plugins/slideshow/`:

    npm install

Generated decks land in `Plugins/slideshow/decks/`. To add a custom Slidev theme, place it in
`Plugins/slideshow/themes/` and reference it in the deck's frontmatter (`theme: ./themes/<name>`).

## Prerequisites

- Node.js installed
- `npm install` run inside `Plugins/slideshow/` after first install
