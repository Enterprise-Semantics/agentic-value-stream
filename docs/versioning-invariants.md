# Versioning Invariants

**Topic:** SV-INV-001..008: Normative Invariants for Versioning
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

List the eight normative invariants (SV-INV-001..008) introduced by CR-VAS-010 to govern how the AVS semantic contract evolves, and identify which versioning tests, mappings, and architecture decisions bind each invariant.

## Core principle

Each invariant has a stable identifier, a normative statement, a rationale, an effective specification version, a status, and a test or verification method where applicable. Invariant identifiers SHOULD remain stable across releases when their meaning remains stable. If an invariant's meaning changes materially, the repository MUST document the change explicitly rather than silently reusing its identifier.

## Scope

All AVS versions and all versioning change requests.

## Normative invariants

| ID | Statement | Rationale |
|---|---|---|
| SV-INV-001 | Semantic change MUST be classified; classification MUST reflect actual impact, not diff size. | Prevents diff-size-driven classification and the silent blending of breaking and editorial changes. |
| SV-INV-002 | SemVer is a release convention; semantic compatibility MUST be assessed and evidenced independently. | Prevents SemVer from being treated as a guarantee of compatibility without explicit review. |
| SV-INV-003 | A change that alters qualification criteria MUST NOT be released as a patch. | Prevents qualification drift under patch-version labels. |
| SV-INV-004 | Invariant identifiers SHOULD remain stable across releases when their meaning remains stable. | Supports traceability of invariants across versions and avoids silent meaning changes. |
| SV-INV-005 | Migration transformations MUST be explicit; the repository MUST NOT silently infer missing semantic evidence to make legacy instances pass a newer conformance suite. | Prevents false-positive conformance for legacy instances under new suites. |
| SV-INV-006 | Multiple repositories MUST NOT independently evolve conflicting canonical definitions without an explicit reconciliation mechanism. | Prevents canonical drift across the Enterprise-Semantics repository family. |
| SV-INV-007 | An instance conformant to one version MUST NOT automatically be labelled conformant to another. | Prevents silent cross-version re-labelling during dual-version support windows. |
| SV-INV-008 | Schema-compatible change may still be semantically breaking; the compatibility report MUST make that distinction explicit. | Prevents reports that mask semantic breaking behind schema-compatibility claims. |

## Verification anchors

- VAS-SV-P01 (Classification Taxonomy)
- VAS-SV-P02 (SemVer Policy)
- VAS-SV-P04 (Five-Dimension Compatibility)
- VAS-SV-P06 (Five Migration Classes)
- VAS-SV-N01..N06 (Negative Cases)
- VAS-SV-BT-01..BT-06 (Boundary Cases)

## Versioning anchor

`versioning.invariants`

## Dependents

- Versioning policy (this version)
- Deprecation and migration (this version)
- Release process (this version)

## Boundary assertion

Per CR-VAS-010 §10, each invariant MUST have a stable identifier, a normative statement, a rationale, an effective specification version, a status, and a test or verification method where applicable. Per SV-INV-004, identifiers SHOULD remain stable when meaning is stable. Per SV-INV-005, migration MUST be explicit.

## Next

For controlled vocabulary evolution rules, see `controlled-vocabulary.md`. For anti-patterns, see `versioning-anti-patterns.md`.
