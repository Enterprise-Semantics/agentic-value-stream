# Boundary Testing ; Agentic Value Stream

Per CR-VAS-004 §21, the conformance kit includes an explicit boundary
test matrix that distinguishes Agentic Value Stream participation
from adjacent constructs.

## Boundary test matrix

| Scenario | Agentic? | Reason |
|---|---|---|
| LLM generates a response | Not necessarily | No delegated action authority. |
| AI recommends an action | Not necessarily | Recommendation != selection. |
| Agent selects within policy | Yes, if material | Delegated bounded selection. |
| RPA executes fixed workflow | No | Deterministic execution. |
| Autonomous vehicle performs transport | Not automatically | Autonomous != AVS. |
| Human resolves exceptional case | Potentially | Conditions must be satisfied. |
| Agent routes tickets using fixed rules | No | Routing alone insufficient. |
| Agent selects customer remediation | Potentially yes | Depends on authority/materiality. |
| Multi-agent negotiation affects fulfilment | Potentially yes | Requires qualification evidence. |
| AI forecasts demand | No | Prediction != agentic realisation. |

## Boundary tests in the kit

The repository carries three categories of boundary tests:

- Boundary tests VAS-BT-01..10 (CR-VAS-003 §24). Participation
  boundary distinction; AI, automation, workflow, autonomous system,
  human discretion, hybrid, multi-agent, non-AI.
- Boundary tests VAS-CF-BT-01..10 (CR-VAS-004 §21). Evidence
  boundary distinction; LLM response, AI recommendation, agent
  within policy, RPA, autonomous vehicle, human exceptional
  resolution, fixed-rule routing, customer remediation, multi-agent
  negotiation, AI forecast.

The two sets are complementary. The participation boundaries (003)
distinguish participation from adjacent constructs. The evidence
boundaries (004) distinguish evidentiary sufficiency from
insufficiency.

## Cardinal author rule preserved

Emmanuel A. Otchere (cardinal author rule, 2026-09-23). D-004 dash
rule: 0 en-dash (U+2013), 0 em-dash (U+2014), 0 triple-em-dash
(U+2E3B). WSF metamodel not modified. OpenDEA metamodel not
modified.
