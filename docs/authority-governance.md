# Authority Governance (CR-VAS-007)

## Why Authority Is Governed

Because bounded authority is a core AVS semantic condition,
authority SHALL be governed throughout the lifecycle. Authority
should be treated as a **governed enterprise resource**, not merely
a prompt or configuration parameter.

## Authority Record Schema

```yaml
authority:
  id:
  scope:
  actor:
  permissions:
  constraints:
  policies:
  thresholds:
  temporal_boundary:
  transaction_boundary:
  escalation_conditions:
  revocation_conditions:
  approval:
  effective_from:
  effective_until:
```

## Authority Escalation

The governance model SHALL support escalation. Escalation SHOULD be
explicit and observable.

Normal case: Agent acts within authority -> outcome progression.

Exceptional case: Authority threshold exceeded -> human /
higher-authority actor -> decision -> agent continues or terminates.

## Authority Revocation

Governance SHALL support immediate or scheduled revocation of
delegated authority. Revocation MUST NOT require semantic deletion
of the AVS.

Triggers include: incident; policy change; regulatory change;
abnormal behavior; authority misuse; material performance
degradation; security event; loss of required evidence.

## Governance Evidence

Each governance decision should have traceable evidence.

```yaml
governance_decision:
  id:
  subject:
  decision:
  rationale:
  authority:
  evidence:
  risks:
  conditions:
  effective_from:
  effective_until:
  decided_by:
  reviewed_by:
  review_date:
```

Governance decisions MUST be distinguishable from semantic
evidence.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
