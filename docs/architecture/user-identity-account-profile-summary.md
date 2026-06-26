# MoneyHorst — User Identity / Account / Profile Architecture Summary

> **Spec**: moneyhorst-user-identity-account-profile
> **Phase**: Task execution in progress — Tasks 1–12 of 14 complete
> **Date**: 2026-06-26
> **Status**: Documentation-only architecture specification
> **Implementation Authorized**: NO
> **Public-Safe**: YES — no user data, no holdings, no credentials

---

## Overview

This spec defines the architecture boundaries for user identity, account, and profile within MoneyHorst — including external portfolio import as a core profile/account capability. It is the sixth MoneyHorst architecture spec to reach task execution and unblocks six downstream specs.

67 requirements (hardened). 14 tasks (12 complete). 10 architecture boundary artifacts produced. Zero runtime code.

---

## Architecture Boundaries

### Identity Boundary
- Canonical actor record: stable system-internal ID, actor type, auth reference, state
- Independent of auth provider, email, or display name
- State machine: ACTIVE → SUSPENDED → DEACTIVATED
- Identity contains ONLY: ID, type, auth ref, timestamp, state

### Account Boundary
- Operational container: lifecycle state, subscription reference, authority level
- Lifecycle: PENDING → ACTIVE → SUSPENDED → DEACTIVATED
- Deactivation preserves all data; reactivation requires CTO override
- Account does NOT contain preferences or profile data

### Profile Boundary
- Preferences and personalizations: language, locale, timezone, notifications, portfolios
- Rendering-layer only — never authority
- Includes imported portfolio records (Bestandportfolio)

---

## Core Governance Rules

| Rule | Description |
|------|-------------|
| Preferences are never authority | Changing language/locale/timezone NEVER alters governance state |
| Language/locale is rendering-only | Display changes only — no canonical value mutation |
| Portfolio import does not authorize action | Bestandportfolio is factual context, not trading signal |
| Reports remain RESEARCH_DRAFT | Portfolio-aware reports preserve research-only classification |
| No silent assumption of asset identity | Confidence < HIGH requires explicit user confirmation |
| User confirmation is the hard gate | No imported asset becomes canonical without user action |
| Agent access defaults to NONE | Purpose-scoped, temporary, auditable grants only |
| Human CTO authority is final | No AI, automation, or workflow may override |

---

## External Portfolio Import (Architecture Boundary Only)

- Core profile/account capability (architecture decision resolved)
- Flow: Upload → Extract → Normalize → User Review → Confirm/Reject → Report-Ready Bestandportfolio
- File lifecycle: 9 states including FAILED, REJECTED, DELETED, EXPIRED
- Asset normalization: ticker, ISIN, WKN, exchange, currency, asset type, sector, duplicates
- Confidence levels: HIGH / MEDIUM / LOW / NONE
- User confirmation: hard gate — no bypass, no agent canonicalization, no time-based acceptance
- Privacy: sensitive financial data classification, encryption required, no external sharing
- Parser/storage/runtime/UI implementation NOT authorized — deferred to future specs

---

## Agent Access and Privacy

- Default agent access to ALL profile and portfolio data: NONE
- Temporary extraction access: purpose-scoped READ only during active extraction, immediately revoked
- No persistent agent access permitted
- No agent may write, modify, delete, or canonicalize profile/portfolio data
- All access grants must be: explicit, purpose-scoped, documented, revocable, auditable, temporary

---

## Downstream Specs Unblocked

| Spec | What It Consumes |
|------|-----------------|
| User Onboarding Journey | Identity creation, account initial state, preference defaults |
| Dashboard / Account Home | Profile for personalization, account state for UI gating |
| Roles / Permissions / Access | Identity as permission subject, account as container |
| CRM / Support | Customer identity, communication language preference |
| Notifications / Communication | Delivery preferences, account eligibility |
| Subscription / Plan | Account as holder, lifecycle for eligibility |

---

## Open Decisions

- **Total**: 29 decisions tracked
- **Resolved**: 1 (portfolio import is core profile capability)
- **Deferred**: 1 (multi-user timeline)
- **Unresolved**: 27 (block future implementation specs)
- **Critical blockers**: Auth provider selection, profile storage technology
- All decisions require explicit CTO resolution — no inference, no time-based resolution

---

## Governance Statement

- **No implementation authorized** — architecture contracts only
- **No runtime code, parsers, storage, APIs, UI, auth, or databases** created
- **Portfolio import does not authorize action** — factual data capture only
- **Reports remain RESEARCH_DRAFT** — no upgrade from portfolio import
- **MoneyHorst does not generate autonomous investment decisions**
- **Human decision authority remains final** — no AI override permitted
- **NO_IMPLEMENTATION_AUTHORIZED preserved** throughout all artifacts

---

## Lifecycle Status

```
preflight        ✓ COMPLETE
requirements     ✓ COMPLETE (67 requirements, hardened)
design           ✓ COMPLETE
tasks            ✓ CREATED (14 tasks)
task execution   IN PROGRESS — Tasks 1–12 complete, Tasks 13–14 pending
implementation   NOT AUTHORIZED
```

---

## Public-Safe Limitation

This document contains NO:
- User portfolio holdings or positions
- WKN/ISIN/ticker data from any user portfolio
- Broker or account information
- Credentials or secrets
- Implementation details or runtime configuration
- Private repository history

Architecture and governance boundaries only.

---

*Documentation-based. No implementation authorized. No autonomous investment decision. Human authority final.*
