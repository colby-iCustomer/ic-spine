# projects/

In-flight work. Everything that someone is actively doing lives here as a **project**, regardless of size.

## Structure

```
projects/
├── README.md     (this file)
├── index.md      (status register — Active / Paused / Complete / Promoted / Deferred)
├── pm/
│   ├── colby/
│   │   └── <project-slug>/
│   └── abhi/
│       └── <project-slug>/
├── eng/          (added when engineering joins the spine workflow)
└── pmm/          (added when PMM joins)
```

Streams (`pm/`, `eng/`, `pmm/`) split projects by which team drives them. Each stream then splits by owner — every person has their own folder so concurrent work doesn't collide.

## Per-project folder shape

When you create a project, the folder gets scaffolded with:

```
projects/<stream>/<owner>/<slug>/
├── brief.md          (North Star, goals, scope, success criteria — 1-2 pages)
├── state.md          (current session state — overwritten each session)
├── notes.md          (working scratchpad — raw thinking)
├── deliverables/     (read-only by convention — versioned outputs only)
├── working/          (read-write — drafts, work-in-progress)
└── sources/          (read-only — reference material, imported docs)
```

Use [templates/projects/colby-project.md](../templates/projects/colby-project.md) for the canonical example of how to create a project.

## Lifecycle

```
Brainstorm  →  Create Project  →  Promote
```

1. **Brainstorm** — idea phase, lives nowhere yet
2. **Create** — folder scaffolds, project added to `index.md` as Active
3. **Promote** — when the work ships, artifacts move to their permanent home:
   - Features → `products/<tier>/features/<slug>/`
   - Design work → `design-guide/`
   - Process changes → `handbooks/<audience>/`
   - Index entry moves to **Promoted**

## Rules

- One owner per project folder. If multiple people contribute, the owner curates the working dir.
- Direct-push allowed in your own owner folder. Everything else (the index, READMEs) is PR-only.
- Don't delete completed projects. Promote them. The index keeps the historical thread.
