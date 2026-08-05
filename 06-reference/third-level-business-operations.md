---
id: three-level-capability-taxonomy
title: "Three-Level Capability Taxonomy"
category: Reference
status: reference
---

# Three-Level Capability Taxonomy

CBCM becomes implementable when every capability can be decomposed into features and business operations.

```text
Capability -> Feature -> Business Operation
```

This structure connects the conceptual model to executable design. It allows teams to move from a stable business boundary to epics, service responsibilities, APIs, commands, events, test cases, implementation work packages, and vendor evidence.

## Taxonomy Levels

| Level | Definition | Design use | Evaluation use |
|---|---|---|---|
| Capability | Stable business responsibility with its own language, rules, state, and authoritative record. | Defines ownership boundary, domain model, service/module responsibility, and governance area. | Determines whether a vendor, product, or solution covers a canonical banking responsibility. |
| Feature | Coherent functional area within a capability. | Groups related operations into product increments, API resources, workflow areas, or backlog epics. | Helps compare coverage at a level more precise than broad capability names. |
| Business Operation | Atomic business action, decision, calculation, or state transition that can be specified, authorized, implemented, tested, evidenced, and audited. | Becomes the unit for commands, events, state transitions, invariants, acceptance criteria, and automated tests. | Becomes the unit for evidence, sandbox validation, gap analysis, and fit assessment. |

## Level Rules

| Rule | Explanation |
|---|---|
| Capabilities own facts | Each authoritative business fact should have one capability that can change it. |
| Features group operations | A feature is not a vague label; it should contain operations that naturally belong together. |
| Operations are testable | A business operation is too broad if it cannot be tested through a clear scenario and expected outcome. |
| Operations are not UI tasks | A screen action may invoke an operation, but the operation is defined by business effect, not by interface gesture. |
| Operations preserve boundaries | If one operation changes facts owned by multiple capabilities, it should be decomposed or modeled as collaboration between operations. |
| Implementation topology can vary | A capability or feature may map to one service, many services, a module, a purchased product, a partner service, or manual operations. |

## Operation Specification Elements

Each Business Operation should be specified with enough detail to support implementation, testing, governance, and evaluation.

| Specification element | Purpose |
|---|---|
| Operation name | Stable business verb phrase, such as Make Repayment or Record Authorization Hold. |
| Owning capability | Capability that owns the operation and its committed state change. |
| Feature | Functional grouping within the capability. |
| Command | Imperative request to perform the operation. |
| Purpose | Business outcome supported by the operation. |
| Actor and authorization | Who or what may request the operation and which authority is required. |
| Inputs | Required and optional request data, identifiers, amounts, dates, references, and evidence. |
| Preconditions | Facts that must already be true before execution. |
| Invariants | Rules that must remain true before and after execution. |
| State transition | Explicit change in lifecycle state, balances, reservations, evidence, or ownership record. |
| Accounting consequence | Journal intent, posting instruction, or financial event derived from the operation, where relevant. |
| Business events | Committed facts published after successful execution. |
| Idempotency rule | How duplicate requests are recognized and safely handled. |
| Error model | Stable business failure codes and recoverability expectations. |
| Evidence required | Documents, traces, approvals, calculations, logs, or external references needed for audit and evaluation. |
| Sandbox or test scenario | Minimal scenario that proves the operation works as claimed. |

## Implementation Guidance

Use the taxonomy to derive platform implementation work:

| Design concern | Taxonomy use |
|---|---|
| Bounded context or service design | Start from capabilities and primary records. |
| API design | Expose commands, queries, and resources around business operations and owned state. |
| Event design | Emit business events for committed operation outcomes. |
| Data ownership | Assign authoritative write ownership at capability level. |
| Workflow design | Use Workflow & Approval to coordinate requested operations without stealing domain ownership. |
| Test strategy | Build acceptance and regression scenarios around operation preconditions, state transitions, events, and failure outcomes. |
| Migration planning | Map source-system features and records to CBCM capabilities, features, and operations. |
| Build-vs-buy decisions | Compare whether a capability, feature, or operation is custom-built, configured, purchased, partnered, BPO-delivered, or unsupported. |

## Evaluation Guidance

Vendor or solution evaluation should map claims to the taxonomy:

```text
Vendor claim -> Evidence -> CBCM capability -> Feature -> Business Operation -> Fit / gap
```

This avoids comparing vendor module names directly. A vendor may claim to support "cards", but CBCM comparison should ask which operations are supported: issue card, activate card, place authorization hold, process clearing advice, manage disputes, and so on.

## Example Decompositions

| Capability | Feature | Business operations |
|---|---|---|
| Card Management | Card Issuance | Request Card; Approve Card; Issue Card; Activate Card; Replace Card; Renew Card; Close Card |
| Card Management | Card Authorization | Update Card Controls; Record Authorization Hold; Release Authorization Hold; Record Clearing Advice |
| Payment Processing | SEPA Credit Transfer | Initiate Payment; Validate Payment; Route Payment; Submit to Clearing; Record Settlement; Reconcile Settlement; Recall Payment; Return Payment; Repair Payment |
| Customer Onboarding / KYC | Screening | Request Screening; Record Screening Result; Request Remediation; Approve Onboarding; Reject Onboarding |
| Product Catalog | Product Lifecycle | Create Product Draft; Simulate Product; Validate Product Version; Approve Product Version; Activate Product; Supersede Product Version; Migrate Product Contracts |
| Limits and Exposure Management | Limit Utilization | Reserve Exposure; Release Exposure; Record Utilization; Recalculate Exposure; Record Limit Breach; Approve Limit Override |
| Loan Management | Loan Repayment | Make Repayment; Reverse Transaction; Allocate Payment; Recalculate Schedule; Generate Accounting Consequences |
| Payment Processing | Direct Debit | Register Direct Debit Mandate; Initiate Collection; Record Rejection; Record Return; Reconcile Settlement |

## Naming Conventions

| Item | Convention | Example |
|---|---|---|
| Capability | Noun phrase expressing responsibility | Payment Processing |
| Feature | Noun phrase expressing functional area | SEPA Credit Transfer |
| Business Operation | Verb phrase expressing business action | Record Settlement |
| Command | Imperative verb phrase | Record Settlement |
| Business Event | Past-tense committed fact | Payment Settled |

## Reusable Template

Use the [Capability Feature Operation Template](capability-feature-operation-template.md) when decomposing a capability into features and operations.

