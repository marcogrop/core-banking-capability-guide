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

| Specification element | Requirement | Purpose |
|---|---|---|
| Operation name | Mandatory | Stable business verb phrase, such as Make Repayment or Record Authorization Hold. |
| Owning capability | Mandatory | Capability that owns the operation and its committed state change or governed view. |
| Feature | Mandatory | Functional grouping within the capability. |
| Command / query / view | Conditional | Imperative request for state-changing operations; query or view name for read-only governed views. |
| Purpose | Mandatory | Business outcome supported by the operation. |
| Actor and authorization | Mandatory | Who or what may request the operation and which authority is required. |
| Inputs | Mandatory | Required and optional request data, identifiers, amounts, dates, filters, references, and evidence. |
| Preconditions | Mandatory | Facts that must already be true before execution or view access. |
| Invariants | Mandatory | Rules that must remain true before and after execution, or during controlled access for read-only views. |
| State transition | Mandatory | Explicit change in lifecycle state, balances, reservations, evidence, or ownership record. Use None for read-only governed views. |
| Accounting consequence | Conditional | Journal intent, posting instruction, or financial event derived from the operation. Use Not applicable for non-financial operations. |
| Business events | Conditional | Committed facts published after successful state changes. Use None when no domain event is expected. |
| Idempotency rule | Conditional | How duplicate state-changing requests are recognized and safely handled. Use Not applicable for read-only governed views. |
| Error model | Mandatory | Stable business failure codes and recoverability expectations. |
| Evidence required | Mandatory | Documents, traces, approvals, calculations, logs, access records, or external references needed for audit and evaluation. |
| Sandbox or test scenario | Mandatory | Minimal scenario that proves the operation or governed view works as claimed. |

## Field Applicability Rules

| Rule | Explanation |
|---|---|
| Mandatory fields must be completed | A mandatory field should not be left blank in an operation specification. |
| Conditional fields require a value or clear exclusion | Conditional fields should be completed when relevant, or marked None / Not applicable when they do not apply. |
| Prefer explicit Not applicable | Use Not applicable rather than leaving a conditional field blank when the exclusion is intentional and obvious from the operation type. |
| Accounting consequence is conditional | It is mandatory for financial operations and normally Not applicable for non-financial operations. |
| Business events are conditional | State-changing operations normally emit business events; read-only governed views normally do not. |
| Idempotency is conditional | State-changing commands should define idempotency behavior; read-only governed views normally mark it Not applicable. |
| Implementation detail does not replace business specification | API endpoint names, table names, and screen names may be added later, but they do not replace operation purpose, state transition, invariants, and evidence. |

## Read-Only Governed Views

CBCM operation documents may include read-only governed views when the view exposes sensitive, regulated, operationally critical, or decision-relevant evidence. These views do not mutate domain state, but they still require explicit access control, masking, auditability, retention, and test coverage.

A read-only governed view uses the same operation specification template and is identified by:

| Field | Expected treatment |
|---|---|
| Operation name | Use a read verb such as View, Search, Retrieve, List, or Export. |
| Command / query / view | Use the query or view name rather than a state-changing command. |
| State transition | None. |
| Accounting consequence | Not applicable, unless the view itself triggers a regulated reporting or evidence workflow. |
| Business events | None, unless the domain treats access as a business-significant fact. Audit may still record access. |
| Idempotency rule | Not applicable. |
| Evidence required | Access log, actor, timestamp, filters, masking decision, source data lineage, and correlation identifier where relevant. |
| Sandbox or test scenario | Demonstrate authorized access, denied access, masking behavior, filtering, and evidence traceability. |

Example:

```text
Customer Management -> Customer History and Audit View -> View Customer History
```

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

Names should use business language rather than implementation language. A stable CBCM name should remain useful whether the operation is implemented through an API, workflow, batch job, vendor product, partner service, or manual process.

| Item | Convention | Example |
|---|---|---|
| Capability | Noun phrase naming a stable business responsibility. | Payment Processing |
| Feature | Noun phrase naming a coherent functional area inside a capability. | SEPA Credit Transfer |
| Business Operation | Verb phrase naming a business action or governed view. | Record Settlement |
| Command | Imperative verb phrase, usually the same as the operation for state-changing operations. | Record Settlement |
| Query / View | Read verb phrase for read-only governed views. | View Customer History |
| Business Event | Past-tense committed fact. | Payment Settled |

### Verb Guidance

| Verb pattern | Use when | Example |
|---|---|---|
| Create X | Creating a new owned domain record. | Create Customer |
| Update X | Amending existing state without changing lifecycle state. | Update Profile |
| Submit X | Moving something into review, approval, or processing. | Submit Customer |
| Activate X | Making something usable, effective, or eligible for downstream use. | Activate Customer |
| Suspend X | Temporarily restricting use while preserving the record. | Suspend Card |
| Close X | Ending a lifecycle while preserving history. | Close Customer |
| Record X | Capturing an external or already-occurred fact. | Record Settlement |
| Request X | Initiating a process whose outcome is not yet known. | Request Screening |
| Approve X | Approval itself is a meaningful domain fact. | Approve Limit |
| Reject X | Rejection itself is a meaningful domain fact. | Reject Onboarding |
| Reverse X | Creating an explicit compensating correction that preserves history. | Reverse Payment |
| View / Search / Retrieve / List / Export X | Read-only governed view. | View Customer History |

### Event Naming Rules

| Rule | Explanation | Example |
|---|---|---|
| Use past tense | Events describe committed facts after they occur. | Customer Activated |
| Do not name events as requests | A request is a command; the event is the committed outcome. | Use Screening Requested only after the screening request is actually recorded. |
| Prefer precise outcomes | Avoid broad event names when a more specific business fact exists. | Payment Settled instead of Payment Processed |
| Name meaningful failures selectively | Use failure/rejection events only when the negative outcome is itself a business fact. | Payment Rejected may be valid; Customer Update Failed is usually an error response. |
| Split materially different outcomes | If outcomes drive different downstream behavior, give them distinct events. | Payment Returned; Payment Recalled; Payment Reversed |
| Preserve domain ownership in event names | The event name should reflect the capability that owns the committed fact. | Customer Closed belongs to Customer Management. |

Examples:

| Operation | Event |
|---|---|
| Activate Customer | Customer Activated |
| Close Customer | Customer Closed |
| Record Settlement | Payment Settled |
| Request Screening | Screening Requested |
| Record Screening Result | Screening Result Recorded |

### Naming Anti-Patterns

| Avoid | Prefer | Reason |
|---|---|---|
| Manage Customer | Create Customer; Update Profile; Close Customer | Manage is too broad to test or implement as an atomic operation. |
| Process Payment | Validate Payment; Route Payment; Submit to Clearing | Process hides lifecycle stages and failure points. |
| Handle Error | Reject Payment; Return Payment; Record Repair | The business outcome should be explicit. |
| Do KYC | Request Screening; Record Screening Result; Approve Onboarding | The work spans multiple operations and capabilities. |
| Update Status | Activate Customer; Suspend Customer; Close Customer | Status changes should reveal business meaning. |
| Sync Data | Import Data; Export Data; Publish Event | Sync is implementation-oriented and ambiguous. |

## Reusable Template

Use the [Capability Feature Operation Template](capability-feature-operation-template.md) when decomposing a capability into features and operations.
