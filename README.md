# forge-plugin-presentation

A [Forge](https://github.com/loehnertz/forge) plugin that adds [Slidev](https://sli.dev/)
presentation generation to Forge workspaces. Generate polished slide decks from any Forge
artifact — Proposals, Decisions, Explorations, and more.

## What It Provides

- `/forge-presentation-generate` — Read a Forge artifact and generate a Slidev presentation from it
- `/forge-presentation-start` — List available decks and start the Slidev dev server
- `Templates/Presentation.md` — Slidev Markdown skeleton for manually crafting presentations
- A ready-to-run Slidev environment (`package.json` + `Themes/`)

## Install

### 1. Copy the plugin into your workspace

```bash
copier copy gh:loehnertz/forge-plugin-presentation Plugins/presentation
```

### 2. Register it in `forge-plugins.yml`

Add an entry to your workspace's `forge-plugins.yml`:

```yaml
plugins:
  - name: presentation
    source: gh:loehnertz/forge-plugin-presentation
    path: Plugins/presentation
```

### 3. Install dependencies

```bash
cd Plugins/presentation
npm install
```

## Usage

### Generate a presentation

Invoke `/forge-presentation-generate` in your AI tool. You will be asked which artifact to convert.
The generated deck is written to `Presentations/<slug>.md` at the workspace root.

### Preview a presentation

Invoke `/forge-presentation-start`, or run from the workspace root:

```bash
npx --prefix Plugins/presentation slidev Presentations/<deck-name>.md
```

Slidev opens the browser at `http://localhost:3030`. Press `Ctrl+C` to stop.

## Theme Customization

Drop a Slidev-compatible theme directory into `Plugins/presentation/Themes/`, then reference it in
a deck's frontmatter:

```yaml
---
theme: ./Themes/<theme-name>
---
```

## Update

```bash
copier update Plugins/presentation
```

This pulls the latest plugin files. Your generated decks in `Presentations/` and custom themes in
`Plugins/presentation/Themes/` are not affected by updates.
