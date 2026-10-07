# Measurement ; Agentic Value Stream

Per CR-VAS-005 (Measurement & Operational Value Model, 2026-10-08),
measurement evaluates an already-qualified and conformant AVS
implementation. Measurement does NOT determine whether the underlying
concept is semantically an AVS.

The most important design decision in CR-VAS-005 is: do not allow
measurement to become a backdoor definition of agenticity.

```
Activity != Effectiveness != Business Value
```

A highly active agent can be ineffective. A highly autonomous agent
can destroy value. A low-volume agentic intervention can create
substantial value. Therefore activity alone SHALL NEVER be treated as
success.

## Normative measurement question

Does agentic participation improve or materially contribute to the
realization of Value Stream outcomes within acceptable authority,
risk, cost, and intervention boundaries?

## Five-level measurement hierarchy

- Level 1 ; Activity. What happened?
- Level 2 ; Behavior. How did the agent behave?
- Level 3 ; Performance. How well did it perform?
- Level 4 ; Value. What value did it create or protect?
- Level 5 ; Strategic effect. What changed because of agentic
  realization?

This prevents dashboards from becoming collections of low-level
telemetry.

## Six primary dimensions

1. Value realization. Primary dimension. Measures whether agentic
   participation improves the intended Value Stream outcome.
2. Agentic effectiveness. Whether agentic behavior functions as
   intended.
3. Decision and action quality. Decision quality, action quality,
   and outcome quality are NOT equivalent.
4. Human intervention. Measured as a dimension, NOT automatically
   treated as failure.
5. Authority and risk. Risk introduced by delegated authority.
6. Operational efficiency. Cost, throughput, cycle time, capacity.

## Conditional metrics

Distinct from universal measurement dimensions. Applicable only where
relevant:

- Multi-agent coordination.
- Adaptive progression.
- AI-specific metrics.
- Autonomy-specific metrics.

A single-agent AVS SHALL NOT be required to implement multi-agent
metrics.

## Baseline model

A baseline is REQUIRED wherever an improvement claim is made. The
baseline SHALL be declared explicitly. Baseline types: historical,
human_only, automated, pre_agentic, controlled, counterfactual,
benchmark.

An assertion such as "agentic implementation improved efficiency by
40%" SHALL NOT be considered complete without identifying the
comparison baseline.

## Counterfactual comparison

The preferred measurement construct is:

```
Incremental AVS Value = AVS Result - Comparable Baseline Result
```

This is substantially more meaningful than measuring agentic activity
alone.

## Measurement context

Every measurement SHALL identify its Value Stream context:

```
measurement:
  id:
  value_stream:
  agentic_participation:
  metric:
  definition:
  unit:
  population:
  period:
  baseline:
  observed_value:
  target:
  threshold:
  provenance:
```

This avoids orphan metrics that cannot be interpreted semantically.

## Value attribution

Attributing Value Stream improvement solely to agentic participation
is difficult. Other factors may change simultaneously (process
redesign, technology modernization, workforce changes, market
conditions, policy changes, product changes, organizational
restructuring). Therefore the measurement model supports an
attribution confidence field:

```
attribution:
  contribution:
  confidence: high | medium | low | unknown
  basis:
```

## Measurement provenance

Every reported metric SHOULD be traceable:

```
Value Stream -> Agentic Participation -> Observed Events -> Measurement -> Outcome
```

This allows measurements to remain semantically anchored.

## Measurement lifecycle

Measurements SHALL support a lifecycle:

```
Defined -> Instrumented -> Collected -> Validated -> Analyzed -> Acted Upon -> Reviewed
```

This distinguishes a metric definition from an operationally trusted
measurement.

## Measurement quality

A metric without reliable measurement provenance SHALL NOT be
treated as equivalent to a validated metric. Quality dimensions:
accuracy, completeness, timeliness, consistency, traceability,
comparability.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
