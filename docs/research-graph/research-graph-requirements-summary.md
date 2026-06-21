# Research Graph — Requirements-Zusammenfassung

> **Typ**: Zusammenfassung (öffentlich sicher)
> **Quelle**: Privates Entwicklungsrepository (requirements.md der Research-Graph-Spec)
> **Status**: Kuratierter Auszug — vollständige Details verbleiben im privaten Repository

---

## Überblick

Die Research-Graph-Anforderungsspezifikation umfasst 48 formale Requirements in 14 Kategorien. Jedes Requirement folgt dem User-Story-Format mit WHEN/THEN-Akzeptanzkriterien.

---

## 14 Requirement-Kategorien

1. **Deep Dive Request Lifecycle** — Frage-Submission, Scope-Definition, State-Machine
2. **Background Research Task Model** — Langfristige Tasks, Timeout, Isolation
3. **Research Graph Entity Taxonomy** — 22 Entity-Typen, Uniqueness, Metadata
4. **Research Graph Relationship Model** — 18 Relationship-Typen, Provenance, Gewichtung
5. **Evidence Memory** — Append-only, Provenance-Chain, Source-Authorization
6. **Signal Memory** — Historische Signalverläufe, Trajectory-Tracking
7. **Narrative Memory** — Investment-Thesen, Story-Trajectories, Supporting/Contradicting
8. **Contradiction Handling** — Erkennung, Dokumentation, Surfacing
9. **Confidence and Uncertainty** — Scoring, Qualitative Labels, Multi-Dimensional
10. **Freshness and Staleness** — Zeitfenster, Verfallsregeln, Re-Evaluation
11. **Storage Classification** — 11 Datenklassen, Authority, Mutability
12. **Interaction Return Patterns** — Interim-Progress, Final-Draft-Delivery
13. **Governance Boundaries** — Authority-Enforcement, Prohibited Actions
14. **Documentation-Only Constraints** — Keine Runtime, keine Implementierung

---

## Schlüsselthemen

- **Evidenz-basiertes Reasoning** — Alle Schlussfolgerungen erfordern nachvollziehbare Evidenz
- **Contradiction Awareness** — Widersprüche werden sichtbar gemacht, nie unterdrückt
- **Freshness Management** — Veraltete Informationen werden als solche markiert
- **Provenance Chain** — Vollständige Herkunftskette für alle Evidenz-Stücke
- **Governance-First** — Alle 48 Requirements respektieren die Human-Authority-Grenze

---

## Governance-Axiome

- Das System produziert Research, keine Investitionsentscheidungen
- Der menschliche CTO ist die einzige Entscheidungsautorität
- Keine Portfolio-Mutation durch das System
- Keine autonome Agent-Ausführung
- Alle KI-Outputs sind Entwürfe
- 10 offene Entscheidungen bleiben explizit UNRESOLVED

---

## Spezifikationsdisziplin

- Jedes Requirement hat eine User-Story mit Rolle, Feature und Nutzen
- Akzeptanzkriterien im WHEN/THEN-Format
- Klare Trennung zwischen „Architektur definiert" und „Implementierung autorisiert"
- Documentation-Only Authority — keine Runtime-Erzeugung durch die Spec

---

*Vollständige 48 Requirements mit Akzeptanzkriterien verbleiben im privaten Entwicklungsrepository.*
