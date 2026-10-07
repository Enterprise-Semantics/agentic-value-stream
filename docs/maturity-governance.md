# Maturity Governance (CR-VAS-006)

## Governance Roles

The maturity model distinguishes the following governance roles.
These are **governance roles**, not semantic requirements of an
Agentic Value Stream itself. They clarify accountability at the
organizational level for maturity outcomes.

| Role | Owns |
|---|---|
| AVS Capability Owner | organizational AVS capability |
| Value Stream Owner | value stream outcomes |
| Agentic Solution Owner | implementation of agentic participation |
| Risk / Governance Owner | authority, risk and policy controls |
| Semantic Steward | semantic consistency and conformance interpretation |
| Measurement / Value Owner | performance and value measurement |

In smaller organizations these MAY be combined, but they MUST
remain conceptually distinguishable.

## Capability Lifecycle

AVS capability SHALL follow a lifecycle:

```
Discover
   -> Qualify
     -> Design
       -> Conform
         -> Deploy
           -> Measure
             -> Improve
               -> Scale
                 -> Reassess
```

This lifecycle is **iterative**. A change to: authority, decision
logic, agentic scope, Value Stream structure, operating context,
risk boundary, or material behavior MAY trigger revalidation.

## Maturity Transition Criteria

Progression between levels SHALL require **demonstrated capability**
rather than elapsed time. There SHALL be no automatic progression
based on age, deployment count, or technology adoption.

| Transition | Requires |
|---|---|
| L2 -> L3 | actual operational realization |
| L3 -> L4 | demonstrated management of performance, value and risk |
| L4 -> L5 | demonstrated organizational scaling and adaptive capability |

## Maturity Drift (Regression Support)

An organization MAY regress. For example:

```
L4 Managed
   -> Major platform migration
     -> Measurement gaps
       -> Authority monitoring degraded
         -> L3 Implemented
```

The model **MUST** support regression. Maturity SHALL NOT be
treated as an irreversible progression.

## Enterprise Architecture Relationship

AVS maturity informs:

- business architecture
- operating model transformation
- enterprise architecture
- AI strategy
- automation strategy
- workforce transformation
- governance
- risk management
- technology investment
- data and knowledge strategy

AVS maturity SHALL remain semantically scoped to Agentic Value
Stream capability. It SHALL NOT become a generic enterprise digital
maturity model.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-006
acceptance review (governance frame ES-ADR-056).
