# MoneyHorst — User Identity / Account / Profile Architecture Summary

> **Spec**: moneyhorst-user-identity-account-profile
> **Phase**: Requirements complete — ready for design
> **Date**: 2026-06-25
> **Status**: Documentation-only architecture specification
> **Implementation Authorized**: NO
> **Public-Safe**: YES — no user data, no holdings, no credentials

---

## Overview

This spec defines the architecture boundaries for user identity, account, and profile within MoneyHorst. It establishes what these concepts mean, where preferences live, how account lifecycle works, and how external portfolio import fits as a core profile capability — all without implementing anything.

This is the sixth MoneyHorst architecture spec to reach requirements completion. It unblocks six downstream specs (onboarding, dashboard, roles/permissions, CRM, notifications, subscriptions).

---

## What This Spec Defines

### Identity Boundary

Identity answers: "Who is this actor in the system?"

- Stable, canonical, system-internal identifier (not email, not username)
- Actor types: human user, system agent, service identity
- Provider-agnostic authentication reference
- Identity state machine: active → suspended → deactivated
- Identity is NOT preferences, NOT permissions, NOT profile data

### Account Boundary

Account answers: "What is the operational container for this identity?"

- Account lifecycle: PENDING → ACTIVE → SUSPENDED → DEACTIVATED
- Account owns: subscription reference, governance authority level
- Account deactivation preserves all governance artifacts and data integrity
- Reactivation requires explicit human CTO override

### Profile Boundary

Profile answers: "What are this user's preferences and personalizations?"

- Language preferences (UI, reports, communication — three independent preferences)
- Locale preference (dates, numbers, currency formatting — independent from language)
- Timezone preference
- Notification preferences
- Imported portfolio records (Bestandportfolio)

### Core Rule: Preferences Are Never Authority

Changing any profile preference (language, locale, timezone) NEVER alters governance state, portfolio truth, evidence meaning, or system authority. Preferences control the rendering layer only.

---

## External Portfolio Import — Architecture Boundary

Portfolio import is a core profile/account capability:

- Users can upload portfolio exports from external brokers, banks, asset managers, or spreadsheets
- Supported formats (CSV, XLSX, PDF, broker-specific) remain open decisions
- Uploaded files are classified as sensitive financial data (encrypted storage required)
- Imported holdings pass through asset identity normalization (ticker, ISIN, WKN, exchange, currency, asset type, sector classification)
- Ambiguous or unresolved assets are NEVER silently assumed — user confirmation is mandatory
- Only after explicit user confirmation do imported holdings become canonical portfolio data
- Users assign labels to portfolios (e.g., "Main Portfolio", "Broker Portfolio", "Bestandportfolio")
- Future reports clearly distinguish imported Bestandportfolio from watchlist assets, simulated allocations, and research recommendations

### What Portfolio Import Does NOT Do

- Does NOT generate buy/sell/hold recommendations
- Does NOT trigger trading signals or execution instructions
- Does NOT authorize autonomous action of any kind
- Does NOT implement parsers, storage, APIs, or UI
- Reports referencing imported portfolios remain classified as RESEARCH_DRAFT

---

## Language Preference Ownership

This spec resolves Language Intelligence Governance Open Question #3: "Where is per-user language preference stored?"

**Answer:** Language preferences are Profile-layer attributes owned by this spec's domain.

| Preference | Scope | Governance |
|-----------|-------|-----------|
| User Language Preference | Platform UI display | Language Intelligence Governance R8 |
| Report Language Preference | Research report rendering | Language Intelligence Governance R9 |
| Communication Language Preference | Notifications, CRM, support | Language Intelligence Governance R10 |
| Locale Preference | Date/number/currency formatting | Language Intelligence Governance R14 |

---

## Downstream Specs Unblocked

| Downstream Spec | What It Consumes From Identity |
|----------------|-------------------------------|
| User Onboarding Journey | Identity creation, initial preferences, PENDING → ACTIVE |
| Dashboard / Account Home | Profile for personalization, account state for UI gating |
| Roles / Permissions / Access | Identity as permission subject, role attachment model |
| CRM / Support | Customer identity, communication language preference |
| Notifications / Communication | User preferences, delivery language, account eligibility |
| Subscription / Plan Governance | Account as subscription holder, lifecycle for eligibility |

---

## Open Decisions (High-Level Summary)

| Area | Key Unresolved Decisions |
|------|------------------------|
| Identity provider | Auth provider not selected (architecture is provider-agnostic) |
| Profile storage | Database/storage technology not committed |
| File format support | Which formats supported first (CSV/XLSX/PDF) undecided |
| Raw file storage | Where uploaded files are stored — undecided |
| Retention policy | How long raw files and extracted data are retained — undecided |
| Asset resolution | Confidence threshold for automatic mapping — undecided |
| Multi-user timeline | When CTO-only expands to additional roles — deferred |

Total: 28 unresolved decisions tracked for design phase resolution.

---

## Governance Statement

- **No implementation authorized** — this spec defines architecture boundaries only
- **No runtime code, no parsers, no storage, no APIs, no UI** created by this spec
- **Portfolio import does not authorize action** — importing holdings is factual data capture, never recommendation
- **Reports remain RESEARCH_DRAFT** — portfolio-aware reports preserve research-only classification
- **MoneyHorst does not generate autonomous investment decisions** — all final decisions remain under human CTO authority
- **Human decision authority is final** — no AI system, automation, or workflow may override human governance

---

## Requirements Summary

- 62 formal requirements (R1–R62)
- 10 correctness properties
- Full traceability to preflight and upstream specs
- EARS-style format with acceptance criteria
- Explicit prohibited actions (no implementation, no trading, no SAI mutation)

---

## Lifecycle Status

```
preflight   ✓ COMPLETE (CTO approved 2026-06-25)
requirements ✓ COMPLETE (62 requirements, ready for design)
design       — NOT STARTED
tasks        — NOT STARTED
implementation — NOT AUTHORIZED
```

---

*Documentation-based. No implementation authorized. No autonomous investment decision. Human authority final.*
