# CLAUDE.md — forge-plugin-slideshow

## What This Repository Is

This is the **forge-plugin-slideshow** plugin repository. It extends Forge workspaces with Slidev
presentation generation. Plugins are distributed via Copier — everything not in `copier.yml`'s
`_exclude` is copied into `Plugins/slideshow/` when a workspace installs this plugin.

## What Gets Distributed

Distributed to workspace (everything NOT in `_exclude`):
- `AGENTS.md` — plugin context for AI tools
- `package.json` — Slidev dependencies
- `.gitignore` — excludes node_modules from workspace git
- `Commands/` — command files
- `Templates/` — artifact templates
- `Themes/` — custom themes directory

NOT distributed (in `_exclude`):
- `copier.yml`, `forge-plugin.yml`, `README.md`, `CLAUDE.md`, `.git`

## Plugin Conventions

- Plugin `name`: `slideshow` (lowercase, no hyphens — used as the namespace)
- Commands: `forge-slideshow-<verb>.md` (e.g., `forge-slideshow-generate.md`)
- Templates: `Slideshow-<Type>.md` (e.g., `Slideshow-Presentation.md`)
- Plugin context: `AGENTS.md` (AI-readable; describes what this plugin provides)

## Testing Changes Locally

```bash
copier copy . /tmp/test-ws/Plugins/slideshow --defaults
```

Verify the installed files match expectations (meta files absent, distributed files present).

## Key References

- Forge Plugin System: see the Plugin System section in `../forge/FORGE.md`
- Slidev documentation: https://sli.dev/
- Plugin descriptor schema: `forge-plugin.yml` in this repo
