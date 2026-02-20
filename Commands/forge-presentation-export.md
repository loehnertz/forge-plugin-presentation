# Forge: Presentation — Export

Export a presentation deck to PDF, PPTX, or both.

## Steps

1. **Resolve deck.**
   - If a deck was named or described in the invocation, search `Initiatives/` and `Products/` for
     a matching `*.md` file inside any `Presentations/` subdirectory and confirm it with the user
     before proceeding.
   - If no deck was specified, search `Initiatives/` and `Products/` for all `*.md` files inside
     any `Presentations/` subdirectory. If none are found, suggest running `/forge-presentation-new`
     first. Otherwise present a numbered list with each deck's title and initiative path, then ask
     the user to pick one.

2. **Resolve format.**
   - If a format (PDF, PPTX, or both) was specified in the invocation, use it.
   - If no format was specified, ask: "Which format? PDF, PPTX, or both?"
   Note: PDF export is reliable and recommended for sharing. PPTX export is supported but may not
   preserve all animations or layouts perfectly.

3. **Ensure dependencies.** If `node_modules/` does not exist in `Plugins/presentation/`, run:

       cd Plugins/presentation && npm install

4. **Run the export.** Derive the output path by replacing the deck's `.md` extension with the
   target format extension (e.g. `slug.md` → `slug.pdf`). Run the relevant command(s) from the
   workspace root:

   For PDF:
       npx --prefix Plugins/presentation slidev export <path-to-deck> --format pdf --output <path-to-deck-without-ext>.pdf

   For PPTX:
       npx --prefix Plugins/presentation slidev export <path-to-deck> --format pptx --output <path-to-deck-without-ext>.pptx

5. **Report.** Tell the user the output path(s) — the exported files land alongside the source
   deck in the same `Presentations/` folder.

**Awaiting your direction.** Which deck should I export, and in what format?
