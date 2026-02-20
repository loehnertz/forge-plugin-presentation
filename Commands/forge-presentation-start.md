# Forge: Presentation — Start

Start the Slidev dev server to preview or edit a presentation deck.

## Steps

1. **Resolve deck.**
   - If a deck was named or described in the invocation, search `Initiatives/` and `Products/` for
     a matching `*.md` file inside any `Presentations/` subdirectory and confirm it with the user
     before proceeding.
   - If no deck was specified, search `Initiatives/` and `Products/` for all `*.md` files inside
     any `Presentations/` subdirectory. If none are found, suggest running `/forge-presentation-new`
     first. Otherwise present a numbered list with each deck's title and initiative path, then ask
     the user to pick one.

2. **First-time setup check.** If `node_modules/` does not exist in `Plugins/presentation/`, remind
   the user to run `npm install` inside that folder first.

3. **Show the command.** Tell the user to run from the workspace root in their terminal:

       npx --prefix Plugins/presentation slidev <path-to-deck>

   Slidev will open the browser at `http://localhost:3030`. Press `Ctrl+C` to stop.

**Awaiting your direction.** Which deck should I start?
