---
id: recommended-third-level-business-operations
title: "Recommended Third-Level Business Operations"
category: Reference
status: reference
---

# Recommended Third-Level Business Operations

The two-level taxonomy of Capability → Feature becomes executable when extended with a third level of Business Operations. Each operation should be specified with inputs, authorization, preconditions, invariants, state transitions, financial effects, emitted events, idempotency, and failure outcomes.

> **Example:** Loan Management → Loan Repayment → Make Repayment / Reverse Repayment / Allocate Payment / Recalculate Schedule / Generate Accounting Consequences

| **Specification element**  | **Purpose**                                                                         |
|----------------------------|-------------------------------------------------------------------------------------|
| **Command**                | Imperative request to change state, such as Make Repayment.                         |
| **Preconditions**          | Facts that must already be true, such as an active loan and valid transaction date. |
| **Invariants**             | Rules that remain true before and after execution.                                  |
| **State transition**       | Explicit change in aggregate state or balances.                                     |
| **Business event**         | Committed fact published after success.                                             |
| **Accounting consequence** | Journal intent or financial event derived from the operation.                       |
| **Idempotency rule**       | How duplicate requests are recognized and safely handled.                           |
| **Error model**            | Stable business failure codes and recoverability expectations.                      |
