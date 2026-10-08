# Lifecycle (CR-VAS-007)

## Purpose

An AVS SHALL have an explicit lifecycle. CR-VAS-007 establishes the
10-state lifecycle that governs how conformant AVS are proposed,
assessed, designed, qualified, approved, implemented, operated,
managed, suspended, and retired.

## Lifecycle Is Not Necessarily Linear

An AVS may move backwards:

```
Operational
   -> Suspended
     -> Revalidated
       -> Operational
```

or:

```
Operational
   -> Material Change
     -> Reassessment
       -> Non-Conformant
         -> Remediation
```

## The 10 Lifecycle States

### Proposed

The Value Stream has been identified as a candidate for agentic
realization. No claim of AVS conformance has yet been established.

### Assessed

The candidate has undergone initial evaluation covering Value
Stream relevance, candidate agentic participation, expected
outcomes, potential authority, risk, materiality, feasibility.

### Designed

The intended realization has been formally designed. Includes
participation scope, intent, authority, contextual inputs, action
space, intervention, escalation, expected outcomes, measurement,
governance.

### Qualified

The implementation/design has satisfied the applicable AVS
semantic qualification and evidence requirements established
through CR-VAS-002 and CR-VAS-004. Qualification is a **semantic
state**, not a technology approval.

### Approved

The relevant governance authority has authorized implementation or
operation within the defined boundary. **Approval SHALL NOT be
interpreted as semantic qualification.** An implementation can be
semantically valid but not yet approved for production.

### Implemented

The AVS realization exists technically and operationally but may
not yet be operating as a production service.

### Operational

The AVS is actively realizing value in its intended operational
environment. Required controls must be active.

### Managed

The AVS is operational and is subject to systematic measurement,
monitoring, risk management, value management, conformance
management, improvement. Aligns with the operational capability
described in CR-VAS-006.

### Suspended

The AVS has temporarily ceased agentic realization. Triggers may
include: material policy violation; authority breach; unacceptable
risk; conformance failure; severe operational incident; unexplained
outcome degradation; loss of required evidence; regulatory
requirement. Suspension SHOULD preserve the Value Stream itself
where possible. The agentic realization may be disabled while a
non-agentic fallback continues.

### Retired

The AVS implementation is no longer authorized for operational
use. Retirement SHOULD preserve: historical evidence; measurement
history; governance decisions; lessons learned; relevant
provenance.

## Governance State vs Lifecycle State

Lifecycle state and governance status SHALL remain distinct. An
AVS may be operational while subject to remediation, heightened
monitoring, conditional approval, or restricted authority.
Similarly, an AVS may be suspended with governance status
remediation. This prevents state explosion.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
