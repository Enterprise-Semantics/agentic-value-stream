# Deprecation and Migration

**Topic:** Deprecation Lifecycle and Migration Model
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

Per CR-VAS-010 §11, §12, §13, §14, define the deprecation lifecycle (Active -> Deprecated -> Retired), migration model, and the five migration classes (M0..M4) used to characterise the work required when an AVS artifact moves between specification versions.

## Core principle

Deprecation MUST NOT imply immediate invalidity unless the release explicitly states that the item is no longer accepted. Migration MUST preserve traceability between the old and new representations. Migration transformations MUST be explicit. The repository MUST NOT silently infer missing semantic evidence merely to make legacy instances pass a newer conformance suite.

## Scope

All artifacts subject to versioning per CR-VAS-010 §5, including canonical definitions, schemas, controlled vocabularies, evidence requirements, mappings, and implementation profiles.

## Deprecation lifecycle

Active -> Deprecated -> Retired. Each deprecated artifact or property MUST document: reason for deprecation; version in which deprecation was introduced; replacement, if one exists; compatibility implications; migration instructions; earliest intended removal version.

## Migration model

```yaml
migration: id, from_specification, to_specification, affected_artifacts, transformations (source_field, target_field, transformation), semantic_review_required, automated.
```

## Migration classes

| Class | Name | Meaning |
|---|---|---|
| M0 | No migration | Existing artifacts remain valid. |
| M1 | Mechanical | Deterministic structural transformation with no semantic reinterpretation. |
| M2 | Reviewed | Transformation requires validation or human review. |
| M3 | Semantic Reassessment | Affected instances must be reassessed against changed qualification or invariant requirements. |
| M4 | Requalification Required | The change requires formal reevaluation before the instance can claim conformance to the new release. |

## Versioning anchor

`versioning.deprecation_lifecycle + versioning.migration_model + versioning.migration_classes`

## Dependents

- Versioning policy (this version)
- Release manifest (this version)
- Dual-version support (this version)

## Boundary assertion

Per CR-VAS-010, migration transformations MUST be explicit. Per SV-INV-005, the repository MUST NOT silently infer missing semantic evidence to make legacy instances pass a newer conformance suite. Per CR-VAS-010, the migration class MUST be selected based on semantic impact, not implementation convenience.

## Next

For invariants governing the migration model, see `versioning-invariants.md`. For anti-patterns to avoid, see `versioning-anti-patterns.md`.
