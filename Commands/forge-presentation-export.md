# Forge: Presentation — Export

Export a presentation deck to PDF, PPTX, or both.

## Steps

1. **List available decks.** List the files in `Presentations/` at the workspace root. If the
   directory is empty or does not exist, suggest running `/forge-presentation-new` first.

2. **Select deck.** If there is more than one deck, ask which one to export. If there is exactly
   one, proceed with it automatically.

3. **Select format.** Ask: "Which format? PDF, PPTX, or both?"
   Note: PDF export is reliable and recommended for sharing. PPTX export is supported but may not
   preserve all animations or layouts perfectly.

4. **First-time setup check.** If `node_modules/` does not exist in `Plugins/presentation/`, remind
   the user to run `npm install` inside that folder first.

5. **Show the command(s).** Tell the user to run from the workspace root in their terminal:

   For PDF:
       npx --prefix Plugins/presentation slidev export Presentations/<deck>.md --format pdf

   For PPTX:
       npx --prefix Plugins/presentation slidev export Presentations/<deck>.md --format pptx

   The exported file(s) will be written to `Presentations/` alongside the source deck.

6. **Report.** Once the user has run the command, confirm the output path(s).

**Awaiting your direction.** Which deck should I export, and in what format?
