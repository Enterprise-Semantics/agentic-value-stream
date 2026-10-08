# Architecture Anti-Patterns (CR-VAS-008)

## Purpose

Per CR-VAS-008 §22, the following anti-patterns SHALL explicitly be
rejected.

## The Six Anti-Patterns

### AP-A01 ; Agent-Centric Architecture

**Incorrect:** "Start with agents and discover the Value Stream
afterward."

**Rejected because:** Architecture realizes AVS semantics; it does
not define them. The primary architectural object is the Value
Stream.

### AP-A02 ; Agentic Workflow Ontology

**Incorrect:** "Create a parallel workflow hierarchy merely because
agents participate."

**Rejected because:** Agentic coordination may overlay multiple
Value Stages without creating a new Value Stream hierarchy. The
overlay (AP-11) is an architectural realization pattern; it is NOT
a new semantic entity such as "Agentic Workflow."

### AP-A03 ; Full-Agentification Assumption

**Incorrect:** "Every Value Stage must become agentic."

**Rejected because:** A Value Stream can be heterogeneous (human,
automation, agentic participation in different stages).

### AP-A04 ; Autonomy Maximization

**Incorrect:** "Treat maximum autonomy as the target architecture."

**Rejected because:** Autonomy is NOT a semantic requirement for
AVS. The objective is appropriate delegated value realization within
authority boundaries, not maximum delegation.

### AP-A05 ; Technology-Led Semantics

**Incorrect:** "Define AVS based on the architecture of a particular
agent platform."

**Rejected because:** The implementation layer may change without
changing AVS semantics. Technology MUST NOT define AVS
qualification.

### AP-A06 ; Orchestration Equals Agenticity

**Incorrect:** "An orchestrator is automatically an agentic
participant."

**Rejected because:** An orchestrator's participation must satisfy
AVS qualification rules independently. Orchestrator presence does
NOT establish agentic qualification.

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-008
acceptance review (governance frame ES-ADR-058).
