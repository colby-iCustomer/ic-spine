# Agent context — architecture/

- C4 model documentation. Context (L0) → Container (L2) → Component (L3). Code level (L4) is skipped — lives in the monorepo.
- Diagrams are Mermaid C4 inside fenced ```mermaid blocks. Keep them small — Mermaid C4 has no auto-layout.
- DON'T duplicate engineering operational content (SDLC, CI/CD, ADRs) here — that lives in [handbooks/engineering/](../handbooks/engineering/).
- Glossary terms specific to platform structure (Decision Trace, FIRE, Immutable ID, three-axis model) live in `reference.md`. Other glossaries live elsewhere.
- When adding a new container, update both `containers.md` (mention) and create a corresponding L3 zoom in `components.md` if the container has > 2 components.
- Source for current content: `icustomer-docs/platform/` in the engineering team's draft repo.
