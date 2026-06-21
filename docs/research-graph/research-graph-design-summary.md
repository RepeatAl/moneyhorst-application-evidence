# Research Graph — Design-Zusammenfassung

> **Typ**: Zusammenfassung (öffentlich sicher)
> **Quelle**: Privates Entwicklungsrepository (design.md der Research-Graph-Spec)
> **Status**: Kuratierter Auszug — vollständige Details verbleiben im privaten Repository

---

## Überblick

Das Research-Graph-Design definiert die konzeptuelle Architektur für das Deep-Dive-System. Es spezifiziert das Schichtenmodell, Entity-/Relationship-Taxonomien, Workflow-Lifecycle, Datenmodelle und Governance-Grenzen.

---

## Architektur-Dimensionen

| Dimension | Umfang |
|-----------|--------|
| Layers | 7 + 1 Report-Emission-Layer |
| Entity-Typen | 22 kanonische Typen |
| Relationship-Typen | 18 gerichtete, typisierte Kantentypen |
| Lifecycle-Zustände | 12 validierte Workflow-Zustände |
| Correctness Properties | 14 formale Korrektheitseigenschaften |
| Storage-Klassifikation | 11 Datenklassen |
| Open Decisions | 10 — alle explizit UNRESOLVED |

---

## Schichtenmodell

1. **Interaction Layer** — User-Facing, Frage und Ergebnis
2. **Research Orchestration** — Dekomposition und Task-Koordination
3. **Background Research** — Langfristige Evidence-Sammlung
4. **Research Graph** — Entity-Traversierung und Anreicherung
5. **Evidence Layer** — Provenance-verknüpfte Evidenz-Speicherung
6. **Memory Layer** — Signal-, Narrative- und Contradiction-Memory
7. **Governance Layer** — Authority- und Scope-Enforcement
8. **Report Layer** — Draft-Emission (nie finale Entscheidung)

---

## Correctness Properties (14)

Die 14 Korrektheitseigenschaften validieren:

- State-Machine-Integrität (keine ungültigen Übergänge)
- Entity-Uniqueness (keine Duplikate im Graph)
- Provenance-Completeness (jede Evidenz hat vollständige Herkunft)
- Relationship-Validity (nur erlaubte Entity-Kombinationen)
- Authority-Boundary-Integrity (keine Überschreitung)
- Freshness-Enforcement (veraltete Daten markiert)
- Contradiction-Surfacing (Widersprüche nie unterdrückt)
- Read-Only Research (keine Schreiboperationen auf SSOT)
- Draft-Classification (alle Outputs als Entwürfe markiert)
- Taxonomy-Governance (keine autonome Typ-Erweiterung)

---

## Design-Constraints

- Documentation-Only — kein Runtime-Code autorisiert
- Keine Storage-Technologie-Entscheidung — deferred
- Consumer Pattern — Deep-Dive konsumiert existierende Frameworks
- Human Authority preserved — Research-Output hat keine Entscheidungsbefugnis
- 10 offene Design-Entscheidungen bleiben explizit ungelöst

---

*Vollständige Design-Architektur mit Datenmodellen und Interface-Spezifikationen verbleibt im privaten Entwicklungsrepository.*
