# Conformance Drift ; Agentic Value Stream

Per CR-VAS-004 §25, the repository supports detection of semantic
drift. A previously conformant instance MAY become non-conformant
when its semantic structure changes.

## Drift triggers

The repository SHOULD detect drift when any of the following
conditions hold:

- Authority has changed.
- Agent behavior has changed.
- Workflow has changed.
- Value Stream has changed.
- Agentic Participation has been removed.
- Action space has changed.
- Policy has changed.
- Human escalation has been removed.
- Materiality has changed.

## Drift vs maturity

Drift is different from maturity deterioration. Drift means the
semantic qualification conditions are no longer met. Maturity
deterioration means the operational quality has degraded while the
semantic qualification is preserved.

## Drift handling

When drift is detected:

1. Re-validate conformance using the current state.
2. Update the qualification evidence record.
3. Move the conformance status to one of:
   - Under Review (while evidence is reassessed).
   - Conditionally Conformant (if evidence gaps remain).
   - Non-Conformant (if any mandatory condition fails).
   - Expired (if previous evidence is no longer valid).
4. Notify the Instance Owner + Semantic Validator.
5. Begin the Revalidated stage of the evidence lifecycle.

## Drift evidence

Drift evidence SHOULD carry provenance per the evidence provenance
template. Drift events SHOULD be recorded in the qualification
evidence record with timestamp + trigger + observed change +
conformance status transition.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
