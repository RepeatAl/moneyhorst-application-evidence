# Sicherheitsrichtlinie

## Grundsatz

Dieses Repository darf KEINE sensiblen Daten enthalten.

## Verbotene Inhalte

- Keine Secrets, API-Keys, Tokens oder Passwörter
- Keine Portfolio- oder Trading-Daten
- Keine Broker- oder Depot-Informationen
- Keine Credentials oder Zugangsdaten
- Keine personenbezogenen Daten (PII)
- Keine WKN/ISIN oder Wertpapier-Identifikatoren
- Keine Positionsgrößen oder Kontoinformationen

## Bei Entdeckung sensibler Daten

Falls sensible Daten in diesem Repository entdeckt werden:

1. Repository SOFORT auf privat setzen
2. Betroffene Commits aus der Historie entfernen (git filter-branch oder BFG)
3. Alle betroffenen Credentials rotieren
4. Erst nach vollständiger Bereinigung wieder öffentlich stellen

## Kontakt

Repository-Inhaber: RepeatAl

## Präventive Maßnahmen

- Vor jedem Commit: Safety-Scan auf Secrets, Credentials und sensible Daten
- Keine automatisierten Pipelines mit Schreibzugriff auf sensible Systeme
- Regelmäßige Überprüfung der Repository-Inhalte
