---
id: review-customer-management-operations-pilot
title: "Review Customer Management Operations Pilot"
category: "Research and Evaluation"
status: draft
capability: customer-management
source: Canonical Banking Capability Model (CBCM), Method Validation Review
---

# Customer Management Pilot Review Notes

## Method Works
Overall clear, structured and not too overengineered.

## Changes To Apply Before Reuse
1. [01-customer-management-operations.md (line 49)](C:/Users/MarcoSegato/OneDrive/Scalapay/projects/canonical-banking-capability-model/01-business-capabilities/01-customer-management-operations.md:49) still uses two-column operation tables:

```
| Specification element | Description |
```

The updated template uses:

```
| Specification element | Requirement | Description |
```

2. It still uses `Command` as the field label. The updated foundation uses:

```
Command / query / view name
```

This matters especially for [View Customer History (line 247)](C:/Users/MarcoSegato/OneDrive/Scalapay/projects/canonical-banking-capability-model/01-business-capabilities/01-customer-management-operations.md:247), which is a read-only governed view, not a command.

3. It does not yet have a `Refinement Selection` section after the feature map. Only add enough refinement-selection metadata to show how the mechanism works. This pilot does **not** need final inclusion/exclusion decisions for every possible Customer Management operation. 

4. The [Method Validation Notes (line 302)](C:/Users/MarcoSegato/OneDrive/Scalapay/projects/canonical-banking-capability-model/01-business-capabilities/01-customer-management-operations.md:302) are now stale. They say fields like `command`, `business events`, and `idempotency` are mandatory, but the updated foundation makes some of these **conditional**.

5. Make events more outcome-specific
   Some operations currently emit `Customer Profile Changed`, but the operation has a more specific business meaning. In this case have the operation emit both the more generic and the more precise events.
   
| Operation          | Current event            | Event to Add                 |
| ------------------ | ------------------------ | ---------------------------- |
| Add Identifier     | Customer Profile Changed | Customer Identifier Added    |
| Add Address        | Customer Profile Changed | Customer Address Added       |
| Submit Customer    | Customer Profile Changed | Customer Submitted           |
| Link Related Party | Customer Profile Changed | Customer Relationship Linked |
| Restrict Customer  | Customer Profile Changed | Customer Restricted          |

6. Add note to  "Update Profile" operation
> Split into more specific operations when changed attributes have distinct authorization, evidence, lifecycle, or regulatory implications.

7. Add some missing operations as P1
   - Update Address
   - Lift Customer Restriction

8. Use the retail payment account lens
Make these ops P0 :

- `Create Customer`
- `Update Profile`
- `Add Identifier`
- `Add Address`
- `Submit Customer`
- `Activate Customer`
- `Restrict Customer`
- `View Customer History`

Defer:

- Transfer Customer
- some relationship operations unless needed for signatories, guardians, or joint accounts.

9. evolve the collaboration section from a generic relationship table into an **operation-level contract map**.

Fields:

```
| Local operation | Collaborating capability | Direction | Interaction type | External trigger / consumed input | Produced output | Purpose |
```

Where:

- `Direction` = `Inbound`, `Outbound`, or `Bidirectional`
- `Interaction type` = `Command`, `Event`, `Query`, `Evidence reference`, `Workflow`, `Manual evidence`
- `External trigger / consumed input` = what this operation listens to, calls, checks, or requires
- `Produced output` = what this operation emits, returns, or makes available

add this rule:

> Cross-capability collaborations must identify direction, interaction style, consumed input, produced output, and business purpose. They describe required business contracts, not mandatory runtime topology.
