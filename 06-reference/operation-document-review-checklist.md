---
id: operation-document-review-checklist
title: "Operation Document Review Checklist"
category: Reference
status: reference
---

# Operation Document Review Checklist

Use this checklist when reviewing a CBCM operation-decomposition document before reusing it as a pattern, marking it reviewed, or deriving implementation artefacts from it.

## 1. Document Role

- [ ] The document is clearly a companion to one capability chapter.
- [ ] The capability chapter remains the canonical summary and links to this operation document.
- [ ] The operation document does not duplicate large parts of the capability chapter.
- [ ] The document status is explicit: draft, reviewed, approved, deprecated, or superseded.

## 2. Feature Map

- [ ] Features are coherent functional areas within the capability.
- [ ] Features do not imply a mandatory service, team, product module, or UI structure.
- [ ] Each feature has clear primary concepts.
- [ ] Representative operations use specific business verb phrases.
- [ ] Vague operations such as `Manage`, `Process`, `Handle`, or broad `Update` are split or justified.

## 3. Refinement Selection

- [ ] The scenario or review lens is stated.
- [ ] P0 operations are required to prove the scenario or core boundary.
- [ ] P1 operations clarify important lifecycle, control, integration, or evidence gaps.
- [ ] P2 and P3 operations are deferred with a clear reason.
- [ ] The document does not attempt exhaustive decomposition unless that is explicitly intended.

## 4. Operation Specification Quality

For each fully drafted operation:

- [ ] Owning capability is correct.
- [ ] Feature assignment is correct.
- [ ] Purpose describes business outcome, not UI behavior.
- [ ] Actor and authorization are explicit.
- [ ] Inputs are sufficient and business-relevant.
- [ ] Preconditions are testable.
- [ ] Invariants protect ownership, lifecycle, and boundary rules.
- [ ] State transition is clear, or `None` for read-only views.
- [ ] Accounting consequence is present where relevant, otherwise `Not applicable`.
- [ ] Business events are outcome-specific where useful, otherwise `None`.
- [ ] Idempotency rule is present for state-changing operations, otherwise `Not applicable`.
- [ ] Error model includes meaningful business failures.
- [ ] Evidence required is explicit.
- [ ] Sandbox or test scenario is executable enough to validate behavior.

## 5. Read-Only Operations

- [ ] Read-only operations are included only when they are governed business views.
- [ ] Sensitive access, masking, and audit expectations are explicit.
- [ ] Read-only operations do not define state transitions.
- [ ] Read-only operations do not require idempotency.
- [ ] Business events are omitted unless access itself is business-significant.

## 6. Events and Evidence

- [ ] Events describe committed business facts, not implementation messages.
- [ ] Specific events are preferred when the business meaning is distinct.
- [ ] Broader summary events are used only when they add value.
- [ ] Audit evidence is captured without transferring domain ownership to Audit.
- [ ] Required evidence is enough to support review, dispute, compliance, and replay analysis.

## 7. Cross-Capability Collaboration

- [ ] Collaborations are expressed at operation level.
- [ ] Each collaboration identifies direction: inbound, outbound, or bidirectional.
- [ ] Each collaboration identifies interaction type: command, event, query, evidence reference, workflow, or manual evidence.
- [ ] Consumed input is explicit.
- [ ] Produced output is explicit.
- [ ] Purpose explains the business contract.
- [ ] The collaboration map does not prescribe mandatory runtime topology.

## 8. Boundaries

- [ ] The operation document preserves the owning capability's state boundary.
- [ ] Operations do not mutate records owned by other capabilities.
- [ ] Cross-capability checks are modeled as queries, events, commands, workflow, or evidence references.
- [ ] Product, accounting, identity, audit, and reporting responsibilities are not accidentally absorbed.

## 9. Evaluation Use

- [ ] Vendor or implementation evidence requirements are stated.
- [ ] Sandbox tests align to P0 operations.
- [ ] Known gap patterns are listed.
- [ ] Acceptance criteria are explicit.
- [ ] The document can support RFP, build/buy/partner, and architecture-review use cases.

## 10. Reuse Readiness

- [ ] The document follows the standard operation template.
- [ ] The level of detail is appropriate for the capability complexity.
- [ ] Naming conventions are consistent with the taxonomy.
- [ ] Links to capability, reference, and related artefacts work.
- [ ] Lessons that affect the method are promoted to reference guidance or TODO items.
