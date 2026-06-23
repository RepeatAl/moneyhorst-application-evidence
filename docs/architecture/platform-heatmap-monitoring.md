# Platform Control Map & Functional Heatmap Monitoring

> **Type**: Architecture Evidence Document
> **Status**: ACTIVE
> **Date**: 2026-06-22
> **Authority**: CTO / Architecture
> **Scope**: Platform-wide governance monitoring
> **Implementation Authorized**: NO

---

## Purpose

MoneyHorst now maintains a platform-level monitoring layer that provides visibility into spec lifecycle, task progress, implementation readiness, unresolved decisions, dependencies, and functional-layer coverage across all platform areas.

This monitoring layer is an architectural governance and evidence artifact. It is not runtime, not automatic execution logic, and not a product feature.

---

## Monitoring Artifacts

| Artifact | Purpose |
|----------|---------|
| `platform_control_map.md` | Top-level platform layer heatmap with status per area |
| `spec_lifecycle_matrix.md` | All specs with lifecycle phase tracking |
| `functional_layer_heatmap.md` | Product/architecture capability status per functional layer |
| `implementation_readiness_matrix.md` | Architecture readiness vs implementation authority separation |
| `dependency_map.md` | Cross-layer and cross-spec dependency tracking |
| `open_decision_register.md` | Cross-spec unresolved decisions with resolution paths |

---

## Architectural Role

The monitoring layer serves:

1. **CTO review** — provides single-view visibility into platform-wide progress
2. **Drift detection** — surfaces when specs or functional layers diverge from governance expectations
3. **Scope control** — confirms what is authorized vs what remains blocked
4. **Implementation-readiness visibility** — separates architecture completeness from implementation permission
5. **Cross-spec consistency** — tracks dependencies and ensures governance consumption chains are intact

---

## What the Heatmap Is NOT

- Not a runtime feature
- Not automatic execution logic
- Not a monitoring dashboard (no UI, no service, no API)
- Not investment authority
- Not execution authority
- Not product runtime behavior
- Not a trading signal or recommendation engine

---

## Task Closure Integration

Starting from the MoneyHorst Language Intelligence Governance Task 5 closure model, every governed task execution cycle requires a mandatory Platform Control Map update as part of task closure.

A task is not considered fully closed until:
- Task artifacts are committed on the spec branch
- Platform control map update is committed on the governance branch
- Both commits are pushed
- Working branch returns to the spec branch

This ensures the monitoring layer always reflects current system state.

---

## Governing Principles

- **Semantics are system truth.** The monitoring layer reports state; it does not create meaning.
- **Language is rendering.** The heatmap displays status; it does not authorize action.
- **Signals decide, system interprets, human decides.** The heatmap informs the CTO; it does not replace judgment.
- **No autonomous investing.** The monitoring layer has no execution authority.
- **No trading bot.** No trading actions derive from monitoring state.
- **No implementation without CTO authorization.** The heatmap reports readiness; it does not grant permission.

---

## Evidence Note

This monitoring architecture became mandatory from the MoneyHorst Language Intelligence Governance spec, specifically from the Task 5 closure model (commit `8fcc2b2` on branch `spec/moneyhorst-language-intelligence-governance-preflight`). The hardening commit (`e1e1c20`) formalized the Platform Control Map Update Protocol and Task Closure Definition requiring both a language task commit and a platform control update commit for every task cycle.

---

## Status

**EVIDENCE_REPO_PLATFORM_HEATMAP_MONITORING_DOCUMENTED**
