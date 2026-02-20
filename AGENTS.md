# Presentations Plugin

This plugin sets up a [Slidev](https://sli.dev/) presentation environment in `Plugins/presentation/`
and provides commands to generate slide decks from any Forge artifact.

## What This Plugin Provides

**Commands:**
- `/forge-presentation-new` — Find a Forge artifact by name/topic and generate a Slidev presentation
  from it. Output goes to `Presentations/<slug>.md` at the workspace root.
- `/forge-presentation-start` — List available decks in `Presentations/` and start the Slidev dev
  server.
- `/forge-presentation-export` — Export a deck to PDF, PPTX, or both via `slidev export`.

**Templates:**
- `Presentation.md` — Slidev Markdown skeleton for manually crafting a presentation.

## Setup

After installing this plugin, run once inside `Plugins/presentation/`:

    npm install

Generated decks land in `Presentations/` at the workspace root. To add a custom Slidev theme,
place it in `Plugins/presentation/Themes/` and reference it in the deck's frontmatter
(`theme: ./Themes/<name>`).

## Prerequisites

- Node.js installed
- `npm install` run inside `Plugins/presentation/` after first install
