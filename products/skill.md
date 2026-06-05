# Agent context — products/

- Each product folder follows the same shape: `README.md`, `positioning.md`, `state.md`, `glossary.md`, `feature-mind-map.md`, plus `features/` and `diagrams/` subfolders.
- `icustomer/` is brand-level (overarching), not a product tier. It doesn't have `features/` or `diagrams/`.
- Tier prefixes (`smb-`, `enterprise-`) are durable; don't rename folders when product names change. Update the README inside instead.
- `positioning.md` is a single doc designed to be website-readable. Pillars → personas → key use cases, in that order.
- `state.md` follows the Now / Next / Later pattern. Updated weekly-ish, not daily.
- `feature-mind-map.md` is a markdown file (not a mark map format). Slot for future auto-generated visualizations.
- `features/<slug>/` is populated by the promotion step — when a project ships, its artifacts move here.
- Glossary terms specific to one product live in that product's `glossary.md`. Platform-wide terms live in [architecture/reference.md](../architecture/reference.md). Don't duplicate.
