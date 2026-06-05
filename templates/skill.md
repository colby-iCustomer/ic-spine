# Agent context — templates/

- These are reusable skeletons. Treat them as read-only when working in other folders — copy + fill, never reference the template file directly from a PR or ticket.
- When asked to "open a PR for a bug fix," copy `templates/pr/bug.md` into the PR body and fill it in. Don't link to the template; the PR carries the filled content.
- Same pattern for Jira tickets — copy `templates/tickets/<type>.md` into the description.
- For new projects: follow `templates/projects/colby-project.md` to scaffold the project folder. The template describes the canonical structure; the actual project gets created via the `create-spine-project` skill (planned, see `.claude/skills/README.md`).
- Updates to template files require PR + at least one reviewer. Templates are upstream of every downstream process, so changes ripple.
- No em-dashes in any template content. Use hyphens, periods, semicolons.
