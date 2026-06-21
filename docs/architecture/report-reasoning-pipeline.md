# Portfolio OS — Report-Reasoning-Pipeline

> **Typ**: Architektur-Zusammenfassung (öffentlich sicher)
> **Quelle**: Privates Entwicklungsrepository (Report Reasoning System + Report Pipeline Architecture)
> **Status**: Kuratierter Auszug — vollständige Details verbleiben im privaten Repository

---

## Zweck

Die Report-Reasoning-Pipeline definiert, wie Portfolio OS erklärbare Portfolio-Intelligence-Reports konstruiert. Das Report-System ist KEIN Textgenerator — es ist ein deterministischer Reasoning-Orchestrator, der Portfolio-Signale synthetisiert, Zustände erklärt und Handlungsräume aufzeigt.

---

## Verarbeitungsziel

Der Report erklärt dem Nutzer:

- Was relevant ist und warum
- Den aktuellen Portfolio-Zustand und Marktkontext
- Abhängigkeiten und Konzentrations-Risiken
- Szenario-Risiken und Tradeoffs
- Den verfügbaren Handlungsraum

---

## Kernprinzipien

- **Reasoning, nicht Textgenerierung** — Reports basieren auf strukturierter Logik, nicht auf KI-Narration
- **Deterministische Orchestrierung** — Pipeline-Stufen sind definiert und wiederholbar
- **Signal-zu-Report-Kette** — Jeder Report-Abschnitt referenziert seine Quell-Signale
- **Mehrstufige Verarbeitung** — Von Rohdaten über Signale und Semantik zu Reports
- **Evidence-Referenzen** — Reports zitieren ihre Evidenz-Grundlage
- **Keine autonomen Empfehlungen** — Reports erklären, empfehlen nicht
- **Erklärbarkeit** — Jede Aussage im Report ist auf Signalquellen rückführbar
- **Governance-konform** — Report-Outputs tragen AGENT_DRAFT-Klassifikation

---

## Pipeline-Stufen

| Stufe | Input | Output |
|-------|-------|--------|
| Signal Collection | Rohdaten, Market-Feed | Quantitative Signale |
| Semantic Transformation | Signale | Semantische Zustände |
| PM Reasoning | Semantische Zustände | Reasoning-Objekte |
| Report Orchestration | Reasoning-Objekte | Strukturierte Report-Segmente |
| Narrative Assembly | Report-Segmente | Erklärbare Berichtsabschnitte |
| Citation & Evidence | Alle Stufen | Evidenz-Referenzen und Provenance |

---

## Governance-Integration

- Reports sind stets als Entwürfe klassifiziert (AGENT_DRAFT / RESEARCH_DRAFT)
- Keine Report-Ausgabe ersetzt menschliche Entscheidung
- Report-Pipeline-Änderungen durchlaufen den Spec-Lifecycle
- Contradiction-Detection ist in die Pipeline integriert

---

*Vollständige Pipeline-Architektur und Reasoning-Regeln verbleiben im privaten Entwicklungsrepository.*
