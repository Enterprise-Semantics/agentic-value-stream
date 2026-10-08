# Versioning

**Topic:** Versioning Policy and Evolution Mechanism
**Authored by:** Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
**CR:** CR-VAS-010
**Status:** Active
**Date:** 2026-10-08
**Depends on:** CR-VAS-002 (Qualification), CR-VAS-003 (Participation), CR-VAS-004 (Evidence), CR-VAS-005 (Measurement), CR-VAS-006 (Maturity), CR-VAS-007 (Governance), CR-VAS-008 (Architecture), CR-VAS-009 (Interoperability).

## Purpose

Establish a controlled semantic evolution mechanism for Agentic Value Stream (AVS) per CR-VAS-010. Defines how the repository evolves without creating contradictory definitions, silently changing qualification criteria, invalidating existing instances without notice, or fragmenting downstream implementations.

## Core principle

The AVS semantic contract MUST evolve deliberately, transparently, and traceably. A repository version change is not merely a software release event. It MAY change the meaning of the concept, the qualification of instances, or the interpretation of downstream architecture. Consequently, AVS MUST distinguish semantic change from implementation change and documentation change.

## Scope

CR-VAS-010 governs changes to: canonical definitions; semantic qualification rules; Agentic Participation relationships; characteristics and invariants; schemas and controlled vocabularies; evidence and conformance requirements; measurement definitions; maturity and governance models; architecture patterns; interoperability contracts; WSF and OpenDEA mappings; examples, documentation, and conformance fixtures.

## Applies to

AVS semantic contract, all artifacts in this repository, and downstream implementations claiming AVS conformance.

## Versioning anchor

`versioning.versioning_policy`

## Dependents

- Release process (this version)
- Migration records (this version)
- Compatibility assessment (this version)

## Boundary assertion

Per CR-VAS-010, the AVS semantic contract MUST evolve deliberately, transparently, and traceably. Semantic compatibility MUST be assessed across five dimensions (Definition, Instance, Schema, Conformance, Mapping). Migration transformations MUST be explicit. The compatibility report MUST distinguish schema-compatible changes from semantically breaking changes.

## Next

For change classifications, see `change-classification.md`. For SemVer rules, see `versioning-policy.md`. For deprecation and migration, see `deprecation-and-migration.md`.
