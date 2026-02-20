# Forge: Slideshow — Start

Start the Slidev dev server to preview or edit a presentation deck.

## Steps

1. **List available decks.** List the files in `Presentations/` at the workspace root. If the
   directory is empty or does not exist, suggest running `/forge-slideshow-generate` first.

2. **Select deck.** If there is more than one deck, ask which one to start. If there is exactly
   one, proceed with it automatically.

3. **First-time setup check.** If `node_modules/` does not exist in `Plugins/slideshow/`, remind
   the user to run `npm install` inside that folder first.

4. **Show the command.** Tell the user to run from the workspace root in their terminal:

       npx --prefix Plugins/slideshow slidev Presentations/<selected-deck>.md

   Slidev will open the browser at `http://localhost:3030`. Press `Ctrl+C` to stop.

**Awaiting your direction.** Ready to start a deck?
