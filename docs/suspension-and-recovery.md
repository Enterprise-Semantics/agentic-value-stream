# Suspension, Fallback and Recovery (CR-VAS-007)

## Suspension Triggers

The AVS has temporarily ceased agentic realization. Triggers may
include:

- material policy violation
- authority breach
- unacceptable risk
- conformance failure
- severe operational incident
- unexplained outcome degradation
- loss of required evidence
- regulatory requirement

Suspension SHOULD preserve the Value Stream itself where possible.
The agentic realization may be disabled while a non-agentic
fallback continues.

## Fallback Patterns

Every production AVS SHOULD define an appropriate fallback
strategy. Possible patterns include:

- Agentic -> Human
- Agentic -> Deterministic Automation
- Agentic -> Manual Process
- Agentic -> Safe Stop

The fallback SHALL be determined by Value Stream criticality and
risk. Fallback behavior SHOULD itself be tested.

## Emergency Controls

Critical AVS implementations SHOULD provide:

- emergency suspension
- authority revocation
- safe fallback
- escalation
- incident capture
- evidence preservation
- controlled restart

These controls SHOULD operate independently enough to remain
effective when the AVS itself is malfunctioning.

## Recovery

A suspended AVS may be resumed after revalidation. Recovery
SHALL:

- preserve evidence of the suspension trigger;
- confirm the cause has been remediated;
- re-validate conformance (CR-VAS-004);
- re-confirm authority scope;
- re-establish governance conditions.

Recovery is NOT automatic. It is a governance decision that
follows the change decision model.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
