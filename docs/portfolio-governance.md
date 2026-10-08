# Portfolio Governance (CR-VAS-007)

## Why Portfolio Governance

At enterprise scale, governance must move beyond individual AVS
instances. The portfolio view identifies:

- AVS inventory
- business domains
- Value Streams
- agentic scope
- authority concentration
- criticality
- risk
- value
- maturity
- technology dependencies
- shared capabilities
- duplication
- lifecycle state

## Prioritization

Portfolio decisions SHOULD consider:

- Expected Value
- Strategic Alignment
- Feasibility
- Risk
- Capability Readiness
- Reuse Potential
- Operational Criticality

A simple "highest automation opportunity first" strategy is
explicitly rejected.

## Capability Reuse

Portfolio governance should identify reusable capabilities such as:

- identity
- authorization
- policy enforcement
- knowledge retrieval
- decision services
- monitoring
- evaluation
- intervention
- audit
- measurement
- orchestration

This prevents each AVS from independently rebuilding enterprise
control capabilities.

## Avoiding Agent Sprawl

Portfolio governance SHOULD explicitly monitor:

- duplicate agents
- duplicate capabilities
- inconsistent authority models
- fragmented policies
- overlapping Value Streams
- redundant AI services
- unnecessary multi-agent architectures

The goal is NOT to minimize the number of agents. The goal is to
minimize unnecessary complexity while maximizing reusable
value-realization capability.

## Portfolio Risk Concentration

An enterprise should identify concentration risks such as:

```
Many AVS
   -> Same authority service
     -> Same policy engine
       -> Same agent platform
         -> Single failure / control point
```

Portfolio governance SHOULD therefore consider systemic
dependencies.

## Portfolio Record Schema

```yaml
portfolio:
  id:
  name:
  members:
    - avs_id:
  governance:
    owner:
    review_cycle:
  dependencies:
    - type:
      subject:
  shared_capabilities:
    - capability:
  risk_profile:
    criticality:
    concentration:
  value:
    aggregate:
    confidence:
```

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
