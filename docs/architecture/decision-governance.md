# Portfolio OS — Decision Governance

> **Typ**: Governance-Zusammenfassung (öffentlich sicher)
> **Quelle**: Privates Entwicklungsrepository
> **Status**: Kuratierter Auszug — vollständige Details verbleiben im privaten Repository

---

## Zweck

Das Decision-Governance-Modell definiert die Entscheidungsprinzipien und KI-Rollengrenzen für Portfolio OS. Das System ist KEIN autonomes Investment-KI-System — es ist ein signalgetriebenes PM-Reasoning-System.

---

## Leitprinzip

**Signale entscheiden. System interpretiert. Mensch entscheidet.**

Das System erfindet keine Entscheidungen. Es sammelt Signale, bewertet Signal-Alignment, interpretiert Portfolio-Bedingungen, erklärt mögliche Handlungsräume und unterstützt menschliches Portfolio-Reasoning.

---

## Kernprinzipien

- **Keine autonomen Investitionsentscheidungen** — System produziert Research, keine Aktionen
- **Signal-basierte Schlussfolgerung** — Alle Konklusionen basieren auf messbaren Bedingungen
- **Explizite Authority-Level** — Klare Trennung zwischen System-Output und menschlicher Entscheidung
- **DEFERRED-Markierung** — Ungeklärte Entscheidungen werden explizit als ungelöst gekennzeichnet
- **No Auto-Resolution** — KI-Agenten dürfen keine offenen Entscheidungen auflösen
- **Verification Gates** — Unabhängige Prüfpunkte mit Evidenz-Anforderung
- **HAG-STAGE-Gates** — Mehrstufige Human Authority Gates für Produktionsentscheidungen
- **KI als Entwurfsassistent** — Alle KI-Outputs sind AGENT_DRAFT / RESEARCH_DRAFT
- **Audit Trail** — Jede Governance-Mutation wird protokolliert
- **Fail-Mode-Configuration** — Definiertes Systemverhalten bei Regelverstoß

---

## Authority-Hierarchie

| Level | Beschreibung |
|-------|-------------|
| Level 1 | Signalberechnung — rein quantitativ |
| Level 2 | Semantische Interpretation — regelbasiert |
| Level 3 | Reasoning — strukturierte Schlussfolgerung |
| Level 4 | Report-Emission — erklärbare Zusammenfassung |
| CTO | Finale Entscheidungshoheit — nicht delegierbar |

---

## Verbotene Aktionen

- Keine Portfolio-Mutation ohne explizite menschliche Genehmigung
- Keine autonome Trading-Entscheidung
- Keine Auflösung offener Entscheidungen durch Zeitablauf oder Inferenz
- Keine KI-generierte Genehmigung
- Keine SAI-Mutation durch das System

---

*Vollständige Governance-Details verbleiben im privaten Entwicklungsrepository.*
