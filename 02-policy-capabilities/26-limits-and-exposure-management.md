---
id: limits-and-exposure-management
title: "Limits and Exposure Management"
capability_number: 26
category: "Policy Capability"
architectural_layer: "Policy Layer"
primary_record: "Limit definitions, approved facilities, utilization, availability, and exposure history"
criticality: "Critical"
status: draft
source: Core Banking Capability Reference Guide, CBCM Evolution Draft
---

# Limits and Exposure Management

> **Capability summary:** Defines, approves, monitors, and evaluates limits and exposure across customers, groups, accounts, cards, overdrafts, credit arrangements, collateralized contracts, and corporate facilities.

| Attribute | Value |
|---|---|
| Capability number | 26 |
| Category | Policy Capability |
| Architectural layer | Policy Layer |
| Primary record | Limit definitions, approved facilities, utilization, availability, and exposure history |
| Criticality | Critical |

## Purpose and Scope

- Define limit types, limit hierarchies, constraints, currencies, validity periods, and utilization rules.
- Approve, activate, suspend, expire, renew, and close customer, group, account, product, card, overdraft, and facility limits.
- Calculate utilization, available headroom, reserved exposure, pending exposure, and breach state.
- Provide limit decisions to origination, authorization, disbursement, drawdown, overdraft, and card workflows.

## Why It Matters

- Exposure often spans products and legal entities, while individual product domains see only part of the risk.
- Credit arrangements, overdrafts, cards, corporate facilities, and collateralized lending require consistent utilization and availability semantics.
- Breach, override, renewal, and expiry decisions must be auditable because they affect risk, customer commitments, and regulatory reporting.

## Domain Model

| **Aggregate or Core Concept** | **Responsibility** |
|---|---|
| **Limit Definition** | Reusable limit type, scope, hierarchy, currency, validation, and utilization method. |
| **Approved Limit** | Customer, group, product, account, card, or facility-specific limit with validity and approval state. |
| **Exposure Position** | Current, reserved, pending, utilized, available, and breached exposure snapshot. |
| **Limit Utilization** | Transactional record of drawdown, authorization, reservation, release, repayment, or adjustment. |
| **Limit Exception** | Breach, override, covenant exception, expiry exception, or manual adjustment requiring control. |

### Supporting Entities

- Credit Arrangement
- Facility
- Sublimit
- Exposure Group
- Utilization Reservation
- Limit Covenant
- Limit Review
- Override Approval
- Currency Conversion Rule

### Value Objects and Policy Concepts

- Limit Amount
- Utilization Amount
- Available Headroom
- Validity Period
- Exposure Scope
- Breach Severity
- Override Reason
- Reservation Expiry

## Lifecycle and Representative Workflows

> **Typical lifecycle:** Proposed -> Approved -> Active -> Utilized -> Breached or Reviewed -> Renewed, Suspended, Expired, or Closed

1. Limit setup: define scope, amount, currency, validity, sublimits, covenants, approval route, and eligible products.
2. Utilization decision: evaluate a proposed authorization, disbursement, overdraft, or drawdown against availability and constraints.
3. Monitoring and review: recalculate exposure, detect breaches or expiry, request remediation, renew, suspend, or close the limit.

## Relationships with Other Capabilities

| **Related capability** | **Interaction** |
|---|---|
| [**Customer Management**](../01-business-capabilities/01-customer-management.md) | Supplies party, group, household, organization, and related-party context. |
| [**Product Catalog**](../01-business-capabilities/04-product-catalog.md) | Defines product-level limit rules, eligibility, and utilization behavior. |
| [**Loan Management**](../01-business-capabilities/05-loan-management.md) | Consumes facility, drawdown, disbursement, refinance, and restructure limit decisions. |
| [**Savings Management**](../01-business-capabilities/06-savings-management.md) | Consumes overdraft, hold, account, and available-balance limit decisions. |
| [**Card Management**](../01-business-capabilities/25-card-management.md) | Consumes card authorization, velocity, and credit-limit decisions. |
| [**Collateral Management**](14-collateral-management.md) | Supplies pledged coverage, LTV, valuation, and secured exposure context. |
| [**Workflow & Approval**](../05-platform-capabilities/17-workflow-and-approval.md) | Coordinates limit approval, renewal, breach, override, and exception handling. |
| [**Accounting**](../03-financial-infrastructure/09-accounting.md) | May consume exposure state for provisions, commitments, and risk-related postings. |
| [**Reporting**](../04-information-capabilities/16-reporting.md) | Produces exposure, concentration, utilization, breach, and facility reports. |

## Distinctive Aspects and Peculiarities

- Approved limit, available balance, accounting balance, and committed exposure are distinct concepts.
- Limit utilization may be reserved before a financial transaction settles or posts.
- Parent limits and sublimits must reconcile so utilization cannot escape the approved hierarchy.
- Multi-currency exposure requires explicit conversion, valuation date, and rate-source rules.
- Overrides should be controlled business decisions, not silent bypasses of validation.

## Representative Commands and Business Events

### Commands

- Define Limit Type
- Propose Limit
- Approve Limit
- Activate Limit
- Reserve Exposure
- Release Exposure
- Record Utilization
- Recalculate Exposure
- Record Limit Breach
- Approve Limit Override
- Renew Limit
- Suspend Limit
- Close Limit

### Business Events

- Limit Type Defined
- Limit Proposed
- Limit Approved
- Limit Activated
- Exposure Reserved
- Exposure Released
- Utilization Recorded
- Exposure Recalculated
- Limit Breached
- Limit Override Approved
- Limit Renewed
- Limit Suspended
- Limit Closed

## Key Invariants and Design Guardrails

- A utilization decision is evaluated against the effective limit, scope, validity period, currency, and hierarchy at decision time.
- Total child-limit utilization cannot exceed the controlling parent limit unless an explicit override is approved.
- Released or expired reservations cannot continue to consume availability.
- Limit breaches, overrides, and manual adjustments preserve actor, reason, approval, and calculation evidence.
- Exposure snapshots are reproducible from limit definitions, utilization records, valuation rules, and source contract references.

> **Boundary:** Limits and Exposure Management owns limit definitions, approved exposure constraints, utilization, availability, and breach state. It does not own the customer contract, collateral asset, card instrument, payment, or accounting ledger.

