# Agentic Value Stream

## Definition

Per CR-ES-005 §4 + ADR-ES-005 §2:

> An Agentic Value Stream is a Value Stream in which one or more
> stages are materially realized through agentic behavior, enabling
> delegated interpretation, action selection, coordination,
> adaptation, or execution toward stakeholder value realization.

## Semantic purpose

The Agentic Value Stream semantic establishes a formal representation
of agentic participation in value realization. Per CR-ES-005 §5 +
ADR-ES-005 §6:

- Agentic Value Stream is a Value Stream ;; not a replacement ;; not
  a parallel construct.
- Agentic Value Stream specialises Value Stream.
- Agentic Value Stream retains the mandatory Value Stream semantics
  established by CR-ES-003.

## Value Stream inheritance

Per CR-ES-005 §8, the Agentic Value Stream schema preserves the
mandatory Value Stream semantics established by CR-ES-003:

- stakeholder
- initiating_condition
- realization_boundary
- stages
- outcomes
- relationships
- grounding
- provenance
- version

The implementation does NOT duplicate or redefine these properties
where inheritance/reference is supported by the repository schema
architecture.

## Agentic characteristics

Per ADR-ES-005 §4, an Agentic Value Stream may exhibit one or more of
the following characteristics:

1. **Delegated Intent** (§4.1) ;; influenced by established or
   delegated intent.
2. **Contextual Interpretation** (§4.2) ;; relevant context can be
   interpreted during value realization.
3. **Dynamic Action Selection** (§4.3) ;; actions selected per
   context, intent, authority.
4. **Agentic Coordination** (§4.4) ;; Agent coordinates within its
   authority.
5. **Adaptive Progression** (§4.5) ;; progression changes in response
   to context.
6. **Bounded Authority** (§4.6) ;; explicit authority boundaries.
7. **Intervention** (§4.7) ;; human intervention remains possible.
8. **Outcome Orientation** (§4.8) ;; directed toward stakeholder
   outcomes.

## Agentic scope

`agentic_scope` is required (per CR-ES-005 §9) because an Agentic
Value Stream does NOT necessarily operate agentically at every stage.
Agentic participation may be localised to selected stages,
decisions, or execution areas.

## Authority and intent

Per CR-ES-005 §10, every Agentic Value Stream provides semantic
linkage between agentic participation and:

- **Intent** ;; the delegated intent that guides agentic
  participation.
- **Authority** ;; the bounded scope within which agentic
  participation occurs.

The canonical pattern is:

```
Agentic Value Stream
        |
        v
Delegated Intent
        |
        v
Agent
        |
        v
Authority
        |
        v
Action Selection
        |
        v
Execution
        |
        v
Outcome
```

## Mixed realization

Per CR-ES-005 §11 + ADR-ES-005 §5, mixed realization is a
first-class invariant. An Agentic Value Stream explicitly permits:

| Stage | Mode |
|-------|------|
| Stage 1 | Conventional |
| Stage 2 | Automated |
| Stage 3 | Agentic |
| Stage 4 | Human |
| Stage 5 | Agentic + Human |

Agentic Value Stream must NOT be interpreted as "a value stream where
everything is performed by agents".

## Human intervention

Per ADR-ES-005 §4.7 + §16, human intervention remains part of the
value stream. Human participation patterns are first-class ;; not
exclusions.

## AI boundary

Per ADR-ES-005 §11 + AG-INV-004:

- AI != Agent
- AI != Agentic
- Agentic Value Stream != AI Value Stream

AI-based agents are an implementation possibility ;; NOT a semantic
requirement.

## Automation boundary

Per ADR-ES-005 §12 + AG-INV-002:

- Agentic != Automation
- Automation may participate in an Agentic Value Stream without
  itself being agentic.

## Autonomy boundary

Per ADR-ES-005 §13 + AG-INV-003 + AG-INV-010:

- Agentic Value Stream != Autonomous Value Stream
- Agentic participation may operate with human approval ;; bounded
  authority ;; policy-controlled decisions ;; fixed organizational
  boundaries ;; externally established objectives.
- Autonomy is a separate semantic dimension ;; held for ADR-ES-008.

## Process boundary

Per ADR-ES-005 §10 + CAP-INV-001:

- Agentic Value Stream != Process
- Agentic Value Stream does not redefine Process, Activity, Task, or
  Workflow.

## Workflow boundary

Per ADR-ES-005 §10 + AG-INV-007:

- Agentic Value Stream != Agentic Workflow
- Agentic Value Stream != Workflow
- Agentic Workflow is held for ADR-ES-006.

## Examples

The canonical worked examples per CR-ES-005 §19 + §20:

- Order-to-Cash (OTCHERE Inc) ;; conventional and agentic
  representations
- Pay-to-Fulfillment ;; agentic participation distributed across
  financial and operational stages

See `examples/foundational/value-stream-order-to-cash-agentic.yaml`
and `examples/foundational/value-stream-pay-to-fulfillment-agentic.yaml`.

## Conformance requirements

The 12 conformance requirements per ADR-ES-005 §17 (AVS-CON-001..012)
are enforced via the agentic-value-stream tests in
`tests/agentic-value-stream/`.

## Provenance

- CR-ES-005 §4 + §5 + §7 + §8
- ADR-ES-005 §2 + §7 + §8 + §16
- FND-ES-AG-008 §1.3 (WSF Tier 1 / Tier 2 grounding boundary)
- ADR-ES-004 §5 + §6 + §7 + §16 (Agent semantics inheritance)

## Cardinal rules

- Author: Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
- D-004 dash rule
- SDO-neutral sourcing (ISO/IEC, ITU-T, ETSI, NIST)
- No vendor-specific material from embargoed sources

## Formal qualification (CR-VAS-002, 2026-10-07)

CR-VAS-002 establishes a normative qualification test for
Agentic Value Stream. The test combines required values,
exclusion conditions, and materiality thresholds. A candidate
passes iff all seven required values hold, none of the seven
exclusion conditions hold, and materiality is satisfied.

### Required values (AVS-VAL-01..07)

1. **Value-Stream Foundation** (AVS-VAL-01). The candidate must
   be a Value Stream. The Value-Stream Foundation is prerequisite.
2. **Material Agentic Participation** (AVS-VAL-02). One or more
   stages must be materially realised through agentic behavior.
3. **Delegated or Entrusted Intent** (AVS-VAL-03). The agentic
   participants must be entrusted with an intended outcome.
4. **Bounded Authority** (AVS-VAL-04). The agentic participants
   must operate within explicit bounded authority.
5. **Contextual Interpretation** (AVS-VAL-05). The agentic
   participants must interpret relevant context in service of
   the entrusted intent.
6. **Permissible Action or Progression Selection** (AVS-VAL-06).
   The agentic participants must select from a set of
   permissible actions or progression paths.
7. **Value-Realization Effect** (AVS-VAL-07). The agentic
   participation must contribute to stakeholder value
   realisation.

### Not-required (AVS-NRQ-01..07)

AI, autonomy, automation, decision-making as isolated quality,
agency as isolated quality, learning, and human intervention
legitimacy are explicitly not prerequisites. Their absence
does not disqualify; their presence alone does not qualify.

### Exclusion conditions (AVS-EXC-01..07)

Deterministic automation only, adaptive automation only,
decision-support AI only, human discretion only, autonomous
system participation only, dynamic workflow participation only,
and insufficient material proportion each fail qualification.

### Materiality (AVS-MAT-01..03)

Stage-count materiality, value-effect materiality, and
continuity materiality jointly determine whether agentic
participation is material.

### Invariants (AVS-INV-001..013)

Thirteen architectural invariants are enforced by the
conformance kit. They include the value-stream anchor invariant,
the stage composition invariant, the material agentic
participation invariant, the delegated intent invariant, the
bounded authority invariant, the contextual interpretation
invariant, the action selection invariant, the value-realisation
invariant, the AI-not-required invariant, the autonomy-not-
required invariant, the automation-not-required invariant,
the determinism-exclusion invariant, and the boundary-
assertion invariant.

### Edge cases (AVS-EDGE-01..05)

Single-stage material agentic participation, cross-stage
material agentic participation, multiple agentic participants
with separate authorities, agentic participation with co-
existing automation, and agentic participation with co-existing
human discretion are recognised as compositional arrangements
under which the candidate still qualifies.

### Conformance kit

The conformance kit (`kit/`) enforces the qualification test
with 5 positive tests (one per required-value group), 5
negative tests (one per primary exclusion condition), and
5 edge-case tests (compositional arrangements). Total: 15
tests. Coverage is auto-derived in `kit/kit.yaml`.