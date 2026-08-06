---
id: customer-management-operations
title: "Customer Management Operations"
capability: customer-management
category: "Business Capability Operations"
status: draft
source: Core Banking Capability Reference Guide, CBCM Method Validation
---

# Customer Management Operations

This companion document applies the CBCM three-level taxonomy to Customer Management.

```text
Capability -> Feature -> Business Operation
```

The purpose is method validation. The operation set is intentionally representative rather than exhaustive, and it should be reviewed before the same pattern is applied to more complex capabilities such as Payment Processing, Card Management, or Limits and Exposure Management.

## Capability Summary

| Field | Value |
|---|---|
| Capability | Customer Management |
| Capability number | 01 |
| Category | Business Capability |
| Architectural layer | Business Layer |
| Primary record | Customer master and relationship history |
| Owner / accountable domain | Customer master domain |
| Status | Draft method-validation pilot |

## Feature Map

| Feature | Purpose | Primary concepts | Representative operations |
|---|---|---|---|
| Customer Profile | Create and maintain accepted customer master data. | Customer, Customer Type, Legal Form, Preferred Language, Dynamic Data Record | Create Customer; Update Profile |
| Customer Lifecycle | Control customer submission, activation, closure, and lifecycle status. | Status, Activation Date, Closure Reason, Customer State Transition | Submit Customer; Activate Customer; Close Customer |
| Customer Identification | Maintain typed identifiers and external references after customer creation. | Customer Identifier, External Identifier, Identifier Type, Identifier Scope | Add Identifier |
| Contact and Address Management | Maintain customer addresses and contact points used by servicing, notification, and reporting. | Address, Contact Point, Consent, Preferred Channel | Add Address; Update Address |
| Customer Relationships | Maintain related-party roles and relationship history. | Customer Relationship, Related Party, Guarantor, Beneficiary, Signatory | Link Related Party |
| Customer Servicing Assignment | Assign institutional ownership and servicing responsibility. | Office Assignment, Staff Assignment, Transfer Reason | Transfer Customer |
| Customer Status and Restrictions | Apply operational restrictions that affect servicing eligibility without closing the customer. | Restriction, Reason Code, Effective Period, Review Date | Restrict Customer; Lift Customer Restriction |
| Customer History and Audit View | Expose customer timeline and change evidence for servicing, compliance, and investigation. | Customer Note, Change History, Audit Reference, Document Reference | View Customer History |

## Refinement Selection

This pilot uses the retail payment account lens to validate the selection method without making Customer Management exhaustive.

| Feature | Operation | Scenario relevance | Priority | Refinement status | Selection reason |
|---|---|---|---|---|---|
| Customer Profile | Create Customer | Required to create the customer master needed before opening or maintaining a retail payment account. | P0 | Drafted | Proves customer master creation and source/onboarding lineage. |
| Customer Profile | Update Profile | Required to maintain customer attributes used by servicing, eligibility, and evidence. | P0 | Drafted | Proves auditable profile change behavior. |
| Customer Identification | Add Identifier | Required when account opening depends on typed customer identifiers. | P0 | Drafted | Proves scoped identifiers, evidence, and uniqueness controls. |
| Contact and Address Management | Add Address | Required when account opening or servicing depends on address evidence and communication details. | P0 | Drafted | Proves address typing, evidence, and history. |
| Customer Lifecycle | Submit Customer | Required to move a draft customer into activation review. | P0 | Drafted | Proves lifecycle transition before activation. |
| Customer Lifecycle | Activate Customer | Required before product origination or account opening can reference the customer. | P0 | Drafted | Proves activation authority and eligibility evidence. |
| Customer Status and Restrictions | Restrict Customer | Required to show downstream account usage controls. | P0 | Drafted | Proves restriction evidence and downstream eligibility exposure. |
| Customer History and Audit View | View Customer History | Required to prove governed access to customer evidence and change history. | P0 | Drafted | Proves read-only governed view treatment. |
| Contact and Address Management | Update Address | Useful counterpart to Add Address for lifecycle completeness, but not fully specified in this pilot. | P1 | Candidate | Tests whether add-only operations need update/retire counterparts. |
| Customer Status and Restrictions | Lift Customer Restriction | Useful counterpart to Restrict Customer for temporary controls, review dates, and eligibility restoration. | P1 | Candidate | Tests lifecycle completion for operational restrictions. |
| Customer Servicing Assignment | Transfer Customer | Not required to prove the basic retail payment account scenario. | P2 | Deferred | Keep identified, but defer detailed refinement unless servicing transfer becomes part of the scenario. |
| Customer Relationships | Link Related Party | Scenario-dependent for joint holders, signatories, guardians, or authorized users. | P2 | Deferred | Keep identified, but refine when the account scenario requires related-party roles. |

## Business Operations

### Operation: Create Customer

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Profile |
| Command / query / view name | Create Customer |
| Purpose | Create an authoritative customer master record for an accepted person, organization, group, or center. |
| Actor and authorization | Back-office user, onboarding conversion process, migration process, or authorized API client with customer-create permission. |
| Inputs | Customer type, legal form, name, servicing office, preferred language, contact summary, source reference, optional onboarding case reference, and idempotency key. |
| Preconditions | Customer type is supported; mandatory minimum data for draft creation is present; servicing office exists; duplicate check has been performed or explicitly deferred according to policy. |
| Invariants | Internal customer identifier is unique; customer is not active by creation alone; source references are retained; customer type cannot be changed into an incompatible type without a controlled migration. |
| State transition | No customer record -> Customer created in Draft or Prospective state. |
| Accounting consequence | Not applicable. |
| Business events | Customer Created |
| Idempotency rule | A repeated create request with the same idempotency key and source reference returns the original customer reference without creating a duplicate. |
| Error model | Missing mandatory field; unsupported customer type; invalid office; duplicate candidate requires review; idempotency conflict. |
| Evidence required | Source system or onboarding reference, duplicate-check result, actor, timestamp, and initial data snapshot. |
| Sandbox or test scenario | Create an individual customer with minimum required fields and verify the returned customer identifier, initial status, and Customer Created event. |

### Operation: Update Profile

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Profile |
| Command / query / view name | Update Profile |
| Purpose | Apply an auditable change to customer master attributes such as name, legal form details, preferred language, configurable attributes, or profile notes. |
| Actor and authorization | Back-office user, authorized API client, or controlled data-correction process with profile-update permission. |
| Inputs | Customer identifier, changed fields, effective date where applicable, reason code, supporting evidence reference, and idempotency key. |
| Preconditions | Customer exists; customer is not closed unless closed-profile amendment is explicitly permitted; changed fields are valid for the customer type. |
| Invariants | Historical values remain auditable; protected fields require appropriate authority; profile changes do not silently change contracts, balances, or authentication credentials. |
| State transition | Customer profile version or change history is appended; lifecycle status may remain unchanged. |
| Accounting consequence | Not applicable. |
| Business events | Customer Profile Changed |
| Idempotency rule | A repeated update with the same idempotency key and identical change set is treated as the same profile change. |
| Error model | Customer not found; closed customer not amendable; invalid field for customer type; missing evidence for protected field; idempotency conflict. |
| Evidence required | Changed-field diff, reason, actor, timestamp, effective date, and supporting evidence reference where required. |
| Sandbox or test scenario | Update preferred language and a configurable profile attribute, then verify change history and Customer Profile Changed event. |

Granularity note: split this operation into more specific operations when changed attributes have distinct authorization, evidence, lifecycle, or regulatory implications.

### Operation: Add Identifier

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Identification |
| Command / query / view name | Add Identifier |
| Purpose | Add a typed customer identifier, such as tax identifier, national identifier, registry number, or external system identifier. |
| Actor and authorization | Back-office user, onboarding conversion process, migration process, or authorized API client with identifier-management permission. |
| Inputs | Customer identifier, identifier type, identifier value, issuing country or authority, validity period, evidence reference, and idempotency key. |
| Preconditions | Customer exists; identifier type is configured; identifier value passes format validation; uniqueness policy is evaluated for the identifier scope. |
| Invariants | Active identifiers are unique within their configured scope; identifier history is preserved; sensitive identifiers follow masking and access-control policy. |
| State transition | Identifier is added to customer identification history as active, pending verification, or historical according to policy. |
| Accounting consequence | Not applicable. |
| Business events | Customer Identifier Added; Customer Profile Changed |
| Idempotency rule | A repeated add request with the same idempotency key and identifier values returns the existing identifier record. |
| Error model | Customer not found; unsupported identifier type; invalid format; duplicate identifier; missing evidence; idempotency conflict. |
| Evidence required | Identifier evidence reference, validation outcome, actor, timestamp, and uniqueness-check result. |
| Sandbox or test scenario | Add a tax identifier and verify uniqueness enforcement by attempting to add the same active identifier to another customer. |

### Operation: Add Address

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Contact and Address Management |
| Command / query / view name | Add Address |
| Purpose | Add a structured address for servicing, correspondence, residency, tax, or legal purposes. |
| Actor and authorization | Back-office user, customer-servicing process, onboarding conversion process, or authorized API client with address-management permission. |
| Inputs | Customer identifier, address type, address lines, locality, country, postal code, effective period, verification status, evidence reference, and idempotency key. |
| Preconditions | Customer exists; address type is valid; mandatory address fields for country and address type are present. |
| Invariants | Address history is preserved; effective periods do not create ambiguous primary address state; privacy and masking rules apply to address access. |
| State transition | Address is added as active, pending verification, or historical according to effective period and verification status. |
| Accounting consequence | Not applicable. |
| Business events | Customer Address Added; Customer Profile Changed |
| Idempotency rule | A repeated add request with the same idempotency key and address payload returns the existing address record. |
| Error model | Customer not found; invalid address type; missing mandatory country-specific fields; overlapping primary address; idempotency conflict. |
| Evidence required | Address evidence reference, verification status, actor, timestamp, and effective period. |
| Sandbox or test scenario | Add a residential address and then add a correspondence address, verifying both are separately typed and visible in customer history. |

### Operation: Submit Customer

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Lifecycle |
| Command / query / view name | Submit Customer |
| Purpose | Mark a draft or prospective customer as ready for activation review or downstream processing. |
| Actor and authorization | Back-office user, onboarding conversion process, or authorized API client with customer-submit permission. |
| Inputs | Customer identifier, submission reason, completeness confirmation, supporting evidence references, and idempotency key. |
| Preconditions | Customer exists in Draft or Prospective state; minimum required data for submission is complete; mandatory identifiers and addresses are present or explicitly waived. |
| Invariants | Submission does not activate the customer; submission cannot bypass mandatory data validation; submitted snapshot is auditable. |
| State transition | Draft or Prospective -> Submitted. |
| Accounting consequence | Not applicable. |
| Business events | Customer Submitted; Customer Profile Changed |
| Idempotency rule | Repeated submission with the same idempotency key returns the same Submitted state and does not duplicate history entries. |
| Error model | Customer not found; invalid lifecycle state; mandatory data incomplete; missing waiver approval; idempotency conflict. |
| Evidence required | Completeness validation result, submitted data snapshot, actor, timestamp, and waiver references where applicable. |
| Sandbox or test scenario | Attempt to submit an incomplete customer and verify validation failure, then complete mandatory data and submit successfully. |

### Operation: Activate Customer

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Lifecycle |
| Command / query / view name | Activate Customer |
| Purpose | Make a submitted customer eligible for product origination, servicing, and contract reference. |
| Actor and authorization | Back-office user, approved workflow, onboarding conversion process, or authorized API client with customer-activate permission. |
| Inputs | Customer identifier, activation date, approval reference, onboarding or due-diligence reference where applicable, and idempotency key. |
| Preconditions | Customer exists in Submitted state; activation requirements for customer type are satisfied; servicing office is active; required onboarding/KYC acceptance exists where policy requires it. |
| Invariants | Every active customer has a unique internal identifier; activation date is recorded; activation does not create any financial contract by itself. |
| State transition | Submitted -> Active. |
| Accounting consequence | Not applicable. |
| Business events | Customer Activated |
| Idempotency rule | Repeated activation with the same idempotency key returns the existing Active state and original activation reference. |
| Error model | Customer not found; invalid lifecycle state; missing approval; KYC acceptance missing; inactive office; idempotency conflict. |
| Evidence required | Approval reference, activation date, actor, timestamp, and eligibility validation result. |
| Sandbox or test scenario | Activate a submitted customer and verify that product domains can reference the active customer but no account or loan is created automatically. |

### Operation: Close Customer

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Lifecycle |
| Command / query / view name | Close Customer |
| Purpose | Close a customer master record when the institution no longer maintains an active customer relationship. |
| Actor and authorization | Back-office user, approved workflow, migration/offboarding process, or authorized API client with customer-close permission. |
| Inputs | Customer identifier, closure reason, closure date, supporting evidence reference, unresolved-obligation check result, and idempotency key. |
| Preconditions | Customer exists; closure is permitted for current state; active contracts, unresolved obligations, active disputes, and legal holds have been checked according to policy. |
| Invariants | Closing a customer must not orphan active contracts or unresolved obligations; closure preserves history; closed customer cannot be used for new origination. |
| State transition | Active, Inactive, or Suspended -> Closed. |
| Accounting consequence | Not applicable. |
| Business events | Customer Closed |
| Idempotency rule | Repeated closure with the same idempotency key returns the existing Closed state and closure reference. |
| Error model | Customer not found; invalid lifecycle state; active contracts exist; unresolved obligations exist; legal hold prevents closure; idempotency conflict. |
| Evidence required | Closure reason, obligation checks, contract checks, legal-hold checks, actor, timestamp, and approval reference where required. |
| Sandbox or test scenario | Attempt to close a customer with an active account reference and verify failure, then close a customer without active obligations successfully. |

### Operation: Transfer Customer

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Servicing Assignment |
| Command / query / view name | Transfer Customer |
| Purpose | Move institutional servicing ownership of a customer to another office, branch, segment, or responsible staff assignment. |
| Actor and authorization | Back-office user, approved workflow, organizational maintenance process, or authorized API client with customer-transfer permission. |
| Inputs | Customer identifier, source office, target office, effective date, transfer reason, staff assignment where applicable, and idempotency key. |
| Preconditions | Customer exists; target office is active; transfer is allowed for customer state; required approvals are present; affected contracts can reference the new servicing context. |
| Invariants | Transfer preserves customer identifier, contracts, and history; effective-dated assignment history is retained; transfer does not move financial balances. |
| State transition | Office assignment changes from source to target as of effective date; customer lifecycle state may remain unchanged. |
| Accounting consequence | Not applicable. |
| Business events | Customer Transferred |
| Idempotency rule | Repeated transfer with the same idempotency key and target assignment returns the original transfer result. |
| Error model | Customer not found; inactive target office; invalid source assignment; transfer not allowed for state; missing approval; idempotency conflict. |
| Evidence required | Transfer reason, source and target assignment, approval reference, actor, timestamp, and effective date. |
| Sandbox or test scenario | Transfer an active customer to another office and verify assignment history and Customer Transferred event. |

### Operation: Link Related Party

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Relationships |
| Command / query / view name | Link Related Party |
| Purpose | Record a typed relationship between a customer and another party, such as guarantor, beneficiary, signatory, director, related organization, household member, or group member. |
| Actor and authorization | Back-office user, onboarding conversion process, servicing workflow, or authorized API client with relationship-management permission. |
| Inputs | Customer identifier, related party identifier or reference, relationship type, role, effective period, evidence reference, and idempotency key. |
| Preconditions | Customer exists; related party exists or can be referenced according to policy; relationship type is configured; relationship is valid for the customer and related-party types. |
| Invariants | Relationship history is preserved; relationship type determines semantics and cannot be treated as a generic note; active relationship periods do not conflict with exclusivity rules. |
| State transition | Relationship is added as active, pending verification, or historical according to effective period and verification status. |
| Accounting consequence | Not applicable. |
| Business events | Customer Relationship Linked; Customer Profile Changed |
| Idempotency rule | A repeated link request with the same idempotency key and relationship payload returns the existing relationship record. |
| Error model | Customer not found; related party not found; unsupported relationship type; invalid role; conflicting active relationship; idempotency conflict. |
| Evidence required | Relationship evidence, consent or authority where required, actor, timestamp, and effective period. |
| Sandbox or test scenario | Link a guarantor relationship to a customer and verify that the relationship is typed, effective-dated, and visible to downstream product eligibility checks. |

### Operation: Restrict Customer

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer Status and Restrictions |
| Command / query / view name | Restrict Customer |
| Purpose | Apply an operational restriction to a customer without closing the customer master record. |
| Actor and authorization | Back-office user, compliance workflow, risk workflow, or authorized API client with customer-restriction permission. |
| Inputs | Customer identifier, restriction type, reason code, effective period, review date, source reference, and idempotency key. |
| Preconditions | Customer exists; restriction type is configured; actor has authority for the restriction severity; conflicting restrictions are evaluated. |
| Invariants | Restrictions are explicit and auditable; restrictions do not silently alter balances or contracts; downstream capabilities must evaluate relevant active restrictions before allowed operations. |
| State transition | Customer receives an active restriction, or customer status changes to Suspended where the restriction policy requires it. |
| Accounting consequence | Not applicable. |
| Business events | Customer Restricted; Customer Profile Changed |
| Idempotency rule | A repeated restriction request with the same idempotency key and restriction payload returns the existing restriction record. |
| Error model | Customer not found; unsupported restriction type; insufficient authority; conflicting restriction; missing review date; idempotency conflict. |
| Evidence required | Reason code, source reference, actor, timestamp, effective period, and review date. |
| Sandbox or test scenario | Apply a debit-relevant customer restriction and verify that the customer profile exposes the active restriction to downstream eligibility checks. |

### Operation: View Customer History

| Specification element | Value |
|---|---|
| Owning capability | Customer Management |
| Feature | Customer History and Audit View |
| Command / query / view name | View Customer History |
| Purpose | Retrieve the customer timeline, profile changes, lifecycle transitions, relationship changes, and evidence references for servicing or investigation. |
| Actor and authorization | Back-office user, auditor, compliance user, support user, or authorized API client with customer-history permission. |
| Inputs | Customer identifier, date range, event type filters, field-level access context, and correlation identifier. |
| Preconditions | Customer exists; actor is authorized to view requested history and sensitive fields. |
| Invariants | History retrieval does not mutate customer state; sensitive fields are masked unless authority permits full visibility; audit access itself may be logged. |
| State transition | None. |
| Accounting consequence | Not applicable. |
| Business events | None required for the customer domain; Audit may record sensitive access. |
| Idempotency rule | Not applicable because the operation is read-only. |
| Error model | Customer not found; access denied; invalid date range; sensitive field restricted. |
| Evidence required | Access log, actor, timestamp, query filters, and masking decision where required. |
| Sandbox or test scenario | Retrieve history for a customer after create, address update, transfer, and restriction operations; verify chronological order and masking behavior. |

## Cross-Capability Collaborations

| Local operation | Collaborating capability | Direction | Interaction type | External trigger / consumed input | Produced output | Purpose |
|---|---|---|---|---|---|---|
| Create Customer | Customer Onboarding / KYC | Inbound | Command / Event / Evidence reference | Approved onboarding case, onboarding conversion request, or Onboarding Approved event. | Customer Created; customer reference; onboarding source reference retained. | Convert an accepted applicant into a customer master record. |
| Activate Customer | Customer Onboarding / KYC | Inbound | Query / Evidence reference | Due-diligence acceptance, screening status, remediation status, and activation eligibility evidence. | Customer Activated; activation eligibility evidence retained. | Ensure activation does not bypass onboarding or due-diligence controls. |
| Create Customer | Organization Management | Outbound | Query | Active servicing office, center, staff assignment, and organizational scope. | Customer Created with valid servicing assignment. | Ensure the customer master is created under a valid servicing context. |
| Transfer Customer | Organization Management | Outbound | Query | Active target office, branch, center, staff, and transfer eligibility. | Customer Transferred. | Ensure servicing assignment changes reference valid organization structures. |
| Activate Customer | Product Catalog | Outbound | Query | Product eligibility context where activation depends on customer type, segment, or restriction state. | Customer Activated or activation rejected. | Ensure activation produces a customer usable for eligible product origination. |
| Restrict Customer | Product Catalog / Product Domains | Outbound | Event / Query | Active customer restriction state and restriction semantics. | Customer Restricted; Customer Profile Changed. | Make restrictions visible to downstream eligibility and servicing checks. |
| Link Related Party | Loan / Savings / Deposit / Share / Card Management | Outbound | Event / Query | Typed relationship role, related-party reference, effective period, and evidence. | Customer Relationship Linked; Customer Profile Changed. | Allow product domains to evaluate holders, borrowers, guarantors, beneficiaries, signatories, and authorized users. |
| Add Address; Update Profile | Notification | Outbound | Event | Contact details, language, consent, preference, and address changes. | Customer Address Added or Customer Profile Changed. | Allow notification routing and consent views to update from customer master changes. |
| All state-changing operations | Audit | Outbound | Event / Evidence reference | Actor, authorization, timestamp, diff, reason, source reference, idempotency key, and correlation context. | Audit evidence reference or auditable event record. | Preserve operation evidence without transferring customer-state ownership to Audit. |
| View Customer History | Audit | Bidirectional | Query / Event / Evidence reference | Actor, access scope, filters, masking decision, and sensitive-access policy. | Customer history view; access log or sensitive-access audit event where required. | Prove governed read access and trace sensitive customer-history retrieval. |

## Implementation Notes

| Concern | Notes |
|---|---|
| Suggested service or module boundary | Customer Management can be a customer-master bounded context or service owning customer profile, lifecycle, identifiers, relationships, and servicing assignment. |
| API resources or endpoints | Likely resources include customers, identifiers, addresses, relationships, restrictions, assignments, and customer history. |
| Events to publish or consume | Publish Customer Created, Customer Activated, Customer Profile Changed, Customer Identifier Added, Customer Address Added, Customer Submitted, Customer Relationship Linked, Customer Restricted, Customer Transferred, and Customer Closed. Consume onboarding approval or customer-conversion events where Customer Onboarding / KYC is separate. |
| Data ownership and persistence | Own customer master and relationship history. Do not own onboarding case evidence, credentials, product contracts, financial transactions, or ledger entries. |
| Batch or periodic processing | Periodic tasks may identify stale draft customers, expired restrictions, or profile remediation needs, but state changes should still be expressed as domain operations. |
| Audit and observability | Every state-changing operation should preserve actor, reason, changed fields, source reference, idempotency key, and correlation identifier. |
| Migration considerations | Source customer IDs, legacy identifiers, relationship records, and historical status transitions should be mapped without reusing identifiers unsafely. |

## Evaluation Notes

| Concern | Notes |
|---|---|
| Native / configured / custom / partner / BPO distinction | Customer master ownership should be distinguished from externally provided onboarding, KYC, AML, CRM, or identity services. |
| Evidence required from vendor or implementation team | API docs, event catalogue, data model excerpt, duplicate-check behavior, audit trail sample, migration mapping, and sandbox evidence. |
| Sandbox test coverage | P0 coverage should include create, update profile, add identifier, add address, submit, activate, restrict, and retrieve history. P1 candidates should test update address and lift customer restriction when the scenario needs lifecycle-completing counterparts. |
| Known gap patterns | Customer and user identity collapsed; onboarding and customer master mixed; identifiers not scoped; relationship roles modeled as free text; closure allowed despite active contracts. |
| Acceptance criteria | Operations are atomic, auditable, idempotent where state-changing, and do not mutate product contracts, credentials, transactions, or accounting state. |

## Method Validation Notes

| Question                                           | Initial observation                                                                                                                                                                                 |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Is the three-level taxonomy understandable?        | Yes. Customer Management decomposes naturally into features and operations without forcing implementation topology.                                                                                 |
| Is the operation template too heavy?               | Slightly heavy for simple CRUD-like operations, but useful because it exposes authorization, evidence, idempotency, and boundary rules.                                                             |
| Which fields should be mandatory?                  | Owning capability, feature, purpose, actor and authorization, inputs, preconditions, invariants, state transition, error model, evidence, and test scenario remain mandatory. |
| Which fields are conditional?                      | Command / query / view name, accounting consequence, business events, and idempotency rule are conditional and should be completed or explicitly marked None / Not applicable. |
| Does the doc belong beside the capability chapter? | For the pilot, yes. It keeps the decomposition close to the capability while avoiding clutter in the main chapter.                                                                                  |
| Can this scale to Payment Processing?              | Yes, but Payment Processing will need stricter feature boundaries and possibly fewer operations per document to remain readable.                                                                    |
| Does the collaboration table work?                 | Yes, if expressed as an operation-level contract map with direction, interaction type, consumed input, produced output, and purpose.                                                               |
| Should read-only operations be included?           | Include only where they represent an important governed business view, such as View Customer History. Use State transition = None, Business events = None unless access is business-significant, and Idempotency rule = Not applicable. |

