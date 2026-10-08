# Release Process

**Topic:** Release Manifest, Dual-Version Support, and Change Request Workflow
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

Per CR-VAS-010 §15, §16, §17, define the machine-readable release manifest, dual-version support rules, and the 14-item change request requirements that every semantic change request MUST include.

## Core principle

Compatibility values MUST be justified by the release review, not automatically inferred from the version number. An instance conformant to one version MUST NOT automatically be labelled conformant to another. The actual dependency graph MUST be derived from repository metadata and references rather than maintained only as a manually written diagram.

## Scope

Every release of the published AVS specification, and every change request that affects the semantic contract.

## Release manifest

```yaml
release: specification, version, status, previous_version, compatibility (semantic, schema, conformance), changes (id, classification, affected_artifacts), migration (required, guide).
```

## Dual-version support

During a major-version transition, the repository MAY support two specification versions concurrently. If so, it MUST declare: supported versions; conformance rules for each version; migration expectations; end-of-support dates or criteria; treatment of cross-version mappings.

## Change request requirements (14 items)

1. `problem_statement`
2. `current_normative_position`
3. `proposed_change`
4. `semantic_rationale`
5. `classification`
6. `compatibility_impact`
7. `affected_invariants`
8. `affected_schemas`
9. `affected_conformance_tests`
10. `affected_mappings`
11. `migration_requirements`
12. `documentation_changes`
13. `acceptance_criteria`
14. `rollback_or_remediation_approach`

## Impact analysis chain

```text
Changed Definition -> Invariants -> Qualification Rules -> Schemas -> Conformance Tests -> Architecture Patterns -> Mappings -> Examples & Documentation.
```

## Versioning anchor

`versioning.release_manifest + versioning.dual_version_support + versioning.change_request_requirements + versioning.impact_analysis`

## Dependents

- Versioning policy (this version)
- Deprecation and migration (this version)
- Versioning invariants (this version)

## Boundary assertion

Per CR-VAS-010, compatibility values MUST be justified by the release review, not automatically inferred from the version number. Per SV-INV-007, an instance conformant to one version MUST NOT automatically be labelled conformant to another. Per SV-INV-008, schema-compatible change may still be semantically breaking; the compatibility report MUST make that distinction explicit.

## Next

For controlled vocabulary evolution rules, see `controlled-vocabulary.md`. For invariants governing release, see `versioning-invariants.md`.
