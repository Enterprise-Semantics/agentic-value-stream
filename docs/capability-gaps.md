# Capability Gaps (CR-VAS-006)

## Purpose

The maturity assessment SHALL produce **capability gaps**, not merely
a maturity score. This makes the model actionable: a dimension-level
gap identifies the concrete improvement initiative required to
advance the organization.

## Gap Model

```yaml
gap:
  capability:
  current_level:
  target_level:
  gap_type: [...]
  priority:
  recommended_action: [...]
```

### Field Semantics

| Field | Description |
|---|---|
| capability | The capability dimension (e.g. `value_performance`). |
| current_level | The current level for that dimension. |
| target_level | The target level for that dimension. |
| gap_type | Tags that classify the nature of the gap. |
| priority | `high`, `medium`, or `low`. |
| recommended_action | Specific actions that close the gap. |

### Common Gap Types

- `baseline_missing`  and  required baselines not yet established
- `attribution_missing`  and  value attribution not yet practiced
- `evidence_missing`  and  evidence required by level not yet produced
- `process_undefined`  and  process artifacts missing
- `measurement_undefined`  and  measurement definitions missing
- `policy_undefined`  and  policy artifacts missing
- `ownership_undefined`  and  governance ownership unclear
- `conformance_drift`  and  drift detected vs prior assessment
- `regression`  and  capability regressed since prior assessment

## Example: Value Performance Gap

```yaml
gap:
  capability: value_performance
  current_level: L2
  target_level: L4
  gap_type:
    - baseline_missing
    - attribution_missing
  priority: high
  recommended_action:
    - establish_counterfactual_baseline
    - implement_value_attribution
```

## Improvement Planning Chain

The gap model feeds a chain that connects assessment to action:

```
Current State
   -> Capability Gap
     -> Required Evidence
       -> Improvement Initiative
         -> Implementation
           -> Measurement
             -> Reassessment
```

This chain connects naturally to enterprise architecture and
transformation planning.

## Gap-to-Initiative Mapping

| Gap Type | Typical Initiative |
|---|---|
| `baseline_missing` | establish counterfactual baseline; instrument pre-AVS state |
| `attribution_missing` | implement value attribution model; define attribution confidence tiers |
| `evidence_missing` | produce required evidence artifacts; refresh existing evidence |
| `process_undefined` | author process definitions; document RACI |
| `measurement_undefined` | define measurement model; select metrics |
| `policy_undefined` | author policy artifacts; align with enterprise policy hierarchy |
| `ownership_undefined` | assign governance roles per CR-VAS-006 §35 |
| `conformance_drift` | trigger revalidation per CR-VAS-004 drift detection |
| `regression` | execute maturity drift recovery per CR-VAS-006 §37 |

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-006
acceptance review (governance frame ES-ADR-056).
