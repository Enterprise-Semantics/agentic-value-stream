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