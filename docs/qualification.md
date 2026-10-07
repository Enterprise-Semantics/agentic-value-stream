# Qualification ; Agentic Value Stream

Per CR-VAS-004 §12 + §30, the qualification decision follows a
deterministic model with explicit rules.

## Qualification decision model

```
Value Stream?
   |
  YES
   v
Agentic Participation?
   |
  YES
   v
Intent + Authority + Context + Selection?
   |
  YES
   v
Material Value Contribution?
   |
  YES
   v
AVS QUALIFIED
```

Any mandatory condition failing SHALL prevent a qualified status.

## Qualification decision rules

The final decision follows:

IF
  Value Stream semantics = PASS
AND
  all mandatory AVS conditions = PASS
AND
  materiality = PASS
AND
  no exclusion = triggered
THEN
  CONFORMANT
ELSE IF
  mandatory evidence incomplete
THEN
  UNDER_REVIEW / CONDITIONALLY_CONFORMANT
ELSE
  NON_CONFORMANT

A triggered exclusion SHALL override superficial positive evidence.

## Materiality evidence

Per CR-VAS-004 §16, the evaluator SHALL answer:

> If the agentic participation were removed and replaced by a
> non-agentic realisation, would the Value Stream's progression,
> consequential decisions, or realisation of stakeholder value
> materially change?

The result SHALL be recorded as:

```
materiality:
  test:
  result: true
  rationale:
  evidence:
```

A simple assertion of true without rationale SHALL be insufficient.

## Counterfactual validation

Materiality SHOULD preferably be tested through a counterfactual.
The baseline is the actual agentic realisation. The counterfactual
is an equivalent non-agentic realisation. The comparison evaluates
differences in:

- Progression.
- Decisions.
- Action selection.
- Outcome.
- Intervention.
- Value realisation.

Conclusion form: A materially differs from B -> Materiality supported.

The counterfactual need not always be executed in production. It
MAY be demonstrated through simulation, historical replay,
controlled testing, or analytical reasoning.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
