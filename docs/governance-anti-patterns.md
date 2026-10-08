# Governance Anti-Patterns (CR-VAS-007)

## Purpose

Per CR-VAS-007 §39, the following anti-patterns SHALL explicitly be
rejected. None of these constitute acceptable governance practice.

## The Six Anti-Patterns

### 1. Approval Equals Qualification

**Incorrect:** "Managerial approval proves a Value Stream is Agentic."

**Rejected because:** semantic qualification (CR-VAS-002) and
governance approval are distinct decisions. An implementation can be
semantically valid but not yet approved for production.

### 2. No Revalidation

**Incorrect:** "Authority is materially expanded without
reassessment."

**Rejected because:** material changes (Class C) require formal
revalidation. The change decision model mandates this.

### 3. Irrevocable Authority

**Incorrect:** "The implementation has no effective mechanism for
authority revocation."

**Rejected because:** authority must be revocable. Revocation is a
governance control, not an exceptional case.

### 4. Agent Controls Policy

**Incorrect:** "Runtime agent instructions can override governing
enterprise policies."

**Rejected because:** runtime instructions cannot supersede
governing authority or policy (AVS-GOV-INV-013). The policy
hierarchy is Enterprise -> Domain -> Value Stream -> AVS ->
Authority Boundary -> Runtime Enforcement.

### 5. No Fallback

**Incorrect:** "A critical AVS has no appropriate intervention,
suspension or fallback mechanism."

**Rejected because:** production AVS should have an appropriate
fallback strategy. The absence of fallback is a governance failure,
not a technical constraint.

### 6. Portfolio By Agent Count

**Incorrect:** "Portfolio investment is prioritized solely by number
of agents deployed."

**Rejected because:** portfolio prioritization SHALL consider
expected value, strategic alignment, feasibility, risk, capability
readiness, reuse potential, and operational criticality. A simple
"highest automation opportunity first" strategy is explicitly
rejected.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
