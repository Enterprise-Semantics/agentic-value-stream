# Versioning Policy

**Topic:** Semantic Versioning Policy (MAJOR.MINOR.PATCH)
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 through CR-VAS-009

## Purpose

Per CR-VAS-010 §4, adopt semantic versioning for the published AVS specification using MAJOR.MINOR.PATCH, with semantic impact as the determinant rather than diff size.

## Core principle

SemVer is the release convention. It does not itself establish semantic compatibility. Compatibility MUST be assessed and evidenced against the five dimensions (Definition, Instance, Schema, Conformance, Mapping).

## Scope

All releases of the published AVS specification. Optional artifact-level versioning is permitted when a schema improvement should not imply a specification change.

## MAJOR

Increment when a change is incompatible with the previous semantic contract. Examples: changing the necessary conditions for AVS qualification; changing the meaning of a canonical relationship; removing a mandatory property; redefining an invariant; changing controlled vocabulary in a way that alters interpretation; changing a conformance rule such that previously conformant instances become non-conformant. A major release MUST include migration guidance and an explicit impact assessment.

## MINOR

Increment when compatible functionality or clarification is added without changing the meaning of existing conformant representations. Examples: adding an optional property; introducing a new optional architecture pattern; adding a compatible mapping type; adding a non-breaking evidence field; adding supplementary examples. A minor release MUST document new capabilities and any implementation actions recommended.

## PATCH

Increment for corrections that do not intentionally alter the semantic contract. Examples: correcting typographical errors; fixing broken documentation links; correcting a schema description; repairing a test fixture that incorrectly represents an already-defined rule. A patch release MUST NOT be used to disguise a semantic or compatibility-breaking change.

## Specification vs artifact version

The repository SHOULD distinguish the version of the overall AVS specification from the version of individual artifacts. An artifact MUST NOT declare compatibility with a specification version if it changes or contradicts that specification's normative semantics.

## Versioning anchor

`versioning.versioning_policy + versioning.version_distinction`

## Dependents

- Change classification (this version)
- Release manifest (this version)
- Compatibility dimensions (this version)

## Boundary assertion

Per CR-VAS-010, SemVer is the release convention and does not itself establish semantic compatibility. Per SV-INV-002, compatibility MUST be assessed and evidenced independently. Per SV-INV-003, a change that alters qualification criteria MUST NOT be released as a patch.

## Next

For deprecation, migration, and migration classes, see `deprecation-and-migration.md`. For invariants governing versioning, see `versioning-invariants.md`.
