# Maturity Assessment (CR-VAS-006)

## Assessment Principle

Maturity SHALL NOT be determined by a simple count of technologies or
features. The assessment evaluates:

> Capability + Evidence + Operational Practice + Performance +
> Governance + Repeatability + Scale.

A capability SHALL NOT be considered mature merely because
documentation exists.

## Multidimensional Assessment Rule

A single arithmetic average SHALL NOT be the default maturity
mechanism. The profile SHALL remain visible with per-dimension
levels and limiting dimensions called out.

Example profile:

```yaml
maturity:
  overall:
    level: L3
  dimensions:
    design: L5
    governance: L4
    operations: L3
    value: L2
    improvement: L2
    scaling: L1
  limiting_dimensions:
    - value
    - improvement
    - scaling
```

## Overall Maturity Rule

If an overall maturity level is reported, it SHALL be derived from
a **minimum-required-dimension gated** model, not a simple average.

> Overall Maturity = minimum of required capability dimensions,
> subject to level-specific gates.

This prevents exceptional strength in one area from masking
fundamental weakness elsewhere.

For example: excellent AI engineering + weak authority governance
+ no outcome measurement SHALL NOT qualify as a highly mature AVS
capability.

## Mandatory Gates

| Gate | Requires |
|---|---|
| L2 Gate | defined AVS semantics, defined qualification approach, authority model, evidence model, measurement model, governance ownership |
| L3 Gate | at least one conformant production AVS, operational authority enforcement, operational intervention/escalation, outcome measurement, traceable evidence |
| L4 Gate | repeatable performance management, baseline comparison, value measurement, risk monitoring, conformance drift management, systematic improvement |
| L5 Gate | multiple operational AVS implementations, portfolio governance, reusable capability patterns, enterprise measurement, demonstrated scaling, continuous capability evolution |

## Evidence Requirements by Level

| Level | Evidence |
|---|---|
| L1 | strategy statements, awareness material, identified candidates, terminology, preliminary assessments |
| L2 | AVS models, qualification assessments, authority models, conformance tests, governance definitions, measurement specifications |
| L3 | production instances, conformance records, runtime evidence, operational metrics, intervention records, authority enforcement, outcome evidence |
| L4 | historical performance, baselines, trend analysis, value attribution, risk analysis, improvement records, conformance drift analysis |
| L5 | portfolio-level measurements, reusable patterns, enterprise governance, cross-AVS analysis, scaling evidence, continuous improvement, capability evolution records |

## Assessment Record Template

A maturity assessment SHOULD be represented separately from the AVS
semantic definition.

```yaml
maturity_assessment:
  id:
  subject:
    organization:
    portfolio:
    value_streams:
  model:
    version:
  assessment_period:
  dimensions:
    design_semantics:           {level, evidence, gaps}
    governance_authority_risk: {level, evidence, gaps}
    operational_realization:    {level, evidence, gaps}
    value_performance:          {level, evidence, gaps}
    learning_improvement:       {level, evidence, gaps}
    portfolio_scaling:          {level, evidence, gaps}
  overall:
    level:
    gating_result:
    limiting_dimensions:
  assessor:
  assessment_date:
  next_review:
```

## Assessment Frequency

Maturity SHOULD be reassessed:

- periodically;
- after major architectural changes;
- after material authority changes;
- after significant changes in agentic scope;
- after major incidents;
- after significant regulatory changes;
- when expanding to new Value Streams;
- when material performance deterioration occurs.

Maturity status is therefore considered time-bound evidence, not a
permanent organizational label.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-006
acceptance review (governance frame ES-ADR-056).
