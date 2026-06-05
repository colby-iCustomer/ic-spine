# templates/

Process artifacts. Reusable skeletons for PRs, tickets, and projects.

## Structure

```
templates/
├── skill.md          (how agents should use these templates)
├── pr/               (PR description templates per change type)
├── tickets/          (Jira ticket templates per type)
└── projects/         (project scaffolding pattern)
```

## When to update

🥶 **Freezing** — process artifacts only change when the underlying process changes. If a PR template is being edited monthly, the process is unstable. Stabilize the process, then update the template.

## How to use

| Template type | When to apply |
|---|---|
| `pr/feature.md` | Opening a PR that adds a new feature |
| `pr/bug.md` | Opening a PR that fixes a bug |
| `pr/spike.md` | Opening a PR documenting a research / investigation spike |
| `pr/refactor.md` | Opening a PR that refactors without behavior change |
| `tickets/bug.md` | Filing a bug in Jira |
| `tickets/task.md` | Filing a task in Jira |
| `tickets/story.md` | Filing a story in Jira |
| `tickets/spike.md` | Filing a spike in Jira |
| `projects/colby-project.md` | Creating a new project under `projects/` — describes the canonical scaffold |
