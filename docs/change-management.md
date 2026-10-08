# Change Management (CR-VAS-007)

## Material Change

A central requirement of CR-VAS-007 is the concept of a Material
AVS Change. A change is material when it could alter:

- whether the implementation remains semantically Agentic;
- delegated authority;
- action space;
- risk exposure;
- stakeholder outcome;
- Value Stream progression;
- intervention requirements;
- regulatory obligations;
- operational boundary.

Examples of material changes:

- change agent model
- change authority threshold
- change decision policy
- expand action space
- move from advisory to delegated execution
- add a new Value Stream stage
- remove human approval
- expand geography
- change customer population
- change regulatory context

These SHOULD trigger revalidation.

## Change Classification

Changes are classified by materiality and required revalidation.

### Class A ; Non-Material

No meaningful effect on semantic qualification, authority, risk,
or value realization. No full requalification required.

### Class B ; Controlled

Potential operational or measurement impact. Requires targeted
review.

### Class C ; Material

Potential impact on semantic qualification, authority, risk or
outcome. Requires formal revalidation.

### Class D ; Critical

Potential significant safety, regulatory, financial, customer or
enterprise impact. Requires governance approval before
implementation.

## Change Decision Model

```
Change Proposed
   -> Materiality Assessment
     -> No: Controlled Change
     -> Yes: Revalidation
       -> Approval
         -> Implementation
           -> Evidence
             -> Monitoring
```

## Cardinal Author Rule

All content authored by Emmanuel A. Otchere (cardinal author rule,
2026-10-08). Promotion to Established reserved for CR-VAS-007
acceptance review (governance frame ES-ADR-057).
