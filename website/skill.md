# Agent context — website/

- Page templates + character limits. The actual website source is in a separate repo — NEVER edit production directly from here.
- When editing a page shell, ONLY edit the text. Don't change the HTML structure. The character-limits reference is the rulebook.
- Use `character-limits.md` to validate copy. If a section exceeds its limit, flag it — don't silently truncate.
- New page templates land in `page-templates/<type>/`. Each has its own README pointing to the character-limit section.
- If a new page type ships, create a new folder under `page-templates/` and update this README's table.
- The workflow is intentionally split: Colby owns shells (structure), Abhi owns text (copy). Don't conflate.
