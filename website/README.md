# website/

Page templates + character limits + the workflow for editing copy on the marketing site.

**The actual website source code lives in its own repo.** This folder is where templates, character constraints, and Claude-editable shells live so they can be edited safely without touching production.

## Structure

```
website/
├── README.md             (this file)
├── skill.md              (agent context for editing here)
├── character-limits.md   (per-section character constraints — the README points Claude to)
└── page-templates/       (HTML / MD shells per page type)
    ├── pricing/
    ├── comparison/
    └── use-case/
```

## How it works

Colby ships HTML shells + a character-limits reference. Abhi opens the shell in his Claude project (with memory enabled, not Claude Code) and edits ONLY the text. The character-limits reference tells Claude to flag overages so copy stays within design constraints.

Workflow:
1. Colby creates / updates a shell under `page-templates/<page>/`
2. README in the page-templates folder points to the relevant character-limits section
3. Abhi opens shell + README in Claude project, edits text
4. Abhi sends back edited shell
5. Colby commits the new version + pushes to the actual website repo

## Why this lives here

- Templates are reusable across launches → spine is the right home
- Character limits are policy → spine is the right home
- The actual website source is engineering / deployable → wrong home for this

## Update cadence

🌤️ **Warm** — updates with each launch. New page templates as new page types ship.
