# Measurement Provenance ; Agentic Value Stream

Per CR-VAS-005 §32 + §34 + AC-13 + AC-25, every reported metric SHOULD
be traceable to its semantic origin and measurement quality SHOULD
be represented.

## Provenance chain

```
Value Stream -> Agentic Participation -> Observed Events -> Measurement -> Outcome
```

This allows measurements to remain semantically anchored. Orphan
metrics that cannot be interpreted semantically are rejected.

## Measurement lifecycle

```
Defined -> Instrumented -> Collected -> Validated -> Analyzed -> Acted Upon -> Reviewed
```

A metric definition is NOT equivalent to an operationally trusted
measurement.

## Measurement quality dimensions

- Accuracy.
- Completeness.
- Timeliness.
- Consistency.
- Traceability.
- Comparability.

A metric without reliable measurement provenance SHALL NOT be treated
as equivalent to a validated metric.

## Measurement context

Every measurement SHALL identify its Value Stream context: id,
value_stream, agentic_participation, metric, definition, unit,
population, period, baseline, observed_value, target, threshold,
provenance.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
