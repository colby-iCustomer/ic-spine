# Reference — cross-cutting + platform glossary

> Stub. Full content lands when engineering merges from `icustomer-docs/platform/reference.md`.

## Cross-cutting concerns

- **Observability & Ops** (vertical, spans all layers) — logging, metrics, tracing, decision monitoring
- **Settings** (horizontal) — 12 MECE sections: Account, Workspace, Platform, Data, Intelligence, Agents, Decisioning, Channels, Registry·Capabilities, Registry·Models, Registry·Strategy, Registry·External

## Platform glossary

| Term | Definition |
|---|---|
| **Decision Context Layer** | iCustomer's positioning — the orchestration middle between data and channels |
| **Decision Traces** | Audit trail of every decision the platform makes |
| **FIRE scoring** | Fit, Intent, Recency, Engagement — the standard scoring model |
| **iWorkers** | Role-based digital twins; OODA loop + causal AI |
| **Immutable ID** | HMAC-SHA-256 deterministic identifier from OneSource |
| **Three-axis model (S×W×L)** | Scope/Authority × Reasoning Ladder × Decisioning Waterfall (L0-L6) |

## C4 conventions

- L0: System Landscape
- L1: System Context (folded into landscape.md)
- L2: Containers (our "Services")
- L3: Components
- L4: Code (skipped here; lives in monorepo)
