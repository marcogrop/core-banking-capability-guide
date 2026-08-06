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

## Business Operations

### Operation: `<Verb Phrase>`

| Specification element | Requirement | Description |
|---|---|---|
| Owning capability | Mandatory |  |
| Feature | Mandatory |  |
| Command / query / view | Conditional |  |
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
