# Forge: Presentation — Start

Start the Slidev dev server to preview or edit a presentation deck.

## Steps

1. **List available decks.** Search for `*.md` files inside any `Presentations/` subdirectory
   under `Initiatives/` and `Products/`. If none are found, suggest running
   `/forge-presentation-new` first.

2. **Select deck.** If there is more than one deck, ask which one to start (show the initiative
   path alongside the filename for clarity). If there is exactly one, proceed automatically.

3. **First-time setup check.** If `node_modules/` does not exist in `Plugins/presentation/`, remind
   the user to run `npm install` inside that folder first.

4. **Show the command.** Tell the user to run from the workspace root in their terminal:

       npx --prefix Plugins/presentation slidev <path-to-deck>

   Slidev will open the browser at `http://localhost:3030`. Press `Ctrl+C` to stop.

**Awaiting your direction.** Ready to start a deck?
