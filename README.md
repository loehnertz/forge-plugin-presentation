# forge-plugin-slideshow

A [Forge](https://github.com/loehnertz/forge) plugin that adds [Slidev](https://sli.dev/)
presentation generation to Forge workspaces. Generate polished slide decks from any Forge
artifact — Proposals, Decisions, Explorations, and more.

## What It Provides

- `/forge-slideshow-generate` — Read a Forge artifact and generate a Slidev presentation from it
- `/forge-slideshow-start` — List available decks and start the Slidev dev server
- `Templates/Slideshow-Presentation.md` — Slidev Markdown skeleton for manually crafting presentations
- A ready-to-run Slidev environment (`package.json` + `themes/` + `decks/`)

## Install

### 1. Copy the plugin into your workspace

```bash
copier copy gh:loehnertz/forge-plugin-slideshow Plugins/slideshow
```

### 2. Register it in `forge-plugins.yml`

Add an entry to your workspace's `forge-plugins.yml`:

```yaml
plugins:
  - name: slideshow
    source: gh:loehnertz/forge-plugin-slideshow
    path: Plugins/slideshow
```

### 3. Install dependencies

```bash
cd Plugins/slideshow
npm install
```

## Usage

### Generate a presentation

Invoke `/forge-slideshow-generate` in your AI tool. You will be asked which artifact to convert.
The generated deck is written to `Plugins/slideshow/decks/<slug>.md`.

### Preview a presentation

Invoke `/forge-slideshow-start`, or run directly:

```bash
cd Plugins/slideshow
npx slidev decks/<deck-name>.md
```

Slidev opens the browser at `http://localhost:3030`. Press `Ctrl+C` to stop.

## Theme Customization

Drop a Slidev-compatible theme directory into `Plugins/slideshow/themes/`, then reference it in
a deck's frontmatter:

```yaml
---
theme: ./themes/<theme-name>
---
```

## Update

```bash
copier update Plugins/slideshow
```

This pulls the latest plugin files. Your generated decks in `decks/` and custom themes in
`themes/` are not affected by updates.
