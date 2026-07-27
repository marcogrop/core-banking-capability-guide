---
id: payment-processing
title: "Payment Processing"
capability_number: 10
category: "Financial Infrastructure"
architectural_layer: "Financial Infrastructure"
primary_record: "Payment instruction, execution state, settlement, and external trace"
criticality: "Critical"
status: reference
source: Core Banking Capability Reference Guide, Edition 1.0
---

# Payment Processing

> **Capability summary:** Executes and tracks movements of money across internal accounts, cash points, clearing networks, payment gateways, and external financial institutions. It manages payment state, authorization, execution, settlement, reversal, and external references.

| Attribute | Value |
|---|---|
| Capability number | 10 |
| Category | Financial Infrastructure |
| Architectural layer | Financial Infrastructure |
| Primary record | Payment instruction, execution state, settlement, and external trace |
| Criticality | Critical |

## Purpose and Scope

- Capture payment instructions and payment method details.
- Validate, authorize, execute, settle, reject, return, or reverse payments.
- Support cash, cheque, internal transfer, bank transfer, standing instruction, and gateway-based payments.
- Provide idempotency, correlation, status tracking, and reconciliation information.

## Why It Matters

- Payments are the operational mechanism by which financial obligations and customer instructions become movement of value.
- Separation from account domains allows consistent control across loans, savings, fees, and external rails.
- Explicit settlement state is essential because authorization, execution, clearing, and finality may occur at different times.

## Domain Model

![Payment Processing conceptual domain model](../assets/images/10-payment-processing-domain-model.png)

| **Aggregate or Core Concept** | **Responsibility**                                                    |
|-------------------------------|-----------------------------------------------------------------------|
| **Payment**                   | End-to-end payment lifecycle and current processing state.            |
| **Payment Instruction**       | Payer, payee, amount, currency, purpose, timing, and routing request. |
| **Transfer**                  | Linked debit and credit legs for an internal or external movement.    |
| **Standing Instruction**      | Recurring future payment instruction.                                 |
| **Settlement Record**         | External or internal evidence of clearing and final settlement.       |

### Supporting Entities

- Payment Method
- Payment Detail
- External Reference
- Cheque Detail
- Authorization
- Return
- Reversal
- Reconciliation Item

### Value Objects and Policy Concepts

- Amount
- Currency
- Value Date
- Payment Status
- Channel
- Idempotency Key
- Correlation ID
- Settlement Date

## Lifecycle and Representative Workflows

> **Typical lifecycle:** Initiated → Validated → Authorized → Executed → Clearing → Settled → Rejected → Returned → Reversed

1. Internal transfer: reserve or validate funds, debit source, credit destination, account for both legs, and complete atomically.
2. External payment: submit to rail, track acknowledgements and settlement, reconcile, and handle return or rejection.
3. Standing instruction: identify due instructions, validate current conditions, execute, and record next run.

## Relationships with Other Capabilities

| **Related capability**            | **Interaction**                                                          |
|-----------------------------------|--------------------------------------------------------------------------|
| [**Savings Management**](../01-business-capabilities/06-savings-management.md)            | Provides source and destination account state and balances.              |
| **Loan and Deposit Management**   | Receive repayments, disbursements, contributions, and maturity proceeds. |
| **Accounting and General Ledger** | Record cash, settlement, suspense, and transfer entries.                 |
| [**Integration**](../05-platform-capabilities/19-integration.md)                   | Connects payment gateways, switches, clearing systems, and banks.        |
| [**Batch Processing**](../05-platform-capabilities/20-batch-processing.md)              | Executes standing instructions, settlement cycles, and reconciliation.   |
| [**Notification**](../05-platform-capabilities/18-notification.md)                  | Communicates payment status and exceptions.                              |
| [**Audit**](../05-platform-capabilities/23-audit.md)                         | Maintains end-to-end transaction trace.                                  |

## Distinctive Aspects and Peculiarities

- Authorization, clearing, and settlement are distinct states and should not be represented by a single completed flag.
- Idempotency keys are mandatory for retried channel requests and asynchronous messages.
- Internal transfers should preserve atomic debit-credit semantics even when implemented through distributed components.
- Reversals, returns, refunds, and chargebacks have different meanings and accounting.
- External references are not always unique globally and require provider or rail scope.

## Representative Commands and Business Events

### Commands

- Initiate Payment
- Authorize Payment
- Execute Transfer
- Submit to Clearing
- Record Settlement
- Return Payment
- Reverse Payment
- Create Standing Instruction

### Business Events

- Payment Initiated
- Payment Authorized
- Payment Executed
- Payment Settled
- Payment Rejected
- Payment Returned
- Payment Reversed

## Key Invariants and Design Guardrails

- A payment amount and currency remain stable after authorization unless a controlled amendment is supported.
- Duplicate instructions with the same idempotency scope do not move funds twice.
- Source and destination legs reconcile to the payment amount and fees.
- Settled payments retain immutable external and accounting references.

> **Boundary:** Payment Processing owns payment lifecycle and movement coordination. It does not own customer account balances, product rules, or the General Ledger.
