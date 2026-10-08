# Controlled Vocabulary

**Topic:** Controlled Vocabulary Evolution
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

Per CR-VAS-010 §11, define how controlled vocabularies are added, deprecated, renamed, or removed. Establishes the rule that a value MUST NOT be redefined to mean something materially different.

## Core principle

Renaming a value MUST preserve its identity through an explicit alias or migration mapping where appropriate. Removing a value requires a deprecation and migration policy. Unknown values MUST be handled according to the consuming schema's declared extensibility policy.

## Scope

All controlled vocabularies in the AVS semantic contract, including avs-agentic-scope (decision, execution, cross_stage) and related taxonomies used in qualification, evidence, governance, architecture, and interoperability.

## Vocabulary template

```yaml
vocabulary: id, version, values (id, status).
```

## Rules

- New compatible values may be introduced additively.
- Renaming a value MUST preserve its identity through an explicit alias or migration mapping where appropriate.
- Removing a value requires a deprecation and migration policy.
- A value MUST NOT be redefined to mean something materially different.
- Unknown values MUST be handled according to the consuming schema's declared extensibility policy.

## Versioning anchor

`versioning.controlled_vocabulary_evolution`

## Dependents

- Versioning policy (this version)
- Deprecation and migration (this version)
- Versioning invariants (this version)

## Boundary assertion

Per CR-VAS-010, a controlled vocabulary value MUST NOT be redefined to mean something materially different. Per CR-VAS-010, removing a value requires a deprecation and migration policy. The status field on each value MUST remain consistent with the deprecation lifecycle (Active -> Deprecated -> Retired).

## Next

For anti-patterns to avoid when evolving controlled vocabularies, see `versioning-anti-patterns.md`.
