---
id: capability-collaboration-patterns
title: "Capability Collaboration Patterns"
category: Reference
status: reference
---

# Capability Collaboration Patterns

The following patterns summarize the most important forms of collaboration in the reference model. They are useful when designing APIs, events, service boundaries, or AI-generated specifications.

| **Pattern**                       | **Description**                                                                                                                                 |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Origination pattern**           | Customer + Product Catalog + Workflow create an approved contract in Loan, Savings, Deposit, or Share Management.                               |
| **Financial transaction pattern** | A contract domain validates the business action; Payment Processing moves value; Accounting creates journals; the General Ledger records them.  |
| **Policy evaluation pattern**     | Product or contract context is supplied to Interest, Fee, Delinquency, or Collateral policy capabilities; the owning domain applies the result. |
| **Asynchronous reaction pattern** | Committed Business Events drive Notification, Reporting projections, Integration delivery, Search indexing, and Audit correlation.              |
| **Periodic processing pattern**   | Batch Processing invokes domain commands using Business Date and Configuration while Administration controls execution.                         |
| **Approval pattern**              | Workflow & Approval authorizes a requested operation; Identity & Security verifies authority; the target domain revalidates and commits.        |
| **Operation contract map pattern** | Operation-level collaborations identify direction, interaction type, consumed input, produced output, and purpose without prescribing runtime topology. |
| **Correction pattern**            | The owning domain creates an explicit reversal or adjustment, Accounting posts compensating journals, and Audit preserves both histories.       |
