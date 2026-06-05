# Project template — canonical scaffold

> The canonical structure for any new project under `projects/<stream>/<owner>/<slug>/`.
> Modeled on the `pm-create-project` skill from `ic-product-mgmt`.

## When you create a project

A new project folder appears at:

```
projects/<stream>/<owner>/<slug>/
```

Where:
- `<stream>` = `pm` for now (eng + pmm added later)
- `<owner>` = `colby` or `abhi` (or a new owner added with team approval)
- `<slug>` = kebab-case, descriptive but short. Example: `utm-capi-product-model`, `audience-activation-model`, `apify-evaluation`.

## What gets scaffolded

```
projects/<stream>/<owner>/<slug>/
├── brief.md          ← 1-2 pages: North Star, goals, scope, success criteria
├── state.md          ← session state; overwritten each work session
├── notes.md          ← scratchpad; raw thinking
├── deliverables/     ← versioned outputs (v1, v2). Read-only by convention.
├── working/          ← active drafts, work-in-progress. Read-write.
└── sources/          ← reference material, imports. Read-only by convention.
```

## File contents

### brief.md

- **North Star** — the one-line outcome this project moves toward
- **Goals** — 3-5 numbered, measurable goals
- **Scope** — in-scope / out-of-scope
- **Resources** — links to source docs, meetings, related projects
- **Key risks** — what might derail this
- **Outcomes** — what artifacts ship at the end (deliverables list)
- **Dependencies** — people + projects this hinges on

### state.md

- **Current phase** — what stage you're in
- **What just happened** — last session's accomplishments
- **What's next** — next concrete step
- **Blockers** — anything blocking progress

### notes.md

- Free-form scratchpad. Q&A, raw thinking, half-formed ideas. Not curated.

## Lifecycle (recap)

```
Brainstorm  →  Create  →  Promote
```

1. **Brainstorm** — idea, not yet a project
2. **Create** — folder scaffolded (this template), added to `projects/index.md` as Active
3. **Promote** — deliverables move to permanent home (`products/<tier>/features/`, `design-guide/`, or `handbooks/`); index status moves to Promoted

## Example slug naming

| Bad | Good | Why |
|---|---|---|
| `new-project` | `apify-evaluation` | Says what the project IS |
| `colbys-feature-1` | `utm-capi-product-model` | No owner in slug; owner is the folder |
| `2026-06-launch-stuff` | `audience-activation-model` | No dates in slug; folder mtime tells you that |
| `THE_BIG_ONE` | `master-audience-architecture` | Descriptive, kebab-case |

## How to actually create a project

For now: manually mkdir + copy this template. Once `.claude/skills/create-spine-project/` ships, it'll be `/create-spine-project <slug>` and the skill handles the scaffold + index update.
