# products/

One folder per product. Plus a brand-level folder for iCustomer overall.

## Structure

```
products/
├── icustomer/                   ← brand-level (overarching positioning, not a product tier)
├── smb-audience-loop/           ← SMB tier (formerly "ALoop")
├── enterprise-decision-os/      ← Enterprise tier (formerly "Decision OS")
└── onesource/                   ← Developer / API tier
```

Tier prefixes (`smb-`, `enterprise-`) are intentional — they're future-proof against product rename. If "Audience Loop" gets a new name, we still know which folder holds the SMB product.

## Per-product files

Each product folder contains:

- `README.md` — product overview, what it is, who owns it
- `positioning.md` — pillars, personas, key use cases. Single doc, website-readable.
- `state.md` — Now / Next / Later. Current state of the product, fast-moving.
- `glossary.md` — product-specific terms (the ALoop glossary is different from the Decision OS glossary)
- `feature-mind-map.md` — mind map of features. Slot for auto-generated content later.
- `features/` — one subfolder per shipped + maintained feature (post-promotion from `projects/`)
- `diagrams/` — flow charts, mind maps, anything visual

## Update cadence

❄️ **Cold** for positioning + glossary. Update when the product story shifts.
🌡️ **Warmer** for `state.md` — Now/Next/Later moves with the team's quarterly + weekly plans.

## Ownership

| Product | Owner |
|---|---|
| icustomer (brand) | Abhi |
| smb-audience-loop | Colby |
| enterprise-decision-os | (TBD — likely Iqbal or Jinesh) |
| onesource | (TBD — likely Vinod or Jeeva) |
