# Versioning Anti-Patterns

**Topic:** Anti-Patterns for Semantic Versioning and Evolution
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

Catalogue the versioning anti-patterns that CR-VAS-010 explicitly forbids, paired with the SV-INV invariants and change request requirements that detect and prevent them.

## Core principle

Anti-patterns in versioning are not implementation bugs. They are commitments that contradict the semantic contract, even when the diff is small. The repository MUST avoid these patterns across the AVS specification, every artifact, and every release.

## Scope

All semantic change requests, all releases, and all migration records.

## Anti-patterns

| Anti-pattern | Description | Detection anchor |
|---|---|---|
| Diff-Size Classification | Classifying a change by the size of the code or documentation diff rather than by its actual semantic impact. SV-INV-001 binds. | Use the nine-class taxonomy from `change-classification.md`. A one-line invariant change may be a Breaking + Semantic change. |
| SemVer As Compatibility | Treating a SemVer increment as a guarantee that compatibility has been preserved. SV-INV-002 binds. | Compatibility MUST be assessed and evidenced across Definition, Instance, Schema, Conformance, and Mapping dimensions. |
| Qualification Change As Patch | Releasing a change that alters qualification criteria as a patch. SV-INV-003 binds. | Qualification changes are Breaking + Semantic and MUST be released as a major version (or an explicitly approved equivalent policy). |
| Cross-Repo Conflicting Evolution | Two repositories evolving the same canonical definition in divergent ways. SV-INV-006 binds. | Establish an explicit reconciliation mechanism and declare canonical authority per `versioning.md` §Canonical Semantic Authority. |
| Silent Migration Inference | Inferring missing semantic evidence to make legacy instances pass a newer conformance suite. SV-INV-005 binds. | Migration transformations MUST be explicit and machine-readable. |
| Value Re-Definition | Redefining a controlled vocabulary value to mean something materially different. CR-VAS-010 §11 binds. | Use the deprecation lifecycle and introduce a new value rather than re-defining the existing one. |
| Cross-Version Re-Labelling | Auto-labelling an instance as conformant to a new version merely because it was conformant to the old. SV-INV-007 binds. | Dual-version support MUST declare conformance rules per version; instances are re-labelled only after explicit re-evaluation. |
| Schema-Compat Equals Semantic-Compat | Reporting schema compatibility alone as evidence of semantic compatibility. SV-INV-008 binds. | The compatibility report MUST include semantic, schema, conformance, instance, and mapping dimensions and call out divergence between them. |
| Evading Review Via Informative Status | Marking a change informative to avoid review when the example implicitly changes normative meaning. CR-VAS-010 §7 binds. | Informative status MUST NOT be used to evade review when an example implicitly changes a normative rule. |
| Manual Dependency Diagrams | Maintaining the dependency graph as a hand-written diagram only. CR-VAS-010 §18 binds. | The actual dependency graph MUST be derived from repository metadata and references. |

## Versioning anchor

`versioning.invariants + versioning.change_classification + versioning.migration_model`

## Dependents

- Versioning policy (this version)
- Deprecation and migration (this version)
- Versioning invariants (this version)

## Boundary assertion

Per CR-VAS-010, every anti-pattern above is detectable from the semantic contract itself: it does not require a behavioural test. Detecting them at release-review time is part of the gate policy that the validation harness in CR-VAS-011 will operationalise.

## Next

For the validation harness that operationalises these anti-pattern checks, see CR-VAS-011 (`validation.md`).
