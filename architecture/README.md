# architecture/

What the iCustomer platform IS, in C4 terms.

This is structural documentation, not operational. If you want to know how to operate the system, see [handbooks/engineering/](../handbooks/engineering/). If you want to understand what the system consists of, you're in the right place.

## C4 model — four zoom levels

| Page | Level | Content |
|---|---|---|
| [landscape.md](landscape.md) | L0 — System Landscape | Three product-systems (ALoop, DOS, OneSource), Shared Platform, external systems, personas |
| [containers.md](containers.md) | L2 — Containers | The seven layers: Sources, Data Foundation, OneSource, AI Infrastructure, Decision Fabric, Activations, Governance |
| [components.md](components.md) | L3 — Components | Zoom into individual containers (OneSource, iConnect, Events) |
| [reference.md](reference.md) | Cross-cutting | Glossary, cross-cutting concerns (observability, Settings) |

L1 (System Context) and L4 (Code) are skipped. L1 is folded into landscape.md; L4 lives in the monorepo as actual code.

## C4 ↔ iCustomer mapping

| iCustomer | C4 element |
|---|---|
| Persona (CMO, CDO, GTM, dev) | Person (L1) |
| External AI Agents (A2A) | Person or External System |
| Warehouse, ad platforms, vendors, channels, Bedrock | External System |
| Audience Loop / Decision OS / OneSource | Software System |
| Shared Platform | Software System (holds shared containers) |
| Service (deployable) | Container (L2) |
| Component (e.g. iConnect) | Component (L3); if independently deployable → a Container |
| Layer (Data Foundation, etc.) | Boundary / group |

## Update cadence

🔥 **Hot right now** — the platform is actively being built pre-launch. Expect frequent updates through Q2. Post-launch, this folder should settle to Cold.

## Source

Content seeded from the `icustomer-docs/platform/` template (Vinod / engineering). Pages stubbed below — full content lands as engineering merges from `icustomer-docs`.
