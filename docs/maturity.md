# Maturity & Capability (CR-VAS-006)

## Purpose

This document introduces the formal maturity and capability progression
model for organizations implementing Agentic Value Streams (AVS).

Per CR-VAS-006, maturity measures **how systematically an organization
can design, govern, operate, measure, improve, and scale** Agentic
Value Streams. Maturity is a property of the **organization**, not of
the AVS itself, and it does **not** determine whether a Value Stream
is semantically an AVS.

## Core Principle

> Maturity measures the organization's capability to realize, govern,
> improve, and scale Agentic Value Streams; it does not determine
> whether a Value Stream is Agentic.

The dependency is intentionally one-directional:

```
Semantic Qualification      (Is it AVS?)
  -> Conformance & Evidence (Is the claim valid?)
    -> Operational Measurement (How well does it perform?)
      -> Maturity & Capability (How systematically can the
         organization operate, govern, improve and scale it?)
```

A high-maturity organization may have non-agentic Value Streams. A
low-maturity organization may operate a semantically conformant AVS.
A highly performant AVS does not automatically imply organizational
maturity.

## Separation Principles

| Layer | Question | Property of |
|---|---|---|
| Semantic qualification (CR-VAS-002) | Is this an AVS? | the candidate |
| Conformance (CR-VAS-004) | Does it satisfy AVS rules? | the implementation |
| Measurement (CR-VAS-005) | How well does it perform? | the AVS instance |
| Maturity (CR-VAS-006) | How capable is the organization? | the organization |

Maturity **shall not** be used as evidence of agenticity. AI adoption,
agent count, autonomy percentage, model sophistication, and
operational scale **shall not** establish maturity on their own.

## Scope of This Document

This document is the entry point for the maturity framework. Detailed
specifications live in:

- `capability-model.md`  and  six capability dimensions and the
  capability progression matrix
- `maturity-levels.md`  and  L0 through L5 definitions, minimum
  capabilities, and critical distinctions
- `maturity-assessment.md`  and  multidimensional assessment rule,
  mandatory gates, evidence requirements by level, assessment
  record template, and assessment frequency
- `capability-gaps.md`  and  gap model, prioritization, and improvement
  planning chain
- `maturity-governance.md`  and  governance roles, capability lifecycle,
  transition criteria, drift, regression, and enterprise
  architecture relationship
- `maturity-anti-patterns.md`  and  eight anti-patterns that shall be
  explicitly rejected

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-006
acceptance review (governance frame ES-ADR-056).
