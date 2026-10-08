# Change Classification

**Topic:** Change Classification Taxonomy
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

Per CR-VAS-010 §3, define the nine change classifications that every proposed change MUST be assigned to one or more of. Classification MUST reflect actual impact, not the size of the code or documentation diff.

## Core principle

A change may have multiple classifications. For example, a semantic change may also be breaking. Classification is a property of the change's impact on the semantic contract, not of the size of its code or documentation diff.

## Scope

Every change to the AVS semantic contract, including canonical definitions, qualification rules, invariants, schemas, controlled vocabularies, evidence requirements, measurement, maturity/governance models, architecture patterns, mappings, examples, and conformance fixtures.

## Change classes

| Class | Meaning | Example |
|---|---|---|
| Editorial | Improves wording without changing meaning. | Clarifying ambiguous prose. |
| Clarification | Makes an existing rule more precise without intentionally changing its meaning. | Explaining an existing invariant. |
| Additive | Introduces an optional compatible capability. | Adding an optional evidence field. |
| Structural | Changes schema structure or relationships. | Reorganizing a schema while preserving semantics. |
| Semantic | Changes definitions, qualification, invariants, or relationship meaning. | Altering what constitutes meaningful action selection. |
| Breaking | Makes a previously valid conformant representation invalid or changes its interpretation. | Making a previously optional qualification condition mandatory. |
| Deprecation | Announces planned withdrawal of a construct or field. | Deprecating a legacy property. |
| Corrective | Fixes an inconsistency between declared semantics and actual repository artifacts. | Correcting a test manifest that misreports test coverage. |
| Multi-classification | A change may have multiple classifications. | A change to qualification may be both semantic AND breaking in classification. |

## Rule

Classification MUST reflect actual impact, not the size of the code or documentation diff.

## Versioning anchor

`versioning.change_classification`

## Dependents

- Versioning policy (this version)
- Change request requirements (this version)
- Release manifest (this version)

## Boundary assertion

Per CR-VAS-010, classification is determined by actual semantic impact, not by code or documentation diff size. Per SV-INV-001, every change MUST be classified. Per SV-INV-002, SemVer is a release convention and does not itself establish semantic compatibility.

## Next

For SemVer rules corresponding to the major/minor/patch buckets, see `versioning-policy.md`. For migration classes, see `deprecation-and-migration.md`.
