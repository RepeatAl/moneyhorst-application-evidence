# MoneyHorst / Portfolio OS — Public-Safe Technical Showcase

> **Typ**: Öffentlich teilbares Showcase-Dokument
> **Datum**: 2026-06-21
> **Status**: Dokumentationsbasiert — keine vertraulichen Daten enthalten
> **Sprache**: Deutsch

---

## Kurzprofil

MoneyHorst / Portfolio OS ist ein dokumentationsgesteuertes Architekturprojekt für Portfolio-Intelligence-Systeme. Das Projekt demonstriert Fähigkeiten in Systemarchitektur, KI-Orchestrierung, Datenmodellierung, Governance-First-Engineering und strukturierter Prozessautomatisierung.

Es handelt sich NICHT um einen Trading-Bot, NICHT um ein autonomes Investment-System und NICHT um einen Finanzberater. Alle finalen Entscheidungen verbleiben unter menschlicher Kontrolle.

---

## Technischer Fokus

- Systemarchitektur mit 12-Domänen-Separation
- Signal-zu-Semantik-zu-Reasoning-Verarbeitungskette
- Konfidenz-Scoring und Marktregime-Klassifikation
- Report-Reasoning-Pipeline mit mehrstufiger Orchestrierung
- Research-Graph-Architektur für Evidenz-Traversierung
- Evidence-Memory mit Provenance-Chain-Anforderungen
- Portfolio-Zustandsmodellierung und Asset-Registry
- Deployment-Intelligence und Governance-Boundaries
- Kommunikations- und Sicherheitsarchitektur
- UI/UX-Architektur mit Figma-Governance

---

## Architekturprinzipien

- **SSOT (Single Source of Truth)**: Jedes Artefakt hat eine kanonische Quelle
- **Engine Separation**: Unabhängige, modulare Verarbeitungseinheiten
- **Consumer Pattern**: Systeme lesen voneinander, schreiben nicht zurück
- **Layered Architecture**: Klare Schichtentrennung mit definierten Authority-Levels
- **Documentation-First**: Architektur wird dokumentiert bevor implementiert wird
- **Spec-Lifecycle**: Preflight → Requirements → Design → Tasks → Execution

---

## Governance und Human Authority

- Alle finalen Entscheidungen erfordern menschliche Freigabe
- Keine autonome Investitionsentscheidung durch das System
- Keine Portfolio-Mutation ohne explizite Genehmigung
- Verification Gates mit Artefakt-Nachweis
- Open Decisions werden explizit als ungelöst markiert
- KI-Outputs sind stets als Entwürfe klassifiziert
- Kein Handelsbefehl, keine Position-Sizing-Automatik

---

## KI-/AI-Orchestrierung

- KI-gestützte Architekturentwicklung mit ChatGPT und Kiro
- Prompt-basierte Steuerung innerhalb definierter Boundaries
- Multi-Agent-Governance (AGENTS.md, Steering-Files)
- Architektur-Hardening über iterative Spec-Verfeinerung
- Research-Only AI Output: KI produziert Entwürfe, keine Entscheidungen
- Formale Verbotslisten für KI-Agenten

---

## Daten-, Signal- und Evidence-Modellierung

- Kanonischer Portfolio-Zustand mit Snapshot-Fähigkeit
- Signal-Berechnung und semantische Zustandserzeugung
- Konfidenz als epistemische Stabilität, nicht als Vorhersagegenauigkeit
- Evidence-Memory mit Provenance, Freshness und Integrity-Regeln
- Source-Authorization-Modell für Evidenz-Quellen
- Contradiction-Handling: Widersprüche werden sichtbar gemacht, nicht unterdrückt
- Freshness-Management: Veraltete Daten werden als veraltet markiert

---

## Prozess- und Automatisierungslogik

- Lifecycle-State-Machine für Artefakt-Management
- Pre-Commit-Hooks für Governance-Enforcement
- CI-Pipeline mit Observability-Checks
- Automatisierte Format-Prüfung (Spec Format Checker)
- Typisierte Commits mit Domain-Separation
- Branch-Governance mit Prefix-Validierung
- Strukturierte Task-Ausführung mit Execution-Reports

---

## Relevanz für IT / KI / Automation

| Anforderungsbereich | Demonstrierte Fähigkeit |
|---------------------|------------------------|
| No-Code/Low-Code | Dokumentations- und konfigurationsgesteuerte Architektur |
| API/SaaS | Schichtenmodell mit definierten Interfaces und Pipeline-Orchestrierung |
| KI-Orchestrierung | Multi-Agent-Steuerung, Prompt-Engineering, Governance-Hooks |
| Datenmodellierung | 12-Domänen-Modell, YAML-Registries, Schema-Governance |
| Prozessautomatisierung | Lifecycle-Machine, Enforcement-Runtime, CI-Hooks |
| Dokumentation | 80+ Execution-Reports, Markdown-SSOT, Requirement-Coverage |
| Troubleshooting | Drift-Detection, Audit-Ledger, Forensik-Reports |
| Governance | HAG-Gates, Verification-Gates, Branch-Governance |

---

## Sicherheits- und Integritätsgrenzen

- Keine vertraulichen Portfolio-Bestände in diesem Dokument
- Keine Handelsempfehlungen oder -anweisungen
- Keine Secrets, Passwörter oder API-Schlüssel
- Keine personenbezogenen Daten Dritter
- Keine Code-Auszüge oder Implementierungsdetails
- Keine Finanzberatung
- Dieses Projekt ist ein Architektur-Demonstrationsprojekt, kein Produktivsystem

---

*Dokumentationsbasiert. Keine Implementierungsfreigabe. Keine autonome Investitionsentscheidung.*
