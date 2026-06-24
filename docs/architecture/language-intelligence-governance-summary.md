# Language Intelligence Governance — Architecture Summary

> **Spec**: moneyhorst-language-intelligence-governance
> **Status**: MERGED — PR #86
> **Date**: 2026-06-24
> **Authority**: CTO / Architecture
> **Implementation Authorized**: NO

---

## Overview

MoneyHorst Language Intelligence Governance defines platform-wide rules for how canonical semantic meaning is rendered into user-facing language. It is a cross-cutting governance layer that affects all current and future specs with user-facing text.

The spec was completed as documentation-only architecture with 14 tasks, 95 artifacts, 72 requirements, and 14 correctness properties. All 16 open governance decisions were resolved by explicit CTO decision using best-practice user-friendly defaults.

---

## Core Principles

1. **Semantics are system truth.** Canonical meaning is language-independent.
2. **Language is rendering.** Display language is a view of truth, not truth itself.
3. **Translation must never mutate canonical meaning.** No translation may alter, soften, or reinterpret semantic content.

---

## Key Decisions

| # | Decision | Resolution |
|---|----------|-----------|
| 1 | Initial languages | German (primary) + English (fallback) |
| 2 | Default language | German for DACH deployment |
| 3 | Preference storage | Profile-level (future implementation) |
| 4 | Report language override | Allowed as future capability |
| 5 | Locale formatting | DACH: DD.MM.YYYY, decimal comma / English: standard |
| 6 | Terminology ownership | CTO governance |
| 7 | Fallback rules | English fallback, always visible |
| 8 | Review authority | CTO-approved human reviewers |
| 9 | Source-language display | Source visible, metadata preserved |
| 10 | Bilingual reports | Allowed for evidence-heavy workflows |
| 11 | CRM/support language | User preference, reviewed templates |
| 12 | Notification language | User preference, no urgency amplification |
| 13 | Governance labels | Stable IDs + localized explanation |
| 14 | Machine translation | Draft/internal only, labeled |
| 15 | Human review conditions | Finance/governance/public content |
| 16 | Citation integrity | Boundary preservation through translation |

---

## Scope

The spec governs:
- Canonical meaning boundary and non-identity rules
- Language preference and locale governance
- Terminology registry governance
- Governance label translation with severity preservation
- Surface language policies (UI, dashboard, account, onboarding)
- Report and research output language
- Source/citation language integrity
- Notification and alert language
- Subscription/access language
- Fallback and error state handling
- Translation quality and human review boundaries
- Cross-spec consumption and future scalability
- Controlled glossary governance

---

## Governance Boundaries

This spec does NOT authorize:
- Runtime implementation
- i18n/translation service integration
- Frontend/backend/API code
- Storage/database/schema changes
- CRM/notification/subscription implementation
- Portfolio mutation, SAI mutation, HAG/VG execution
- Trading/broker actions

---

## Completion Evidence

- 14/14 tasks complete
- 95 artifacts created
- R1–R72 requirements covered
- 14 correctness properties verified
- 16/16 open decisions resolved by CTO
- Platform Control Map integration complete
- PR #86 merged into main (squash merge)
- Merge commit: `cc997aadae00e726c993f0722722c01d5431dc5c`

---

## Relationship to Other Specs

- Consumes: `multilingual_rendering_framework.md`, `README_language_rendering_framework.md`
- Integrates with: Deep Dive report contract, `decision_governance.md`, `semantic_signal_registry`
- Future consumers: Identity/Profile, Onboarding, Dashboard, CRM, Notifications, Subscription specs

---

## Status

**LANGUAGE_INTELLIGENCE_GOVERNANCE_MERGED — DOCUMENTATION_ONLY — NO_IMPLEMENTATION_AUTHORIZED**
