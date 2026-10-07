# Validation ; Agentic Value Stream

Per CR-VAS-004 §22 + §23, validation is not purely mechanical. It
combines machine validation, evidence inspection, and semantic
review.

## Validation chain

```
Machine validation
   +
Evidence inspection
   +
Semantic review
```

Automated validation SHALL NOT be the sole mechanism for semantic
qualification. Certain questions require semantic judgement,
particularly:

- Whether authority is genuinely delegated.
- Whether action alternatives are meaningful.
- Whether participation is material.
- Whether the claimed outcome is genuinely a Value Stream outcome.

## Validation roles

The repository distinguishes four roles. These roles SHALL NOT be
embedded as semantic requirements for being an AVS.

- Instance Owner. Responsible for making the AVS claim and
  supplying evidence.
- Semantic Validator. Evaluates conformance against the Agentic
  Value Stream specification.
- Domain Reviewer. Validates domain-specific interpretation where
  required.
- Governance Authority. May approve formal certification where
  organisational governance requires it.

## Evidence lifecycle

Evidence has a lifecycle:

```
Created
   |
   v
Submitted
   |
   v
Validated
   |
   v
Accepted
   |
   v
Monitored
   |
   v
Revalidated
   |
   v
Expired / Superseded
```

A conformance claim is therefore potentially time-bound.

## Evidence freshness

Evidence SHOULD optionally specify freshness:

```
freshness:
  valid_from:
  valid_until:
  review_interval:
```

Evidence freshness SHOULD be determined according to the volatility
of the underlying semantic claim:

- Static Value Stream definition -> relatively stable.
- Agent authority configuration -> potentially volatile.
- Runtime decision behavior -> highly dynamic.

## Conformance result

Each test result SHOULD be machine-readable:

```
result:
  test_id:
  status: pass | fail | inconclusive | not_applicable
  qualification_condition:
  evidence:
  observations:
  rationale:
```

Inconclusive SHALL be distinguished from fail. Absence of evidence
is NOT necessarily evidence of semantic failure; it MAY indicate
insufficient evidence. However, an instance cannot become fully
conformant while mandatory evidence remains inconclusive.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
