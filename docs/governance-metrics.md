# Governance Metrics (CR-VAS-007)

## Purpose

CR-VAS-007 introduces governance-specific measures that complement
(do NOT replace) CR-VAS-005 measurement metrics. Governance metrics
evaluate the **control plane** around AVS, not the AVS performance
itself.

## Six Governance Metrics

### 1. Governance Review Timeliness

`reviews_completed_within_required_period / reviews_due`

### 2. Revalidation Compliance

`material_changes_revalidated / material_changes`

### 3. Authority Control Coverage

`agentic_authority_boundaries_with_active_controls / total_delegated_authority_boundaries`

### 4. Governance Exception Rate

`governance_exceptions / governed_avs_events`

### 5. Suspension Response Time

Time from critical governance trigger to effective suspension.

### 6. Remediation Closure Rate

`closed_governance_findings / open_governance_findings`

## Governance Dashboard

A portfolio governance dashboard should expose:

### Lifecycle View

- Proposed, Assessed, Designed, Qualified, Approved, Operational,
  Suspended, Retired.

### Semantic View

- conformance status
- drift
- qualification age

### Authority View

- authority utilization
- exceptions
- revocations
- escalation

### Risk View

- incidents
- boundary violations
- policy exceptions

### Value View

- outcome realization
- incremental value
- cost
- risk-adjusted value

### Maturity View

- capability profile
- gaps
- improvement trajectory

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
