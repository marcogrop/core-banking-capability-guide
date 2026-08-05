---
id: cbcm-charter
title: "CBCM Charter"
category: Foundation
status: draft
---

# CBCM Charter

The Canonical Banking Capability Model (CBCM) is a vendor-neutral reference model for defining, implementing, governing, and evaluating modern banking platforms.

Its primary purpose is to help teams design and build a coherent banking platform with clear business ownership, explicit state boundaries, auditable operations, stable contracts, and disciplined cross-capability collaboration. Vendor or product evaluation is a supported use case, but it is not the model's only or primary purpose.

## What CBCM Is

CBCM is a capability and operating model for banking platforms. It identifies the stable business responsibilities that a platform must account for, regardless of whether those responsibilities are implemented through custom services, purchased products, third-party providers, legacy systems, manual operations, or a combination of these.

The model defines:

| CBCM element | Purpose |
|---|---|
| Capability | Stable business responsibility and ownership boundary. |
| Primary record | Authoritative state or evidence owned by the capability. |
| Lifecycle | Meaningful business states and transitions. |
| Domain concepts | Aggregates, entities, value objects, policies, and evidence concepts. |
| Commands | Requests to perform business-changing operations. |
| Business events | Committed facts published after successful state changes. |
| Invariants | Rules that must remain true regardless of implementation technology. |
| Relationships | Collaboration patterns with other capabilities. |

## What CBCM Is Not

CBCM is not a vendor module map, implementation topology, product catalogue, API specification, database schema, or delivery methodology.

It should not be interpreted as:

| Not this | Reason |
|---|---|
| Vendor marketing taxonomy | Vendor names and modules can inform research, but do not define canonical boundaries. |
| Deployment architecture | A capability may be implemented as one service, many services, a module, a workflow, or a managed external service. |
| Physical data model | Domain models describe conceptual ownership, not table design. |
| Legal or regulatory advice | The model can identify control points and evidence needs, but does not replace qualified advice. |
| Complete product requirements catalogue | CBCM provides the structure from which requirements can be derived and evaluated. |

## Primary Uses

### Custom Platform Definition

CBCM can guide the definition of a custom banking platform by identifying which capabilities are needed, what each capability owns, which invariants must hold, and how capabilities collaborate without sharing uncontrolled state.

Use CBCM to answer:

- Which business responsibilities must the platform support?
- Which capability owns each authoritative fact?
- Which operations change state?
- Which events should be emitted after committed changes?
- Which cross-capability dependencies are acceptable?
- Which boundaries should not be blurred during implementation?

### Implementation Planning

CBCM can be translated into implementation work packages. Capability chapters can inform epics, bounded contexts, service boundaries, APIs, event contracts, test scenarios, data migration plans, and operational controls.

The model is especially useful when turning high-level banking intent into executable design:

```text
Capability -> Feature -> Business Operation -> Command / Event / Test / Evidence
```

### Architecture Governance

CBCM provides a shared reference for architecture review. Proposed solutions can be assessed for boundary clarity, data ownership, lifecycle completeness, auditability, accounting consequences, idempotency, event design, and operational control.

The model should help reviewers distinguish between:

- a feature that is genuinely owned by the platform,
- a feature delegated to a provider,
- a feature requiring custom extension,
- a feature handled manually or through operations,
- and a feature that is not supported.

### Vendor and Solution Evaluation

CBCM can be used to compare vendors, products, and solution options against the same canonical structure. Evaluation should focus on business capability coverage, semantic completeness, operation maturity, integration quality, evidence, and architectural fit.

It should not score vendors merely by matching their product names to CBCM capability names. A vendor claim should be mapped to CBCM through evidence:

```text
Vendor claim -> Evidence -> CBCM capability / feature / operation -> Gap or fit assessment
```

## Design Principles

- Business ownership is more important than system ownership.
- Every authoritative business fact should have one clear owner.
- Commands request change; business events state committed facts.
- Business operations should be specific enough to test, evidence, authorize, and implement.
- Product configuration does not replace explicit domain concepts.
- Reversal and correction preserve history.
- Integration contracts should preserve capability boundaries.
- Vendor language is evidence, not authority.
- Implementation topology may vary without changing the capability model.

## Success Criteria

CBCM is successful when it helps a team:

- define a banking platform without starting from vendor modules,
- decompose capabilities into implementable business operations,
- design clean service, API, event, and data ownership boundaries,
- identify gaps before build or procurement decisions,
- compare build, buy, partner, and BPO options consistently,
- govern change as the platform evolves,
- and preserve a shared banking language across product, engineering, operations, risk, compliance, and finance.

