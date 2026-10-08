# Reference Architecture (CR-VAS-008)

## The Primary Architectural Object

The primary architectural object remains the **Value Stream
realization**. Agentic components are positioned according to where
delegated decision/action capability is required.

Thus a Value Stream can be heterogeneous:

```
Value Stream
   +-- Value Stage A
   |     +-- Human
   +-- Value Stage B
   |     +-- Agentic Participation
   +-- Value Stage C
   |     +-- Automation
   +-- Value Stage D
         +-- Human + Agent
```

## Six Architectural Planes

The canonical AVS reference architecture uses six architectural
planes. This layering deliberately keeps technology at the bottom of
the semantic dependency chain.

### P1 ; Value & Outcome Plane

Represents: stakeholder; outcome; value; Value Stream; value
realization; outcome measures. This is the business anchor.

### P2 ; Value Stream Realization Plane

Represents: Value Stages; progression; decisions; actions; handoffs;
dependencies; realization boundaries. Agentic participation is
positioned here rather than creating a parallel "agentic process."

### P3 ; Agentic Participation Plane

Represents: actor; entrusted intent; contextual interpretation;
action selection; progression; coordination; intervention. This
plane implements the semantics established in CR-VAS-003.

### P4 ; Control & Governance Plane

Represents: authority; policy; constraints; risk; approval;
escalation; intervention; revocation; audit; governance.

### P5 ; Knowledge & Context Plane

Represents the information required for contextual interpretation:
enterprise data; knowledge; business state; customer context;
external signals; policies; historical information. The architecture
MUST distinguish access to context from interpretation of context.

### P6 ; Technology & Integration Plane

Represents implementation mechanisms: applications; APIs; services;
agent runtimes; models; workflow systems; automation; event
infrastructure; data platforms. Technology is realization
infrastructure, not AVS semantics.

## Canonical Architecture Pattern

The default pattern is:

```
Value Stream
   |
   v
Agentic Participation
   |
+---+----+
v   v    v
Intent Context Authority
   |
   v
Decision / Selection
   |
   v
Action
   |
   v
Value Outcome
```

Governance surrounds the entire realization:

```
        +---------------------------+
        |       GOVERNANCE          |
        | Policy + Authority + Risk |
        | Intervention + Audit      |
        +-------------+-------------+
                      |
Value Stream -> Agentic Participation -> Outcome
                      |
                  Technology
```

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-008
acceptance review (governance frame ES-ADR-058).
