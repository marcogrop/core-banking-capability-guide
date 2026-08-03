---
id: product-catalog
title: "Product Catalog"
capability_number: 4
category: "Business Capability"
architectural_layer: "Business Layer"
primary_record: "Versioned financial product definitions, simulation evidence, and product lifecycle decisions"
criticality: "High"
status: reference
source: Core Banking Capability Reference Guide, Edition 1.0
---

# Product Catalog

> **Capability summary:** Defines, validates, simulates, approves, and retires reusable financial product definitions. A product specifies commercial terms, eligibility, interest, repayment, charge, accounting, servicing behavior, limits, and operational configuration from which customer contracts are created.

| Attribute | Value |
|---|---|
| Capability number | 04 |
| Category | Business Capability |
| Architectural layer | Business Layer |
| Primary record | Versioned financial product definitions, simulation evidence, and product lifecycle decisions |
| Criticality | High |

## Purpose and Scope

- Define loan, savings, current-account, fixed-deposit, recurring-deposit, share, card, overdraft, credit-line, Islamic-finance, bundled, and specialized product variants.
- Associate interest, fees, accounting mappings, currencies, limits, schedules, controls, channels, eligibility, servicing rules, and operational constraints.
- Manage product compatibility, product mix, pricing packages, effective dates, lifecycle states, migration rules, mass changes, and retirement.
- Simulate product behavior before activation, including schedule, balance, pricing, accounting, limit, card, and edge-case outcomes.
- Provide controlled defaults and constraints for contract origination and servicing.

## Why It Matters

- Product configuration is the primary mechanism for launching differentiated offerings without rewriting core code.
- It separates reusable policy from individual customer contract state.
- Versioned products make historical calculations and contractual terms reproducible.
- Product simulation and controlled versioning reduce the risk of deploying inconsistent, non-compliant, or financially incorrect product behavior.

## Domain Model

![Product Catalog conceptual domain model](../assets/images/04-product-catalog-domain-model.png)

| **Aggregate or Core Concept** | **Responsibility** |
|---|---|
| **Loan Product** | Template for lending terms, schedules, allocation, charges, limits, and accounting. |
| **Savings Product** | Template for transactional deposit accounts, interest, overdraft, controls, and fees. |
| **Deposit Product** | Template for fixed or recurring contractual deposits, contribution behavior, profit or interest, and maturity rules. |
| **Share Product** | Template for member equity, issuance, redemption, and dividend constraints. |
| **Card Product** | Template for debit, prepaid, charge, credit-card, virtual-card, card-control, and linked-account behavior. |
| **Product Version** | Approved or draft set of product terms, lifecycle state, activation window, and change lineage. |
| **Product Simulation** | Test run or scenario that validates expected product behavior before activation or migration. |
| **Pricing Package** | Bundle, segment, campaign, relationship, or arrangement-level commercial terms. |
| **Charge Definition** | Reusable fee or penalty definition. |
| **Floating Rate** | Effective-dated reference rate and spread model. |

### Supporting Entities

- Accounting Mapping
- Eligibility Rule
- Repayment Rule
- Interest Rule
- Charge Association
- Product Mix Rule
- Currency Rule
- Limit Rule
- Card Control Rule
- Product Migration Rule
- Product Test Scenario
- Bundle Rule
- Islamic Finance Rule

### Value Objects and Policy Concepts

- Effective Period
- Calculation Method
- Frequency
- Rounding Rule
- Minimum and Maximum
- Grace Period
- Accounting Profile
- Simulation Result
- Product State
- Product Family
- Arrangement Template

## Lifecycle and Representative Workflows

> **Typical lifecycle:** Draft -> Simulated -> Reviewed -> Approved -> Active -> Superseded or Suspended for New Sales -> Migrated or Retired

1. Product design: compose terms, policies, charges, accounting, limits, eligibility, controls, and servicing behavior into a draft version.
2. Product simulation: run representative scenarios for balances, schedules, fees, interest, accounting, limits, card behavior, and exceptional cases.
3. Product approval: validate internal consistency and authorize the version for use.
4. Contract origination: copy or reference the effective product terms into a new customer contract or access instrument.
5. Product change: create a successor version, simulate impacts, approve, activate, and control migration or mass-change behavior.

## Relationships with Other Capabilities

| **Related capability** | **Interaction** |
|---|---|
| [**Interest Engine**](../02-policy-capabilities/11-interest-engine.md) | Supplies calculation methods, rate plans, day-count, and posting conventions. |
| [**Fee Engine**](../02-policy-capabilities/12-fee-engine.md) | Supplies charge definitions, triggers, schedules, and waiver rules. |
| [**Limits and Exposure Management**](../02-policy-capabilities/26-limits-and-exposure-management.md) | Supplies limit types, facility rules, overdraft rules, utilization behavior, and product-level exposure constraints. |
| [**Accounting**](../03-financial-infrastructure/09-accounting.md) | Consumes product-to-ledger mappings and posting profiles. |
| **Loan / Savings / Deposit / Share / Card Management** | Instantiate contracts or access instruments from effective product versions. |
| [**Customer Onboarding / KYC**](27-customer-onboarding-and-kyc.md) | Uses product eligibility and due-diligence requirements during onboarding. |
| [**Configuration**](../05-platform-capabilities/21-configuration.md) | Provides institution-wide defaults, feature flags, and code tables. |
| [**Reporting**](../04-information-capabilities/16-reporting.md) | Uses product hierarchy and versions as primary analytical dimensions. |

## Distinctive Aspects and Peculiarities

- Products are templates, not accounts: they do not own balances or transaction history.
- Existing contracts should not silently inherit changed product terms unless the contract explicitly references dynamic policy.
- Effective-dated versions are preferable to in-place mutation of active products.
- Cross-field validation is essential; individually valid parameters may form an impossible schedule, authorization rule, or accounting setup.
- Product mix rules can prevent incompatible combinations for a customer, group, relationship, or arrangement.
- Simulation is evidence, not authority: live contract behavior must still be governed by approved product versions and domain invariants.
- Product migration and mass change require explicit eligibility, customer impact, accounting, communication, and rollback semantics.
- Product bundles and pricing packages should not obscure the underlying authoritative product terms applied to each contract.

## Representative Commands and Business Events

### Commands

- Create Product Draft
- Simulate Product
- Validate Product Version
- Add Charge
- Configure Accounting
- Configure Product Limits
- Configure Product Bundle
- Define Product Migration
- Define Eligibility
- Approve Product Version
- Activate Product
- Supersede Product Version
- Migrate Product Contracts
- Retire Product

### Business Events

- Product Draft Created
- Product Simulated
- Product Version Validated
- Product Version Approved
- Product Activated
- Product Version Superseded
- Product Contracts Migrated
- Product Terms Changed
- Product Retired

## Key Invariants and Design Guardrails

- Every originated contract identifies the exact product version or contractual term set used.
- An active product passes configuration, currency, schedule, limit, control, and accounting validation.
- Retiring a product prevents new origination but does not invalidate existing contracts.
- Product changes are effective-dated and auditable.
- Simulation, approval, activation, and migration decisions retain evidence of tested scenarios and expected financial effects.
- Product bundles preserve traceability to each underlying product, price, fee, interest, and accounting rule.

> **Boundary:** Product Catalog owns reusable definitions, product versions, product simulation evidence, and product lifecycle decisions. It must not own customer-specific balances, schedules, transactions, authorization outcomes, or contract lifecycle decisions.

