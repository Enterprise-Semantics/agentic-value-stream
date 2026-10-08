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


## Measurement and Operational Value (CR-VAS-005)

Per CR-VAS-005 (Measurement & Operational Value Model, 2026-10-08),
the Agentic Value Stream repository establishes the measurement layer
that operates on top of qualification (CR-VAS-002), participation
(CR-VAS-003), and evidence & conformance (CR-VAS-004).

### Normative principle

Measurement evaluates an already-qualified and conformant AVS
implementation. Measurement does NOT determine whether the underlying
concept is semantically an AVS.

```
Activity != Effectiveness != Business Value
```

The most important design decision in CR-VAS-005 is: do not allow
measurement to become a backdoor definition of agenticity.

### Five-level measurement hierarchy

- Level 1 ; Activity. What happened?
- Level 2 ; Behavior. How did the agent behave?
- Level 3 ; Performance. How well did it perform?
- Level 4 ; Value. What value did it create or protect?
- Level 5 ; Strategic Effect. What changed because of agentic
  realization?

This prevents dashboards from becoming collections of low-level
telemetry.

### Six primary measurement dimensions

1. Value Realization (PRIMARY). Outcome realization rate, outcome
   improvement, outcome quality, value leakage, value recovery,
   exception resolution rate, time-to-outcome, outcome variance,
   customer/stakeholder outcome.
2. Agentic Effectiveness. Delegation success rate, context
   utilization rate, action selection effectiveness, adaptive
   progression effectiveness, agentic resolution rate, agentic
   decision density, agentic action selection rate, authority
   utilization.
3. Decision and Action Quality. Decision acceptance rate, action
   success rate, action reversal rate, decision override rate,
   rework rate, exception rate, downstream defect rate,
   policy-compliance rate.
4. Human Intervention. Intervention rate, intervention effectiveness,
   escalation precision, escalation miss rate, intervention success
   rate, intervention reversal rate, intervention-induced delay,
   unnecessary-intervention rate.
5. Authority and Risk. Boundary compliance rate, boundary exception
   rate, unauthorized action rate, constraint violation rate,
   escalation failure rate, risk-adjusted outcome, risk-adjusted
   value.
6. Operational Efficiency. Cost per outcome, cost per successful
   resolution, time per outcome, throughput, capacity utilization,
   human effort avoided/redirected, infrastructure cost, agent
   execution cost, exception handling cost, value stream cycle time.

### Conditional metrics

Multi-agent, adaptive progression, AI-specific, and autonomy-specific
metrics are CONDITIONAL. A single-agent AVS SHALL NOT be required to
implement multi-agent metrics. Adaptation is measurable but is NOT
itself proof of agenticity.

### Baseline model

A baseline is REQUIRED wherever an improvement claim is made. The
baseline SHALL be declared explicitly: historical, human-only,
automated, pre-agentic, controlled, counterfactual, or benchmark.

### Counterfactual comparison

```
Incremental AVS Value = AVS Result - Comparable Baseline Result
```

This is substantially more meaningful than measuring agentic activity
alone. The counterfactual MAY be demonstrated through simulation,
historical replay, controlled testing, or analytical reasoning.

### Measurement anti-patterns

- Agent Count As Value. False.
- Autonomy As Performance. False.
- Automation Rate As Agenticity. False.
- Decision Volume As Effectiveness. False.
- Intervention Minimization. False.
- AI Model Quality As Value. False.
- Cost Reduction As Sole Value. False.

### Separation principles

CR-VAS-005 explicitly separates measurement from:

- Semantic qualification (CR-VAS-002). Measurement may use
  qualification evidence as an input but SHALL NOT replace it.
- Conformance (CR-VAS-004). Measurement may use conformance evidence
  as an input but SHALL NOT replace it. A poorly performing AVS can
  remain semantically conformant. A high-performing automated system
  can remain non-conformant.
- Maturity (CR-VAS-006 territory). CR-VAS-005 SHALL NOT introduce
  maturity levels.

### Measurement-to-semantics traceability

Every core metric SHALL be traceable back to the semantic model:

- Delegated Intent -> Outcome Realization Rate.
- Bounded Authority -> Authority Compliance Rate.
- Contextual Interpretation -> Context Utilization / Adaptation
  Effectiveness.
- Action Selection -> Action Selection Effectiveness.
- Material Value Contribution -> Incremental Value / Outcome
  Improvement.
- Human Intervention -> Intervention Effectiveness.

This prevents the measurement framework from becoming disconnected
from semantics.

### Conformance kit expansion

The conformance kit now contains 91 tests:

- 5 positive (AVS-VAL-01..07, CR-VAS-002).
- 5 negative (AVS-EXC-01..07, CR-VAS-002).
- 5 edge case (AVS-EDGE-01..05, CR-VAS-002).
- 8 structural (VAS-ST-01..08, CR-VAS-003).
- 10 boundary (VAS-BT-01..10, CR-VAS-003).
- 8 conformance positive (VAS-CF-P01..P08, CR-VAS-004).
- 10 conformance negative (VAS-CF-N01..N10, CR-VAS-004).
- 10 conformance boundary (VAS-CF-BT-01..10, CR-VAS-004).
- 10 measurement positive (VAS-ME-P01..P10, CR-VAS-005).
- 10 measurement negative (VAS-ME-N01..N10, CR-VAS-005).
- 10 measurement boundary (VAS-ME-BT-01..10, CR-VAS-005).

The measurement positive tests (ME-P) establish scenarios where a
candidate SHOULD be measurable across the 6 primary dimensions. The
measurement negative tests (ME-N) cover the 7 anti-patterns and 3
separation principles. The measurement boundary tests (ME-BT)
distinguish measurement from qualification, conformance, and maturity.

### Documentation set (Wave 3 additions)

Six new documentation files accompany this layer:

- `docs/measurement.md`. Normative question, 5-level hierarchy, 6
  primary dimensions, conditional metrics, baseline model,
  counterfactual comparison, measurement context, value
  attribution, provenance chain, lifecycle, quality dimensions.
- `docs/value-realization.md`. Primary dimension detail,
  risk-adjusted value, counterfactual value.
- `docs/operational-metrics.md`. Economic and operational efficiency
  metrics, cycle time decomposition, human effort reallocation.
- `docs/measurement-baselines.md`. Baseline types, improvement
  claim rule, counterfactual value construct, conditional
  applicability.
- `docs/measurement-provenance.md`. Provenance chain, lifecycle,
  quality dimensions, measurement context.
- `docs/measurement-anti-patterns.md`. 7 anti-patterns with verdict
  (False).

## Maturity and Capability (CR-VAS-006, Wave 4)

CR-VAS-006 introduces the **organizational maturity and capability
progression model** for Agentic Value Streams. Maturity is a property
of the **organization**, not of the AVS itself. It measures how
systematically the organization can design, govern, operate, measure,
improve, and scale AVS.

The dependency is intentionally one-directional:

> Semantic Qualification -> Conformance & Evidence -> Operational
> Measurement -> Maturity & Capability.

A high-maturity organization may have non-agentic Value Streams. A
low-maturity organization may operate a semantically conformant AVS.
A highly performant AVS does not automatically imply organizational
maturity.

### Six Maturity Levels

| Level | Name | Meaning |
|---|---|---|
| L0 | Unaware | No deliberate AVS capability. |
| L1 | Aware | AVS concepts understood and identified. |
| L2 | Defined | AVS practices, boundaries and governance are defined. |
| L3 | Implemented | Conformant AVS implementations operate in production. |
| L4 | Managed | AVS performance, risk, value and improvement are systematically managed. |
| L5 | Scaled & Adaptive | AVS capability is governed and continuously optimized across the enterprise. |

Levels represent increasing organizational capability, **not**
increasing agenticity.

### Six Capability Dimensions

| ID | Dimension | Description |
|---|---|---|
| C1 | Design & Semantic Modeling | Identify, model, qualify AVS correctly. |
| C2 | Authority, Governance & Risk | Establish and govern delegated authority. |
| C3 | Operational Realization | Deploy and operate AVS reliably. |
| C4 | Value & Performance Management | Demonstrate agentic participation contribution. |
| C5 | Learning & Continuous Improvement | Improve AVS performance based on evidence. |
| C6 | Portfolio Scaling & Enterprise Integration | Scale AVS capability beyond isolated implementations. |

### Separation Principles

Maturity is **separated** from qualification, conformance, and
measurement:

- Maturity vs qualification: maturity does not determine whether a
  Value Stream is semantically an AVS.
- Maturity vs conformance: a non-conformant implementation cannot
  become conformant by achieving a higher maturity score.
- Maturity vs measurement: maturity is not a measurement score. It
  is a multidimensional organizational capability assessment.

### Maturity Anti-Patterns (rejected)

Per CR-VAS-006 §21, the following are explicitly rejected as
maturity evidence: maturity = autonomy; maturity = AI
sophistication; maturity = agent count; maturity = automation
percentage; maturity = intervention reduction; maturity = cost
reduction; maturity = production deployment; maturity = semantic
complexity.

### Maturity Tests

Wave 4 adds 30 maturity tests (10 positive + 10 negative + 10
boundary):

- 10 maturity positive (VAS-MA-P01..P10, CR-VAS-006): L1..L5
  capability, six capability dimensions, multidimensional
  assessment profile, machine-readable maturity schema, human
  participation guarantee, capability lifecycle + regression.
- 10 maturity negative (VAS-MA-N01..N10, CR-VAS-006): the eight
  anti-patterns and two anti-pattern category tests
  (maturity-as-qualification and arithmetic-average-concealment).
- 10 maturity boundary (VAS-MA-BT-01..10, CR-VAS-006):
  maturity vs qualification, conformance, measurement, AI,
  autonomy, automation, human intervention, drift/regression,
  technology maturity model, operational performance.

### Documentation set (Wave 4 additions)

Seven new documentation files accompany this layer:

- `docs/maturity.md`. Purpose, core principle, separation
  principles, scope.
- `docs/capability-model.md`. Six capability dimensions with
  detailed scope, capability progression matrix.
- `docs/maturity-levels.md`. L0..L5 with definitions, minimum
  capabilities, critical distinctions, gates.
- `docs/maturity-assessment.md`. Assessment principle, multi-
  dimensional assessment rule, overall maturity rule, mandatory
  gates, evidence requirements by level, assessment record
  template, assessment frequency.
- `docs/capability-gaps.md`. Gap model, gap types, improvement
  planning chain.
- `docs/maturity-governance.md`. Governance roles, capability
  lifecycle, transition criteria, drift, regression, enterprise
  architecture relationship.
- `docs/maturity-anti-patterns.md`. Eight anti-patterns with
  rejection rationale and detection heuristics.

## Governance, Lifecycle & Portfolio (CR-VAS-007, Wave 5)

CR-VAS-007 establishes the **management control plane** around the
already-defined AVS semantic object. Governance does NOT redefine
AVS semantics; it governs how conformant AVS are created, changed,
monitored, suspended, retired, and managed across an enterprise
portfolio.

### Core Principle

An Agentic Value Stream is governed as a **Value Stream with agentic
participation**, not as an autonomous technology asset.

```
Value Stream
   -> Agentic Participation
     -> Authority
       -> Risk
         -> Outcome
           -> Governance
```

rather than `AI Model -> Agent -> Agentic System -> Governance`.

### Ten Lifecycle States

| State | Meaning |
|---|---|
| Proposed | Candidate identified for agentic realization. |
| Assessed | Initial evaluation covering relevance, authority, risk, materiality. |
| Designed | Formal design (scope, intent, authority, action space, etc.). |
| Qualified | Semantic qualification + evidence satisfied. |
| Approved | Governance authority authorizes implementation or operation. |
| Implemented | Realization exists technically/operationally. |
| Operational | Actively realizing value. Required controls active. |
| Managed | Systematic measurement, monitoring, risk, value, conformance, improvement. |
| Suspended | Temporary cessation of agentic realization. |
| Retired | No longer authorized for operational use. |

### Seven Governance Domains

| ID | Domain |
|---|---|
| G1 | Semantic Governance |
| G2 | Authority Governance |
| G3 | Operational Governance |
| G4 | Risk & Policy Governance |
| G5 | Value Governance |
| G6 | Change Governance |
| G7 | Portfolio Governance |

### Change Classification (4 Classes)

| Class | Meaning |
|---|---|
| Class A | Non-Material ; no requalification required. |
| Class B | Controlled ; targeted review required. |
| Class C | Material ; formal revalidation required. |
| Class D | Critical ; governance approval required before implementation. |

### Governance Anti-Patterns (rejected)

Per CR-VAS-007 §39, the following are explicitly rejected: approval
equals qualification; no revalidation; irrevocable authority;
agent controls policy; no fallback; portfolio by agent count.

### Runtime vs Governance Policy Distinction

```
Instruction != Policy != Authority != Governance Decision
```

An agent instruction cannot legitimately override a higher-order
authority constraint (AVS-GOV-INV-013). The policy hierarchy is
Enterprise -> Domain -> Value Stream -> AVS -> Authority Boundary
-> Runtime Enforcement.

### Governance Tests

Wave 5 adds 30 governance tests (10 positive + 10 negative + 10
boundary):

- 10 governance positive (VAS-GV-P01..P10, CR-VAS-007): lifecycle
  management, seven governance domains, material change
  revalidation, authority revocation, safe suspension and
  fallback, portfolio governance, capability reuse and avoidance
  of agent sprawl, governance evidence and decision types,
  runtime instruction shall not override authority, governance
  metrics and dashboard.
- 10 governance negative (VAS-GV-N01..N10, CR-VAS-007): the six
  anti-patterns and four additional negative tests (governance
  redefines semantics, operational status implies continuing
  conformance, lifecycle without retirement support, governance
  decisions without evidence).
- 10 governance boundary (VAS-GV-BT-01..10, CR-VAS-007):
  governance vs semantic qualification, qualification vs
  approval, lifecycle state vs governance status, material vs
  non-material change, authority escalation vs normal authority
  use, conformance drift vs version change, governance maturity
  vs AVS maturity, governance metrics vs measurement metrics,
  intervention as control vs intervention as failure, governance
  RACI vs ontology responsibility.

### Documentation set (Wave 5 additions)

Eight new documentation files accompany this layer:

- `docs/governance.md`. Purpose, core principle, governance
  objective, dimensions, scope.
- `docs/lifecycle.md`. 10-state lifecycle, non-linearity, state
  separation.
- `docs/change-management.md`. Material change concept, change
  classification (4 classes), change decision model.
- `docs/authority-governance.md`. Authority record schema,
  escalation, revocation, governance evidence.
- `docs/suspension-and-recovery.md`. Suspension triggers,
  fallback patterns, emergency controls, recovery.
- `docs/portfolio-governance.md`. Portfolio inventory,
  prioritization, capability reuse, agent sprawl avoidance,
  concentration risk.
- `docs/governance-metrics.md`. Six governance metrics,
  dashboard views.
- `docs/governance-anti-patterns.md`. Six anti-patterns with
  rejection rationale.

## Architecture Patterns & Reference Architectures (CR-VAS-008, Wave 6)

CR-VAS-008 translates the established semantic model into
architecture without introducing implementation-specific concepts
into the AVS ontology.

### Core Principle

> Architecture realizes Agentic Value Stream semantics; it does
> NOT define them.

The dependency is intentionally one-directional:

```
AVS Semantics
   -> Participation Model
     -> Governance & Authority
       -> Architecture Pattern
         -> Technology Realization
```

NOT:

```
Technology Platform
   -> Agent Architecture
     -> "Agentic Value Stream"
```

### Six Architectural Planes

| ID | Plane | Represents |
|---|---|---|
| P1 | Value & Outcome Plane | Stakeholder, outcome, value, Value Stream, value realization, outcome measures. The business anchor. |
| P2 | Value Stream Realization Plane | Value Stages, progression, decisions, actions, handoffs, dependencies, realization boundaries. |
| P3 | Agentic Participation Plane | Actor, entrusted intent, contextual interpretation, action selection, progression, coordination, intervention. Implements CR-VAS-003. |
| P4 | Control & Governance Plane | Authority, policy, constraints, risk, approval, escalation, intervention, revocation, audit, governance. |
| P5 | Knowledge & Context Plane | Enterprise data, knowledge, business state, customer context, external signals, policies, historical information. |
| P6 | Technology & Integration Plane | Applications, APIs, services, agent runtimes, models, workflow systems, automation, event infrastructure, data platforms. Technology is realization infrastructure, not AVS semantics. |

### Twelve Architecture Patterns (AP-01..AP-12)

| Pattern | Summary |
|---|---|
| AP-01 | Agentic Stage Participation ; localized agentic realization in one stage. |
| AP-02 | Agentic Decision ; concentrated around a consequential decision. |
| AP-03 | Agentic Execution ; selects among permissible execution alternatives. |
| AP-04 | Human-Agent Hybrid ; explicit human interaction. |
| AP-05 | Agent-to-Human Escalation ; boundary-condition escalation with explicit threshold. |
| AP-06 | Human-to-Agent Delegation ; entrusted intent + bounded authority. |
| AP-07 | Distributed Agentic Participation ; multiple agents across the Value Stream. |
| AP-08 | Coordinated Multi-Agent Realization ; optional multi-agent architecture. |
| AP-09 | Agentic Orchestration ; orchestrator is not automatically agentic. |
| AP-10 | Agentic Exception Resolution ; agenticity for material exceptions only. |
| AP-11 | Agentic Coordination Overlay ; overlay, NOT a new semantic entity like "Agentic Workflow." |
| AP-12 | Progressive Delegation ; governed progression, NOT maturity progression. |

### Architecture Anti-Patterns (rejected)

Per CR-VAS-008 §22, the following are explicitly rejected: agent-centric
architecture; agentic workflow ontology; full-agentification
assumption; autonomy maximization; technology-led semantics;
orchestration equals agenticity.

### Architecture Tests

Wave 6 adds 18 architecture tests (6 positive + 6 negative + 6
boundary):

- 6 architecture positive (VAS-AP-P01..P06, CR-VAS-008): six
  architectural planes, twelve architecture patterns, four
  architecture boundaries, architecture decision record template,
  architecture quality attributes, heterogeneous Value Streams.
- 6 architecture negative (VAS-AP-N01..N06, CR-VAS-008): the six
  anti-patterns.
- 6 architecture boundary (VAS-AP-BT-01..06, CR-VAS-008):
  architecture vs semantic qualification, multi-agent vs agentic,
  orchestrator vs agentic participant, technology substitution vs
  AVS identity, context access vs context interpretation,
  progressive delegation vs maturity progression.

### Documentation set (Wave 6 additions)

Six new documentation files accompany this layer:

- `docs/architecture.md`. Purpose, core principle, normative
  question, scope.
- `docs/reference-architecture.md`. Six architectural planes with
  detailed scope; canonical architecture pattern.
- `docs/architecture-patterns.md`. Twelve reusable patterns
  AP-01..AP-12.
- `docs/architecture-boundaries.md`. Four architectural boundaries.
- `docs/architecture-decisions.md`. Architecture decision record
  template, quality attributes, selection criteria.
- `docs/architecture-anti-patterns.md`. Six anti-patterns with
  rejection rationale.

## Semantic Versioning, Evolution & Migration (CR-VAS-010, Wave 7)

Per CR-VAS-010, Wave 7 introduces the `versioning:` block in
`concept.yaml`, formalising how the AVS semantic contract evolves
deliberately, transparently, and traceably. Version 1.6.0 is
incremented to 1.7.0 with 18 new tests using the `sv-` prefix
(6 positive + 6 negative + 6 boundary = 187 total).

The block comprises 20 sub-keys:

- `principle`: The AVS semantic contract MUST evolve deliberately,
  transparently, and traceably; distinguish semantic from
  implementation and documentation change.
- `change_classification`: Nine classes (Editorial, Clarification,
  Additive, Structural, Semantic, Breaking, Deprecation, Corrective,
  Multi-classification); classification MUST reflect actual impact,
  not diff size.
- `versioning_policy`: SemVer MAJOR.MINOR.PATCH with explicit rules
  per tier (major examples: changing qualification conditions,
  removing mandatory properties, redefining invariants; minor:
  optional properties, new optional patterns; patch: typo, broken
  link, test fixture repair).
- `version_distinction`: Specification vs artifact version split
  with a mandatory warning that an artifact MUST NOT declare
  compatibility with a spec version if it contradicts the spec.
- `canonical_authority`: Per-artifact record with id, authoritative
  location, artifact version, specification version, status, owner,
  dependencies, compatibility declaration, supersession history.
- `normative_vs_informative`: Asset classification plus warning
  that informative status MUST NOT be used to evade review.
- `compatibility_dimensions`: Five dimensions (Definition, Instance,
  Schema, Conformance, Mapping) plus warning that schema-compatible
  does not equal semantically-compatible.
- `qualification_change_review`: Heightened review checklist and
  rule that qualification change MUST NOT be released as a patch.
- `invariant_evolution`: Per-invariant template (id, statement,
  rationale, introduced_in, status, verification) plus stability
  and meaning-change rules.
- `controlled_vocabulary_evolution`: Five rules covering add,
  rename, remove, redefinition, and unknown-value handling.
- `deprecation_lifecycle`: Active -> Deprecated -> Retired with
  per-deprecation documentation checklist.
- `migration_model`: Migration record template plus rule that
  transformations MUST be explicit and the repository MUST NOT
  silently infer missing semantic evidence.
- `migration_classes`: Five classes M0..M4 (No, Mechanical,
  Reviewed, Semantic Reassessment, Requalification Required).
- `dual_version_support`: Cross-version conformance rules plus
  principle that conformant-to-one does not imply conformant-to-another.
- `release_manifest`: Machine-readable manifest template with
  compatibility, changes, and migration fields.
- `change_request_requirements`: 14-item mandatory checklist
  (problem, current position, proposed change, rationale,
  classification, compatibility, invariants, schemas, tests,
  mappings, migration, documentation, acceptance, rollback).
- `impact_analysis`: Repository + downstream impact chain plus
  rule that the dependency graph MUST be derived from repository
  metadata, not maintained as a hand-drawn diagram.
- `invariants`: Eight normative invariants SV-INV-001..008 binding
  classification, SemVer-as-convention, qualification-as-patch
  prohibition, invariant ID stability, explicit migration, cross-
  repo conflict prohibition, cross-version re-labelling
  prohibition, and schema/semantic compatibility distinction.
- `boundary_assertions`: Per-CR-VAS-010 evolution principle binding
  the block to its release-time impact analysis.

### Documentation set (Wave 7 additions)

Eight new documentation files accompany this layer:

- `docs/versioning.md`. Purpose, core principle, scope, applies-to,
  depends-on.
- `docs/change-classification.md`. Nine-class taxonomy table with
  per-class meaning and example.
- `docs/versioning-policy.md`. SemVer MAJOR.MINOR.PATCH policy with
  per-tier examples, spec-vs-artifact distinction.
- `docs/deprecation-and-migration.md`. Deprecation lifecycle, migration
  model template, five migration classes M0..M4.
- `docs/release-process.md`. Release manifest template, dual-version
  support, 14-item change request checklist, impact analysis chain.
- `docs/versioning-invariants.md`. SV-INV-001..008 table with
  statement, rationale, and verification anchors.
- `docs/controlled-vocabulary.md`. Vocabulary template plus five
  evolution rules.
- `docs/versioning-anti-patterns.md`. Ten anti-patterns with
  detection anchors (SV-INV-001..008 + CR-VAS-010 §3, §4, §7, §11,
  §14, §17).

### PUML diagrams (Wave 7 additions)

Three new PUML diagrams visualise the layer:

- `diagrams/semantic-evolution-lifecycle.puml`. State diagram of the
  end-to-end change flow: Change Proposed -> Classify -> Impact
  Analysis -> Migration Class -> SemVer -> Release Manifest ->
  Compatibility Reported.
- `diagrams/migration-classes.puml`. Trigger conditions and class
  ladder for M0..M4 with downgrade refusal under semantic impact.
- `diagrams/release-process.puml`. Activity diagram of the release
  process with SV-INV-003 (qualification-as-patch rejection) and
  SV-INV-006 (cross-repo conflict rejection) gates.

### Mapping alignment (Wave 7 additions)

The WSF and OpenDEA mapping files receive `versioning_alignment`
blocks:

- `mappings/wsf.yaml` -> `versioning_alignment` with eight WSF
  correspondences (SemVer, spec-vs-artifact, compatibility report,
  migration records, release manifest, change request checklist).
- `mappings/opendea.yaml` -> `versioning_alignment` with eight
  OpenDEA correspondences (change management, canonical source of
  truth, invariant lifecycle, vocabulary governance, deprecation,
  dual-version support, dependency analysis, normative invariants).

Both blocks carry five-dimension compatibility evidence (semantic,
schema, conformance, instance, mapping = compatible) and anchor
SV-INV-001..008.

Wave 7 adds 18 versioning tests (6 positive + 6 negative + 6
boundary = 187 total in the conformance inventory), the
`versioning:` block, the eight-versioning-doc documentation set,
the three-versioning-visual PUML set, the two mapping alignment
blocks, and updates the kit manifest (`kit/kit.yaml` v1.7.0,
provenance now includes ES-ADR-059 and CR-VAS-010, and
`boundary_assertions` includes `per_cr_vas_010_versioning_evolution`).
The 9 of 9 governance frame (ES-ADR-059 + CR-VAS-010) is authored
in `enterprise-semantics-governance` at slot 0059/0062 and pushed
alongside this wave.
