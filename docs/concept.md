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

## Participation and Realization (CR-VAS-003)

Per CR-VAS-003 (Agentic Participation & Value Stream
Realization Model, 2026-10-08), the Agentic Value Stream
formalises a subordinate participation relationship inside
the canonical Value Stream rather than introducing a
parallel value-stage ontology.

### Hierarchical subordination

The semantic dependency is:

```
Value Stream
   |
   +-- Value Stage / Value-Realization Area
   |
   +-- Agentic Participation
            |
            +-- Actor / Agent
            +-- Entrusted Intent
            +-- Bounded Authority
            +-- Context
            +-- Decision / Selection
            +-- Action / Progression
            +-- Outcome Contribution
```

Agentic Participation does NOT replace the Value Stream,
does NOT create a parallel value-stage hierarchy, and
does NOT make the Agent the semantic center of the model.

### Participation scope vocabulary

```
agentic_scope:
  - decision
  - execution
  - coordination
  - stage
  - cross_stage
  - end_to_end
```

End-to-end is explicitly NOT the default representation.
A Value Stream can qualify as Agentic because of a single
material agentic participation point.

### Agent, AI, Automation, Autonomy distinctions

- `Agent != Agentic Participation != Agentic Value Stream`.
- AI remains orthogonal. AI + non-agentic, AI + agentic,
  and non-AI + agentic are all valid configurations.
- `Automation != Agentic Participation`. Automation may
  participate in an AVS without itself becoming agentic.
- Autonomy remains an independent dimension. Agenticity
  describes the presence of delegated, bounded, contextual,
  outcome-oriented action selection. Autonomy describes
  the degree of independent operation.

### Prohibited parallel constructs

The repository does NOT introduce any of the following as
parallel semantic constructs solely to represent
agenticity:

- Agentic Value Stage
- Agentic Process
- Agentic Workflow
- Agentic Operation
- Agentic Activity

A canonical Value Stage may contain any combination of
human, automated, agentic, hybrid, or multiple forms of
realization.

### Human participation patterns

Per CR-VAS-003 §13, human participation is a valid
realization pattern rather than an exception. Five
patterns are supported:

- Pattern A ; Human delegates an intended outcome to an
  agent.
- Pattern B ; Agent escalates an exception or threshold
  breach to a human, who decides, and the agent proceeds.
- Pattern C ; Human decides, agent executes.
- Pattern D ; Agent decides, human validates, then
  execution proceeds.
- Pattern E ; Shared progression (Human and Agent
  alternate).

### Governance rules

CR-VAS-003 §29 establishes eight governance rules that
constrain the participation model:

1. Value Stream remains primary.
2. Participation is explicit.
3. Authority is explicit.
4. Materiality is mandatory.
5. AI is implementation-independent.
6. Autonomy is orthogonal.
7. Human participation is first-class.
8. No parallel value-stage ontology.

### Conformance kit expansion

The conformance kit now contains 33 tests:

- 5 positive (AVS-VAL-01..07 required-value coverage),
- 5 negative (AVS-EXC-01..07 exclusion coverage),
- 5 edge case (compositional arrangements, AVS-EDGE-01..05),
- 8 structural (VAS-ST-01..08 participation structure, per
  CR-VAS-003 §24), and
- 10 boundary (VAS-BT-01..10 participation boundary
  distinction, per CR-VAS-003 §24).

The structural tests assert that the participation
hierarchy, intent, authority, context, action selection,
and material value contribution are explicitly
represented. The boundary tests distinguish Agentic
Participation from adjacent concepts (automation, AI,
workflow, autonomy, deterministic behavior, human
discretion, hybrid, multi-agent, non-AI).


## Evidence and Conformance (CR-VAS-004)

Per CR-VAS-004 (Evidence, Conformance & Qualification Validation
Model, 2026-10-08), the Agentic Value Stream repository establishes
the evidence layer that connects qualification (CR-VAS-002) and
participation (CR-VAS-003) to a machine-testable conformance
decision.

### Three levels of evidence

- Structural evidence. The required semantic relationships exist.
- Behavioural evidence. The represented participation actually
  behaves according to the semantics.
- Outcome evidence. The agentic participation materially contributes
  to Value Stream realisation.

### Claim != Evidence != Validation

An AVS instance SHALL NOT be considered semantically conformant
solely because it is named "agentic", contains an Agent, uses AI,
uses an LLM, is autonomous, uses orchestration, adapts, or
performs automated actions. The validation chain is:

```
Claim -> Evidence -> Validation -> Qualification Decision -> Conformance Status
```

### Conformance status vocabulary

- Claimed. The owner asserts that the instance is an AVS.
- Under Review. Evidence is being assessed.
- Conditionally Conformant. Most conditions are satisfied but
  defined exceptions or evidence gaps remain.
- Conformant. All mandatory semantic requirements are satisfied.
- Non-Conformant. One or more mandatory requirements fail.
- Expired. Previously conformant evidence is no longer current or
  valid.

### Conformance vs Maturity

Conformance != Maturity. An organisation can have a highly mature
implementation that is not semantically Agentic, or a semantically
conformant AVS that is operationally immature. Maturity is
addressed in CR-VAS-006.

### Validation chain

```
Machine validation + Evidence inspection + Semantic review
```

Automated validation SHALL NOT be the sole mechanism for semantic
qualification. Certain questions (whether authority is genuinely
delegated, whether action alternatives are meaningful, whether
participation is material, whether the claimed outcome is
genuinely a Value Stream outcome) require semantic judgement.

### Conformance kit expansion

The conformance kit now contains 61 tests:

- 5 positive (AVS-VAL-01..07 required-value coverage, CR-VAS-002).
- 5 negative (AVS-EXC-01..07 exclusion coverage, CR-VAS-002).
- 5 edge case (AVS-EDGE-01..05 compositional arrangements,
  CR-VAS-002).
- 8 structural (VAS-ST-01..08 participation structure,
  CR-VAS-003).
- 10 boundary (VAS-BT-01..10 participation boundary distinction,
  CR-VAS-003).
- 8 conformance positive (VAS-CF-P01..P08, CR-VAS-004).
- 10 conformance negative (VAS-CF-N01..N10, CR-VAS-004).
- 10 conformance boundary (VAS-CF-BT-01..10, CR-VAS-004).

The conformance positive tests (CF-P) establish scenarios where a
candidate SHOULD be conformant (delegated outcome, contextual
selection, bounded authority, material progression, human-agent
hybrid, non-AI agentic, localised agenticity, multi-agent
coordination). The conformance negative tests (CF-N) establish
scenarios where a candidate SHOULD be non-conformant (AI only,
agent label only, workflow only, recommendation only, fixed
automation, autonomous system without materiality, human routine
execution, missing authority, missing selection, non-material
agentic behavior). The conformance boundary tests (CF-BT) cover
the boundary matrix per CR-VAS-004 §21.

### Evidence freshness and drift

Conformance claims are time-bound. The repository supports
detection of conformance drift when authority, agent behavior,
workflow, Value Stream, agentic participation, action space,
policy, human escalation, or materiality changes. A previously
conformant instance MAY become non-conformant when its semantic
structure changes. This is different from maturity deterioration.

### Documentation set

Five new documentation files accompany this layer:

- `docs/evidence.md`. Evidence model, three levels, qualification
  evidence chain, sufficiency vocabulary, mandatory vs supporting
  evidence, provenance, confidence.
- `docs/qualification.md`. Qualification decision model, decision
  rules, materiality evidence, counterfactual validation.
- `docs/validation.md`. Validation chain (machine + evidence +
  review), roles, evidence lifecycle, freshness, conformance
  result template.
- `docs/boundary-testing.md`. Boundary test matrix per CR-VAS-004
  §21 and reconciliation with the CR-VAS-003 boundary tests.
- `docs/conformance-drift.md`. Drift triggers, drift vs maturity,
  drift handling, drift evidence.
