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

2. **Ensure dependencies.** If `node_modules/` does not exist in `Plugins/presentation/`, run:

       cd Plugins/presentation && npm install

3. **Start the dev server.** Use the Task tool (subagent_type: Bash) to run the server as a
   background task, so it keeps running while the conversation continues. The command must be run
   from inside `Plugins/presentation/` and supply an absolute theme path:

       cd <workspace-root>/Plugins/presentation && \
       node_modules/.bin/slidev "<absolute-path-to-deck>" \
         --theme "$(pwd)/node_modules/@slidev/theme-default" \
         --no-open

4. **Report.** Tell the user the server is running at `http://localhost:3030` and that they can
   stop it by PID if needed, or by closing the conversation.

**Awaiting your direction.** Which deck should I start?
