# Containers — L2

> Stub. Full content lands when engineering merges from `icustomer-docs/platform/containers.md`.

The Shared Platform's deployable units (Services) grouped by Layer (boundary).

## Layers, bottom-up

1. **Sources** — Signals + Events. Warehouse-native, zero-ETL.
2. **Data Foundation** (Data Manager) — substrate: Snowflake / BigQuery / Databricks, read in place.
3. **OneSource** — Identity (Immutable ID, DID) + Enrichment (waterfall + cooperative).
4. **AI Infrastructure** (Registry Manager) — Inference router, model registry, hybrid SLM/LLM via Bedrock + Neurometric.
5. **Decision Fabric** (Intelligence Manager) — Decision Engine, Harness, iWorkers, Intelligence. Three-axis model (S×W×L), Decision Traces, FIRE scoring. Orchestration via Temporal.io.
6. **Governance** — Policy, permissions, compliance, decision oversight.
7. **Activations** (Activation Manager) — iConnect (MCP), Audience Sync, Destination Connectors.

Mermaid C4 diagram → port from `icustomer-docs/platform/containers.md`.
