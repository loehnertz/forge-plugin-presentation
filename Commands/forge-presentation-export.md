# Forge: Presentation — Export

Export a presentation deck to PDF, PPTX, or both.

## Steps

1. **List available decks.** Search for `*.md` files inside any `Presentations/` subdirectory
   under `Initiatives/` and `Products/`. If none are found, suggest running
   `/forge-presentation-new` first.

2. **Select deck.** If there is more than one deck, ask which one to export (show the initiative
   path alongside the filename for clarity). If there is exactly one, proceed automatically.

3. **Select format.** Ask: "Which format? PDF, PPTX, or both?"
   Note: PDF export is reliable and recommended for sharing. PPTX export is supported but may not
   preserve all animations or layouts perfectly.

4. **First-time setup check.** If `node_modules/` does not exist in `Plugins/presentation/`, remind
   the user to run `npm install` inside that folder first.

5. **Show the command(s).** Tell the user to run from the workspace root in their terminal:

   For PDF:
       npx --prefix Plugins/presentation slidev export <path-to-deck> --format pdf

   For PPTX:
       npx --prefix Plugins/presentation slidev export <path-to-deck> --format pptx

   The exported file(s) will be written to the same `Presentations/` folder as the source deck.

6. **Report.** Once the user has run the command, confirm the output path(s).

**Awaiting your direction.** Which deck should I export, and in what format?
