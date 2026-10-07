# Evidence ; Agentic Value Stream

Per CR-VAS-004 (Evidence, Conformance & Qualification Validation Model,
2026-10-08), an Agentic Value Stream instance must be able to supply
evidence for its qualification. This document explains the evidence
model, the three evidence levels, the qualification evidence chain,
evidence sufficiency, evidence provenance, evidence confidence, and the
qualification evidence record.

## Three levels of evidence

Evidence is classified into three semantic levels:

- Structural evidence. Evidence that the required semantic
  relationships exist (Value Stream, Agentic Participation, Intent,
  Authority, Context, Action selection, Outcome contribution).
  Answers: Is the required semantic structure represented?
- Behavioural evidence. Evidence that the represented participation
  actually behaves according to the semantics (interprets context,
  alternatives exist, selects among alternatives, authority boundaries
  enforced, escalation occurs, progression changes). Answers: Does
  the realisation actually behave agentically?
- Outcome evidence. Evidence that agentic participation materially
  contributes to Value Stream realisation (altered progression,
  consequential decision, materially different action, improved or
  changed value realisation, successful resolution of contextual
  variation). Answers: Does the agentic behavior materially matter
  to the Value Stream?

## Qualification evidence chain

The minimum evidence chain is:

```
Value Stream
   |
   v
Agentic Participation
   |
   v
Entrusted Intent
   |
   v
Bounded Authority
   |
   v
Contextual Interpretation
   |
   v
Permissible Alternatives
   |
   v
Action / Progression Selection
   |
   v
Material Value Contribution
```

A missing mandatory link SHALL prevent full semantic qualification.

## Evidence sufficiency

Evidence is classified as:

- Sufficient. Evidence supports the relevant qualification condition.
- Partial. Some evidence exists but does not fully establish the
  condition.
- Insufficient. The condition is asserted but not demonstrated.
- Contradictory. Available evidence conflicts with the qualification
  claim.
- Unverifiable. Evidence is referenced but cannot be independently
  inspected or validated.

## Mandatory vs supporting evidence

Mandatory evidence (required for AVS qualification):

- Value Stream identity.
- Agentic Participation.
- Intent.
- Authority.
- Context.
- Alternative selection.
- Material value contribution.

Supporting evidence (useful but not mandatory):

- AI model information.
- Agent architecture.
- Automation architecture.
- Autonomy level.
- Performance metrics.
- Intervention statistics.
- Implementation technology.
- Training data.
- Model evaluation.

This distinction prevents implementation details from replacing
semantic evidence.

## Evidence independence

The same evidence SHALL NOT automatically satisfy multiple
independent semantic conditions. The validation framework SHALL
avoid circular evidence. For example: "The agent has access to
customer data" may support contextual access but does NOT establish
delegated intent, authority, action selection, or outcome
contribution.

## Evidence provenance

Every material evidence item SHOULD have provenance. The
recommended structure is:

```
evidence:
  id:
  type:
  description:
  source:
  source_type: design_document | architecture_model | policy |
    configuration | execution_trace | decision_log | audit_record |
    test_result | simulation | human_review | system_observation |
    measurement
  observed_at:
  provided_by:
  validated_by:
  validation_method:
  confidence: high | medium | low | unknown
```

## Evidence confidence

Evidence may carry a confidence classification (high, medium, low,
unknown). However, confidence SHALL NOT override a missing mandatory
semantic condition. High-confidence evidence of AI usage cannot
compensate for absent evidence of delegated intent or bounded
authority.

## Qualification evidence record

The repository supports a machine-readable qualification record. The
structure follows the evidence chain above with one record per
qualification condition, each carrying a status and a list of
references.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
