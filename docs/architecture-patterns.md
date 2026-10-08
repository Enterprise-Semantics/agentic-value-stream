# Architecture Patterns (CR-VAS-008)

## Twelve Reusable Patterns

CR-VAS-008 defines twelve reusable architecture patterns.

### AP-01 ; Agentic Stage Participation

An AVS contains a localized agentic realization within one Value
Stage.

```
Stage A -> [Agentic Stage Participation] -> Stage C
```

Use when: only one stage requires contextual decisions; other
stages remain human or automated; localized delegation is
preferable. **This is NOT an "Agentic Value Stage" semantic type.**

### AP-02 ; Agentic Decision

Agentic participation is concentrated around a consequential
decision.

```
Context -> Agentic Decision -> Selected Path -> Value Stream
   Progression
```

Examples: case routing; eligibility determination; treatment of an
exception; prioritization; resource allocation. The architecture
must demonstrate that the decision affects Value Stream
progression.

### AP-03 ; Agentic Execution

The agent determines or selects how an intended action is executed
within bounded authority.

```
Intent -> Context -> Action Selection -> Execution
```

The agent may select among permissible execution alternatives.

### AP-04 ; Human-Agent Hybrid

Agentic participation operates with explicit human interaction.

Primary: Human Intent -> Agent Interpretation -> Agent
Recommendation / Selection -> Human Decision -> Agent Execution.

Alternative: Agent -> Exception -> Human -> Resolution -> Agent.

This is a first-class AVS architecture pattern.

### AP-05 ; Agent-to-Human Escalation

The agent operates within delegated authority until a boundary
condition is encountered.

```
Agent
   -> Within Authority?
     -> YES: Continue
     -> NO: Escalate -> Human
```

The escalation threshold must be explicit.

### AP-06 ; Human-to-Agent Delegation

A human or organizational role delegates a defined outcome or
decision scope to an agent.

```
Human / Role -> Entrusted Intent -> Bounded Authority -> Agentic
   Participation
```

Delegation is NOT equivalent to issuing a task instruction.

### AP-07 ; Distributed Agentic Participation

Multiple agents participate in different portions of the Value
Stream.

```
Value Stream
   |
+--+-----+--+
v         v
Agent A  Agent B
```

Each participation point must retain: intent; authority; context;
action selection; outcome contribution.

### AP-08 ; Coordinated Multi-Agent Realization

Multiple agents jointly contribute to a Value Stream outcome.
Coordination may involve: task allocation; negotiation; information
exchange; shared state; escalation; synchronization. Multi-agent
architecture is **optional**; it is not a semantic requirement for
AVS.

### AP-09 ; Agentic Orchestration

An orchestrating actor coordinates multiple realizations.

```
Intent -> Orchestrator -> Agent A / Agent B / Human -> Outcome
```

The orchestrator itself does NOT automatically qualify as Agentic.
Its participation must satisfy the AVS qualification rules.

### AP-10 ; Agentic Exception Resolution

The normal Value Stream is largely deterministic, but material
exceptions require agentic interpretation and selection.

```
Normal Flow -> Exception -> Contextual Interpretation -> Agentic
   Selection -> Resolution -> Resume Value Stream
```

Especially important because agenticity need not dominate the
entire Value Stream.

### AP-11 ; Agentic Coordination Overlay

Agentic coordination may operate across multiple Value Stages
without creating a new Value Stream hierarchy.

```
Stage A ----- Stage D
       \   //
   Agentic Overlay
```

The overlay is an architectural realization pattern. It is NOT a
new semantic entity such as "Agentic Workflow."

### AP-12 ; Progressive Delegation

Delegated authority can increase or decrease according to defined
governance criteria.

```
Advisory -> Delegated Selection -> Bounded Execution -> Expanded
   Delegation
```

Progression must be governed by evidence and authority policy. It
must NOT be interpreted as mandatory maturity progression.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-008
acceptance review (governance frame ES-ADR-058).
