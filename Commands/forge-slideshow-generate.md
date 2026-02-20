# Forge: Slideshow — Generate

Generate a Slidev presentation deck from a Forge artifact.

## Steps

1. **Get artifact path.** If not provided, ask: "Which artifact should I turn into a presentation?
   Provide the file path."

2. **Read artifact.** Read the file at the given path. Extract:
   - `title` from frontmatter or the first `#` heading
   - `status` from frontmatter if present
   - All `##` section headings and their content

3. **Derive deck name.** Slugify the title: lowercase, spaces replaced with hyphens. The output
   file will be `Plugins/slideshow/decks/<slug>.md`.

4. **Generate deck.** Using `Templates/Slideshow-Presentation.md` as a structural guide, produce
   a Slidev Markdown file:
   - Title slide: artifact title, status if available, today's date
   - One slide per major `##` section (trim prose to bullets; keep slides concise)
   - Closing "Next Steps" or "Questions?" slide

5. **Write output.** Write the generated deck to `Plugins/slideshow/decks/<slug>.md`.

6. **Report.** Tell the user the output path, the slide count, and how to preview it:
   run `/forge-slideshow-start` or `cd Plugins/slideshow && npx slidev decks/<slug>.md`.

**Awaiting your direction.** Which artifact should I generate a presentation from?
