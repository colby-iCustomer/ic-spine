# Agent context — projects/

Rules for editing anything in this folder.

- Each project lives at `projects/<stream>/<owner>/<slug>/`. Never put loose files at any intermediate level.
- Stream folders right now: `pm/`, `eng/` (placeholder), `pmm/` (placeholder).
- Owner folders inside `pm/`: `colby/`, `abhi/`. Don't create new owner folders without explicit human approval.
- Slug is kebab-case, descriptive but short: `utm-capi-product-model`, `audience-activation-model`.
- When creating a new project, you MUST update `projects/index.md` with a new row under **Active**.
- When marking a project complete, move the index row to **Complete**. Keep the folder where it is.
- When promoting a project, move artifacts to their target (e.g., `products/<tier>/features/<slug>/`) and move the index row to **Promoted**. The original project folder can be deleted after promotion, OR kept as a thin pointer (your choice — be consistent within a stream).
- Don't edit other owners' folders. PR for cross-owner changes.
- For project scaffolding, use the canonical structure: `brief.md`, `state.md`, `notes.md`, `deliverables/`, `working/`, `sources/`.
- `deliverables/` is versioned (`v1.md`, `v2.md`). Never overwrite.
- `sources/` is read-only by convention — only add files, don't edit existing imports.
- `working/` is fair game — drafts, scratch files, anything in motion.
