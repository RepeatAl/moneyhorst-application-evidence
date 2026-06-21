# Research Graph & Deep Dive — Architektur-Überblick

> **Typ**: Zusammenfassung (öffentlich sicher)
> **Quelle**: Privates Entwicklungsrepository (Spec: moneyhorst-research-graph-deep-dive-architecture)
> **Status**: Kuratierter Auszug — vollständige Details verbleiben im privaten Repository

---

## Zweck

Der Research Graph ist die Intelligenzschicht zwischen fragmentierten Portfolio-Informationen und kohärentem, evidenzbasiertem Research-Kontext für menschliche Entscheidungsfindung. Er verbindet Signale, Narrative, Evidenz und Entitäten zu einem traversierbaren Wissensgraph.

---

## Leitprinzip

**Signale entscheiden. System interpretiert. Mensch entscheidet.**

Das Deep-Dive-System produziert Research-Intelligence. Es produziert KEINE Investitionsentscheidungen, Portfolio-Mutationen oder autonome Aktionen.

---

## Schichtenmodell (7+1 Layers)

| Schicht | Rolle |
|---------|-------|
| 1. Interaction Layer | Nutzer stellt Frage, erhält Research-Ergebnis |
| 2. Research Orchestration | Dekomposition komplexer Fragen in Research-Tasks |
| 3. Background Research | Langfristige Research-Tasks mit Timeout-Boundaries |
| 4. Research Graph Layer | Entity/Relationship-Traversierung und Anreicherung |
| 5. Evidence Layer | Quell-, Snapshot- und Zitations-Speicherung mit Provenance |
| 6. Memory Layer | Signal-, Narrative- und Widerspruchs-Memory |
| 7. Governance Layer | Authority-, Scope-, Konfidenz- und Provenance-Prüfung |
| Report Layer (Emission) | Deep-Dive-Entwurf — NICHT finale Entscheidung |

---

## Entity-Taxonomy (22 Typen)

Kanonische Entity-Typen umfassen unter anderem: Asset, Issuer, Sector, Theme, Signal, Narrative, Evidence, Contradiction, Research-Task, Market-Regime, Dependency, Risk-Factor und weitere. Jeder Typ hat definierte Metadata-Anforderungen und Governance-Regeln.

---

## Relationship-Taxonomy (18 Typen)

Gerichtete, typisierte, gewichtete Kanten mit Provenance und Freshness-Metadata verbinden Entitäten. Beziehungstypen umfassen: supports, contradicts, depends_on, correlates_with, signals, enriches, und weitere.

---

## Deep-Dive-Workflow-Lifecycle (12 Zustände)

REQUESTED → SCOPED → DECOMPOSED → RESEARCHING → EVIDENCE_COLLECTED → SYNTHESIZING → CONFIDENCE_SCORED → CONTRADICTION_CHECKED → DRAFT_READY → HUMAN_REVIEWED → APPROVED → ARCHIVED

Jeder Zustandsübergang ist validiert — keine Überspringung möglich.

---

## Governance-Boundaries

- Keine autonome Research-Ausführung ohne definierte Scope-Grenzen
- Research-Outputs sind stets Entwürfe (AGENT_DRAFT / RESEARCH_DRAFT)
- Evidence ist append-only — keine nachträgliche Manipulation
- Nur autorisierte Quellen fließen in den Graph ein
- Widersprüche werden dokumentiert, nicht unterdrückt
- DEFERRED-Entscheidungen bleiben ungelöst bis CTO-Authority vorliegt

---

## Documentation-Only Authority

Diese Architektur-Spezifikation autorisiert ausschließlich Dokumentation — keine Runtime-Implementierung, keine Speicher-Bereitstellung, keine Agent-Ausführung.

---

*Vollständige Entity-/Relationship-Taxonomie, Workflow-Details und Governance-Regeln verbleiben im privaten Entwicklungsrepository.*
