# Spine Skills (registry)

> Procedural skills for spine-aware work. Each skill is a multi-step procedure invoked as `/<skill-name>`. Different from the per-folder `skill.md` files (which are short context cheat-sheets for agents editing that folder).

## Planned skills (Day 1 stubs — to be ported in a follow-up project)

| Skill | Purpose | Source pattern |
|---|---|---|
| `create-spine-project` | Scaffold a new project under `projects/<stream>/<owner>/<slug>/` with brief / state / notes / deliverables / working / sources. Update `projects/index.md` (Active). | Modeled on `pm-create-project` from `ic-product-mgmt` |
| `promote-project` | Move a finished project's artifacts from `projects/<stream>/<owner>/<slug>/` into its permanent home (`products/<tier>/features/`, `design-guide/`, `handbooks/<audience>/`). Update `projects/index.md` to `Promoted`. | New |
| `update-product-state` | Edit `products/<tier>/state.md` with current now / next / later items. | New |
| `update-positioning` | Edit `products/<tier>/positioning.md` (pillars, personas, use cases). | New |
| `update-feature-mind-map` | Update or regenerate `products/<tier>/feature-mind-map.md`. | New (auto-gen later) |

## Out of scope for these skills

- Meeting extraction, triage, sprint planning — those live in `ic-product-mgmt/.claude/skills/`
- Jira posting — same; Jira lives in the PM repo's workflow

## Convention

Each skill folder will follow the `SKILL.md` pattern used in `ic-product-mgmt`:

```
.claude/skills/<skill-name>/
├── SKILL.md              ← human + agent-readable instructions
└── (optional templates, references)
```

## Status

Day 1 (scaffold): folder + this README only. Skills will be ported in a focused follow-up after the team agrees on the structure and concurrency model.
