# Measurement Baselines ; Agentic Value Stream

Per CR-VAS-005 §14 + §27, the measurement framework SHALL require a
baseline wherever an improvement claim is made. The baseline SHALL
be declared explicitly.

## Baseline types

- Historical. Compare against the pre-agentic or historical state.
- Human-only. Compare against an equivalent human-only realization.
- Automated. Compare against an automated (non-agentic)
  realization.
- Pre-agentic. Compare against the pre-agentic operating model.
- Controlled. Compare against a controlled experiment.
- Counterfactual. Compare against a counterfactual simulation.
- Benchmark. Compare against an external benchmark.

## Improvement claim rule

An assertion such as "agentic implementation improved efficiency by
40%" SHALL NOT be considered complete without identifying the
comparison baseline.

## Counterfactual value construct

```
Incremental AVS Value = AVS Result - Comparable Baseline Result
```

This is substantially more meaningful than measuring agentic activity
alone.

## Conditional applicability

Counterfactual comparison MAY be demonstrated through simulation,
historical replay, controlled testing, or analytical reasoning.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
