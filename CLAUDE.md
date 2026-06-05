# ic-spine — Claude / Cursor / Agent Instructions

> This file is read directly by Claude Code and other coding agents. Keep instructions terse and authoritative.

## What this repo is

The iCustomer **spine** — the governance layer between product and engineering. It holds:
- How we operate (handbooks)
- What the system is (architecture)
- What our products are (products)
- What we're doing now (projects)
- The templates we use (templates)
- The website's page templates (website)
- Design standards (design-guide)

Read [README.md](README.md) for the human-facing overview.

## Editing rules

### Format

- **All content is Markdown** (`.md`). Upgrade to `.mdx` ONLY when a page genuinely needs an embedded React component (rare).
- Use standard CommonMark. No project-specific dialects.
- No em-dashes (`—`) in any text you write. Use hyphen, comma, period, semicolon, or line break instead. Em-dashes in code, CLI flags, and markdown table separators (`|---|`) are fine.

### Per-folder context

Each top-level folder has a `skill.md` that defines local rules. Read the relevant folder's `skill.md` before editing files in that folder.

### Concurrency

| Folder | Edit rule |
|---|---|
| `projects/pm/<your-name>/**` | Direct push allowed — single owner |
| All other content | Open a short-lived branch + PR. Merge same day. |

Never force-push to main. Never rewrite history on main.

### Linking

- Use relative links between files inside the spine (`[brief](../projects/pm/colby/<slug>/brief.md)`).
- Use absolute links for external (`https://icustomer.atlassian.net/...`).
- Verify a target file exists before linking to it. If it doesn't, write `(planned)` after the link.

### When to update what

| Change | Update |
|---|---|
| Created a new project | `projects/<stream>/<name>/<slug>/` + add row to `projects/index.md` (Active) |
| Project finished | Move to `Complete` in `projects/index.md`; if artifacts move, also move to `Promoted` |
| Product positioning shifted | `products/<tier>/positioning.md` + bump the change-log line at the top |
| New process / SOP | `handbooks/<audience>/` |
| New architecture (container or component added) | `architecture/containers.md` or `components.md` |
| New PR / ticket convention | `templates/pr/` or `templates/tickets/` |

## Out of scope

Do **not** add to this repo:
- Code (lives in the monorepo)
- Meetings or triage notes (lives in `ic-product-mgmt`)
- Jira ticket copies (Jira is SSOT)
- CI config (lives in monorepo)
- The actual website source

## Glossary

For terms (iStack, iDash, iWorker, Decision Trace, FIRE, Immutable ID, etc.), check:
1. `architecture/reference.md` — platform-level terms
2. `products/<tier>/glossary.md` — product-specific terms
3. `handbooks/engineering/glossary.md` — engineering process terms

Don't duplicate a term across glossaries. Link to the canonical one.

## Skills

Procedural skills (multi-step agent procedures) live in `.claude/skills/`. They are different from the per-folder `skill.md` context files. See [.claude/skills/README.md](.claude/skills/README.md) for the registry.
