# Architecture Boundaries (CR-VAS-008)

## Four Architectural Boundaries

Every AVS architecture SHOULD identify four boundaries.

### Value Boundary

Where Value Stream realization begins and ends.

### Agentic Boundary

Where delegated agentic participation occurs.

### Authority Boundary

What the agent may and may not decide or execute.

### Technology Boundary

Which systems and infrastructure implement the realization.

## Boundary Diagram

```
+-----------------------------------+
|        VALUE BOUNDARY             |
|                                   |
|  +-----------------------------+  |
|  |     AGENTIC BOUNDARY        |  |
|  |                             |  |
|  |  Intent -> Context -> Sel.  |  |
|  |           v                 |  |
|  |   AUTHORITY BOUNDARY         |  |
|  |           v                 |  |
|  |         Action              |  |
|  +-----------------------------+  |
|                                   |
|     TECHNOLOGY BOUNDARY           |
+-----------------------------------+
```

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-008
acceptance review (governance frame ES-ADR-058).
