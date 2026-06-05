# ic-spine

The spine is where iCustomer keeps the things that hold everything else together.

Engineering builds in the monorepo. Product plans in `ic-product-mgmt`. Meetings live in calendar tools. Conversations live in Slack. **The spine is what those surfaces lean on.** It's the durable answer to "how do we work here," "what is this product," "what are we doing right now," and "show me the template."

If you're new: read this page top to bottom, then open the folder you need. If you're looking something up: jump straight to [Where to find things](#where-to-find-things).



## The folders, briefly

| Folder | What lives here | Read this when |
|---|---|---|
| [handbooks/](handbooks/) | How each team operates — engineering's dev loop, product's sprint cadence, marketing's launch playbook | You're new and learning the ropes |
| [architecture/](architecture/) | What the platform is — the C4 model (landscape, containers, components) | You need to understand the system, not just operate it |
| [products/](products/) | One folder per product: positioning, state, glossary, shipped features, mind maps | You want to know what a product is, what it does, what's shipped |
| [projects/](projects/) | Active work in flight — one folder per person, per project. Status tracked in [projects/index.md](projects/index.md) | You're doing the work, or want to see what's underway |
| [templates/](templates/) | PR templates, ticket templates, project scaffolds | You're starting something new |
| [website/](website/) | Page templates + character limits for the marketing site (the actual site lives in its own repo) | You're editing copy or shipping a new page |
| [design-guide/](design-guide/) | Visual + interaction standards | You're designing something user-facing |



## How the spine breathes (pace of change)

Different folders move at different speeds. We label them by temperature so you know what to expect:

```
🥶 templates/         Freezing  → almost never change
❄️  handbooks/        Cold      → quarterly-ish
❄️  products/         Cold      → updated when positioning or state shifts
🌤️  website/          Warm      → with each launch
🌤️  design-guide/     Warm      → with each design pass
🔥 projects/         Hot       → daily
🔥 architecture/     Hot       → currently — actively being built pre-launch
```

A change in a Cold folder is a big deal. A change in a Hot folder is Tuesday.



## Project lifecycle: brainstorm → create → promote

Everything is a project from day one. There are no "initiatives" or "drafts" as separate concepts.

1. **Brainstorm** — an idea. Lives nowhere yet. A Slack thread, a notebook page, a meeting note.
2. **Create** — the idea becomes a project. A folder appears at `projects/<stream>/<owner>/<slug>/` with `brief.md`, `state.md`, `notes.md`, plus `deliverables/`, `working/`, `sources/` subfolders. The project is added to [projects/index.md](projects/index.md) as **Active**.
3. **Promote** — when the project ships, its artifacts move into their permanent home: usually `products/<tier>/features/`, sometimes `design-guide/` or `handbooks/`. The index entry moves to **Promoted**.

Status options in the index: **Active · Paused · Complete · Promoted · Deferred**. (Complete and Promoted are kept separate: a project can be done but not yet integrated.)



## Folder shape inside a project

```
projects/<stream>/<owner>/<slug>/
├── brief.md          ← What and why (North Star, goals, scope). 1-2 pages.
├── state.md          ← Where I left off. Overwritten each session.
├── notes.md          ← Scratchpad. Raw thinking, Q&A.
├── deliverables/     ← Read-only by convention. Versioned outputs only.
├── working/          ← Read-write. Active drafts, work-in-progress.
└── sources/          ← Read-only. Reference material, imported docs.
```

The split between `working/` and `deliverables/` matters: anything in `deliverables/` should be an explicit version (`strategy-v1.md`, not `strategy.md`), so review history is preserved without leaning on git.



## Where to find things

| Looking for... | Go to |
|---|---|
| How we run sprints | [handbooks/product/](handbooks/product/) |
| The dev loop (`/build`, `/qa`, `/ship`, `/retro`) | [handbooks/engineering/sdlc-lifecycle.md](handbooks/engineering/sdlc-lifecycle.md) |
| The ADR governance tiers | [handbooks/engineering/adr-governance.md](handbooks/engineering/adr-governance.md) |
| The platform layer diagram | [architecture/containers.md](architecture/containers.md) |
| OneSource component diagram | [architecture/components.md](architecture/components.md) |
| ALoop positioning | [products/smb-audience-loop/positioning.md](products/smb-audience-loop/positioning.md) |
| Decision OS positioning | [products/enterprise-decision-os/positioning.md](products/enterprise-decision-os/positioning.md) |
| OneSource positioning | [products/onesource/positioning.md](products/onesource/positioning.md) |
| Brand positioning (cross-product) | [products/icustomer/positioning.md](products/icustomer/positioning.md) |
| What's in flight right now | [projects/index.md](projects/index.md) |
| How to start a new project | [templates/projects/colby-project.md](templates/projects/colby-project.md) |
| PR template for a bug | [templates/pr/bug.md](templates/pr/bug.md) |
| Character limits for the pricing page | [website/character-limits.md](website/character-limits.md) |



## Concurrency

We work in one repo, so we need a simple rule: **you only direct-push to your own folder.** Everything else is a PR.

| File | Edit how |
|---|---|
| `projects/pm/colby/**`, `projects/pm/abhi/**` | Direct push — single owner |
| Anything else (READMEs, indexes, positioning, handbooks, templates) | Short-lived branch + PR. Merge same day. |

If two people need to work the same doc at the same time: use Notion or Google Doc, then import on finalize. Don't try to git-collaborate on prose.



## What the spine is not

To keep the surface tight, the spine does **not** hold:

- Code — that's the monorepo
- Meetings, triage notes, sprint logs — those live in `ic-product-mgmt`
- Jira tickets — Jira is the SSOT; spine references it, doesn't mirror
- CI / build config — monorepo
- The actual website source — only templates + character limits live here



## Open questions for the team

These got flagged during scoping but didn't need to land before Day 1. Raise them when convenient:

1. Where should `design-guide/` permanently live? Root (current), inside `architecture/`, inside `handbooks/engineering/`, or split per product?
2. Glossary strategy — one master, per-folder (current), or hybrid with cross-references?
3. Should a `sprint/` folder exist? Currently kept out; sprint planning lives in `ic-product-mgmt`.
4. MD vs MDX — default is MD. MDX upgrade is per-page, only when a real React component needs to render.



## Adjacent repos

- **`ic-product-mgmt`** — Colby's PM working surface. Meetings, triage, sprints, active PM artifacts.
- **`icustomer-docs`** — engineering's draft handbook (will merge into `handbooks/engineering/` + `architecture/`).
- **monorepo** — code. The spine governs but never touches code.
