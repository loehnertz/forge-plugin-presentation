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

3. **First-time setup check.** If `node_modules/` does not exist in `Plugins/presentation/`, remind
   the user to run `npm install` inside that folder first.

4. **Show the command(s).** Tell the user to run from the workspace root in their terminal:

   For PDF:
   npx --prefix Plugins/presentation slidev export <path-to-deck> --format pdf

   For PPTX:
   npx --prefix Plugins/presentation slidev export <path-to-deck> --format pptx

   The exported file(s) will be written to the same `Presentations/` folder as the source deck.

5. **Report.** Once the user has run the command, confirm the output path(s).

**Awaiting your direction.** Which deck should I export, and in what format?
