# Governance (CR-VAS-007)

## Purpose

This document introduces the formal governance and lifecycle control
plane for Agentic Value Streams. CR-VAS-007 governs how conformant
AVS are created, changed, monitored, suspended, retired, and managed
across an enterprise portfolio.

Per CR-VAS-007, governance does NOT redefine AVS semantics.
Instead, it establishes the management control plane around an
already-defined semantic object.

## Core Principle

An Agentic Value Stream is governed as a **Value Stream with agentic
participation**, not as an autonomous technology asset.

Governance therefore begins with:

```
Value Stream
   -> Agentic Participation
     -> Authority
       -> Risk
         -> Outcome
           -> Governance
```

rather than:

```
AI Model
   -> Agent
     -> Agentic System
       -> Governance
```

The latter incorrectly makes technology the primary governance
object. The correct direction anchors governance in the Value
Stream and its delegated agentic participation.

## Governance Objective

Ensure that delegated agentic participation remains:

- semantically valid
- appropriately authorized
- operationally controlled
- outcome-oriented
- measurable
- aligned with enterprise intent

throughout its lifecycle.

## Governance Dimensions

Six dimensions:

1. Semantic integrity
2. Authority integrity
3. Operational integrity
4. Risk and policy integrity
5. Value integrity
6. Lifecycle integrity

## Scope of This Document

This document is the entry point for the governance framework.
Detailed specifications live in:

- `lifecycle.md` ; lifecycle model + 10-state vocabulary + state
  separation
- `change-management.md` ; material change + change classification
  + change decision model
- `authority-governance.md` ; authority record schema + escalation
  + revocation + governance evidence
- `suspension-and-recovery.md` ; suspension triggers + fallback
  patterns + emergency controls + recovery
- `portfolio-governance.md` ; portfolio inventory + prioritization
  + capability reuse + agent sprawl avoidance + concentration risk
- `governance-metrics.md` ; 6 governance metrics + dashboard views
- `governance-anti-patterns.md` ; 6 anti-patterns that shall be
  explicitly rejected

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
