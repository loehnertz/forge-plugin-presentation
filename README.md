# forge-plugin-presentation

A [Forge](https://github.com/loehnertz/forge) plugin that adds [Slidev](https://sli.dev/)
presentation generation to Forge workspaces. Generate polished slide decks from any Forge
artifact — Proposals, Decisions, Explorations, and more.

## What It Provides

- `/forge-presentation-new` — Find a Forge artifact by name/topic and generate a Slidev presentation
- `/forge-presentation-start` — List available decks and start the Slidev dev server
- `/forge-presentation-export` — Export a deck to PDF, PPTX, or both
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

### Create a presentation

Invoke `/forge-presentation-new` in your AI tool. Describe the artifact by name or topic — the AI
will find it in your workspace. The generated deck is written to a `Presentations/` subfolder
inside the same initiative as the source artifact (e.g.
`Initiatives/<Initiative>/Presentations/<slug>.md`).

### Preview a presentation

Invoke `/forge-presentation-start`, or run from the workspace root:

```bash
npx --prefix Plugins/presentation slidev Presentations/<deck-name>.md
```

Slidev opens the browser at `http://localhost:3030`. Press `Ctrl+C` to stop.

### Export a presentation

Invoke `/forge-presentation-export` in your AI tool, or run from the workspace root:

```bash
# PDF (recommended)
npx --prefix Plugins/presentation slidev export Presentations/<deck-name>.md --format pdf

# PPTX
npx --prefix Plugins/presentation slidev export Presentations/<deck-name>.md --format pptx
```

> **Note:** PDF export is reliable. PPTX export may not preserve all animations or layouts.

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

This pulls the latest plugin files. Your generated decks (inside initiative `Presentations/`
folders) and custom themes in `Plugins/presentation/Themes/` are not affected by updates.
