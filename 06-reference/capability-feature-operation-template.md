---
id: capability-feature-operation-template
title: "Capability Feature Operation Template"
category: Reference
status: template
---

# Capability Feature Operation Template

Use this template when decomposing a CBCM capability into implementable features and business operations.

## Capability Summary

| Field | Value |
|---|---|
| Capability |  |
| Capability number |  |
| Category |  |
| Architectural layer |  |
| Primary record |  |
| Owner / accountable domain |  |
| Status | Draft |

## Feature Map

| Feature | Purpose | Primary concepts | Representative operations |
|---|---|---|---|
|  |  |  |  |

## Refinement Selection

Use this section to record which features and operations are selected for the current scenario, implementation increment, or model review. Detailed selection rules are defined in the [Three-Level Capability Taxonomy](third-level-business-operations.md).

| Feature | Operation | Scenario relevance | Priority | Refinement status | Selection reason |
|---|---|---|---|---|---|
|  |  |  | P0 / P1 / P2 / P3 | Identified / Candidate / Selected / Drafted / Reviewed / Approved / Deferred |  |

## Business Operations

### Operation: `<Verb Phrase>`

Use a business verb phrase such as `Activate Customer`, `Record Settlement`, or `View Customer History`. Avoid vague names such as `Manage`, `Process`, `Handle`, or `Update Status` unless they are decomposed into more precise business operations.

| Specification element | Requirement | Description |
|---|---|---|
| Owning capability | Mandatory |  |
| Feature | Mandatory |  |
| Command / query / view name | Conditional |  |
| Purpose | Mandatory |  |
| Actor and authorization | Mandatory |  |
| Inputs | Mandatory |  |
| Preconditions | Mandatory |  |
| Invariants | Mandatory |  |
| State transition | Mandatory |  |
| Accounting consequence | Conditional |  |
| Business events | Conditional |  |
| Idempotency rule | Conditional |  |
| Error model | Mandatory |  |
| Evidence required | Mandatory |  |
| Sandbox or test scenario | Mandatory |  |

Use `None` for `State transition` when the operation is a read-only governed view. Use `Not applicable` for conditional fields that are intentionally excluded, such as accounting consequence for non-financial operations or idempotency for read-only views.

## Cross-Capability Collaborations

| Source operation | Collaborating capability | Collaboration type | Expected contract or evidence |
|---|---|---|---|
|  |  | Command / Event / Query / Workflow / Batch / Manual Evidence |  |

## Implementation Notes

| Concern | Notes |
|---|---|
| Suggested service or module boundary |  |
| API resources or endpoints |  |
| Events to publish or consume |  |
| Data ownership and persistence |  |
| Batch or periodic processing |  |
| Audit and observability |  |
| Migration considerations |  |

## Evaluation Notes

| Concern | Notes |
|---|---|
| Native / configured / custom / partner / BPO distinction |  |
| Evidence required from vendor or implementation team |  |
| Sandbox test coverage |  |
| Known gap patterns |  |
| Acceptance criteria |  |
