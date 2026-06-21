# Portfolio OS — Semantisches Signal-Modell

> **Typ**: Architektur-Zusammenfassung (öffentlich sicher)
> **Quelle**: Privates Entwicklungsrepository (Semantic Signal Registry + Semantic Reasoning Rules)
> **Status**: Kuratierter Auszug — vollständige Details verbleiben im privaten Repository

---

## Zweck

Das semantische Signal-Modell definiert das kanonische Vokabular und die Interpretationsregeln für Portfolio OS. Semantische Signale sind die Zwischenschicht zwischen Rohdaten und Reasoning — sie transformieren quantitative Metriken in sprachunabhängige, erklärbare Zustände.

---

## Signal-Eigenschaften

- **Sprachunabhängig** — Semantische Zustände sind nicht an natürliche Sprache gebunden
- **Deterministisch** — Gleiche Inputs erzeugen gleiche semantische Zustände
- **Erklärbar** — Jeder Zustand hat eine nachvollziehbare Herleitung
- **Wiederverwendbar** — Zustände werden von Reports, Dashboards und Reasoning konsumiert
- **Nachvollziehbar** — Jeder Zustand referenziert seine Quell-Signale

---

## Kernprinzipien

- **Keine direkte Verarbeitung von Rohdaten** — System erzeugt zuerst semantische Bedeutung
- **Kanonisches Vokabular** — Alle Systeme verwenden dasselbe Signal-Register
- **Signal-Hierarchie** — Signale sind nach Authority-Level und Domäne organisiert
- **Strukturelle Beziehungen** — Signale existieren nicht isoliert, sondern in Abhängigkeitsnetzwerken
- **Regelbasierte Transformation** — Von Signalen zu semantischen Zuständen über definierte Regeln
- **Keine KI-generierte Intuition** — Reasoning basiert auf Zuständen, nicht auf generativer Interpretation
- **Semantic Triggers** — Definierte Schwellwerte lösen Zustandsübergänge aus
- **Contradiction Awareness** — Widersprüchliche Signale werden sichtbar gemacht

---

## Verarbeitungskette

```
Rohdaten → Signal-Berechnung → Semantische Zustandserzeugung → PM-Reasoning → Report
```

Jede Stufe hat ein eigenes Authority-Level und darf nur innerhalb ihrer Befugnisse operieren.

---

## Governance-Integration

- Semantische Zustände sind SSOT — sie sind die kanonische Systemwahrheit
- Reports, Dashboards und Reasoning MÜSSEN diese Zustände konsumieren
- Keine Systemkomponente darf direkt aus Rohdaten schlussfolgern
- Änderungen am Vokabular erfordern den vollen Spec-Lifecycle

---

*Vollständige Signal-Registry und Reasoning-Regeln verbleiben im privaten Entwicklungsrepository.*
