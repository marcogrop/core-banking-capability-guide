---
id: cbcm-gap-assessment
title: "CBCM Gap Assessment"
category: Research
status: draft
---

# CBCM Gap Assessment

This assessment translates the first vendor research pass into candidate modifications for the Canonical Banking Capability Model (CBCM). It is intentionally a proposal layer. Capability chapters should be changed only after the modification set is selected.

## Decision Principles

| Principle | Meaning |
|---|---|
| Canonical before commercial | A capability belongs in CBCM when it represents a stable banking responsibility, not merely a vendor module. |
| Business ownership before technology | Prefer capability boundaries based on authority over business facts, states, contracts, and controls. |
| Evidence before expansion | Add or split a capability only when multiple sources or strong domain reasoning support it. |
| Specialization without fragmentation | Product families such as Islamic finance or cards may need explicit treatment without duplicating the entire model. |
| Evaluation dimensions stay separate | Deployment model, cloud posture, ecosystem, and vendor viability should support vendor assessment but not become CBCM business capabilities. |

## Prioritized Modification Candidates

| Priority | Candidate modification | Proposed treatment | Rationale | Initial source signals |
|---:|---|---|---|---|
| 1 | Card Management / Card Servicing | Add new Business Capability | Cards have issuer lifecycle, tokenization, authorization holds, clearing, limits, fraud controls, account linkage, and credit-card contract behavior that generic Payment Processing does not fully own. | Mambu, Tuum, Temenos, Thought Machine |
| 2 | Limits and Exposure Management | Add new Policy Capability or Risk Capability | Credit arrangements, umbrella limits, overdraft limits, consolidated exposure, facility availability, and cross-account constraints recur across vendors. | Mambu, Tuum, Temenos |
| 3 | Product Design, Simulation, and Lifecycle | Expand or split Product Catalog | Current Product Catalog captures versioned product definitions, but vendors expose product-as-code, product builder tooling, simulation, arrangement construction, product versions, pricing packages, and mass change. | Thought Machine, Temenos, Mambu, Tuum |
| 4 | Customer Onboarding / KYC | Add new Business Capability or expand Customer Management | Customer master data is not the same as onboarding, identity verification, due diligence, screening handoff, and onboarding state. | Temenos, Fineract, Mambu |
| 5 | Financial Crime Interface | Add adjacent Platform/Policy Capability or explicit boundary | AML, fraud, screening, sanctions, and halted-payment workflows are often implemented by specialist systems, but CBCM should define the boundary and integration obligations. | Temenos, Tuum |
| 6 | Corporate Credit Facilities | Add new Business Capability or expand Loan Management | Bilateral loans, syndicated lending, participations, umbrella facilities, drawdowns, commercial finance, and exposure control exceed retail loan lifecycle semantics. | Temenos, Tuum |
| 7 | Payments Orchestration and Scheme Connectivity | Expand Payment Processing | Payment Processing currently covers payment instruction and settlement, but should better distinguish routing, scheme validation, direct debit, bulk payments, exception handling, settlement provider integration, and liquidity dependencies. | Tuum, Temenos, Mambu, Thought Machine |
| 8 | Treasury, Liquidity, and Nostro Interface | Add Financial Infrastructure candidate or expand Payment Processing/General Ledger | Nostro balances, liquidity management, treasury positions, FX, and settlement funding appear in vendor material but are not clearly owned in CBCM. | Tuum, Temenos |
| 9 | Islamic Finance Support | Add specialization model | Islamic deposits, profit-sharing, Tawarruq, Shari'ah segregation, and Islamic windows recur. This may be best modeled as product-family specialization across Product, Deposit, Loan, Accounting, and Compliance. | Mambu, Tuum, Temenos, Thought Machine |
| 10 | Data Migration / Back-Book Migration | Add Platform Capability candidate | Migration APIs, historical data ingestion, back-book replication, account switching, and product migration are first-class concerns in core replacement. | Thought Machine, Temenos |
| 11 | Regionalization / Localization | Add evaluation dimension; consider Platform Capability later | Regional packs, local regulatory support, calendars, tax, statement formats, payment schemes, and market conventions matter strongly in product evaluation, but may be a dimension before a capability. | Temenos, Mambu, Tuum |
| 12 | Event Streaming and Data Products | Expand Integration, Reporting, and Platform Services | Streaming APIs, operational data stores, analytics, and event schemas need clearer canonical expectations around event publication, governed read models, lineage, and delivery guarantees. | Mambu, Thought Machine, Temenos, Fineract |

## Recommended First CBCM Evolution Wave

The first wave should focus on high-signal changes that improve vendor comparison without over-expanding the model.

| Wave item                         | Action                                                   | Notes                                                                                                                                                                                               |
| --------------------------------- | -------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Card Management / Card Servicing  | Add capability chapter                                   | Strongest missing business capability. Distinct from payment execution because it owns card instrument lifecycle and issuer controls.                                                               |
| Limits and Exposure Management    | Add capability chapter                                   | Strong cross-product policy/risk capability. Should own limits, utilization, availability, and breach events.                                                                                       |
| Product Design and Lifecycle      | Split or substantially expand Product Catalog            | Preserve Product Catalog as the authoritative product definition owner, but add simulation, product version lifecycle, arrangement construction, pricing packages, and product migration semantics. |
| Customer Onboarding / KYC         | Add capability chapter or split from Customer Management | Keep Customer Management as party/customer master; give onboarding its own lifecycle and evidence boundary.                                                                                         |
| Payments Orchestration refinement | Expand existing Payment Processing chapter               | Clarify scheme connectivity, routing, direct debits, exception handling, settlement integration, liquidity dependency, and screening hooks.                                                         |

## Candidate Capability Definitions

### Card Management / Card Servicing

Owns the lifecycle of card instruments and card-linked credit or debit access, including issuance, activation, cardholder status, tokenization, authorization controls, clearing outcomes, card limits, card fees, card holds, fraud-control hooks, and processor/network integration evidence.

Likely relationships:

| Related capability | Relationship |
|---|---|
| Customer Management | Identifies cardholder and authorized users. |
| Savings Management / Account Management | Supplies linked funding account and available balance. |
| Loan Management / Revolving Credit | Supplies credit-card contract or credit line where applicable. |
| Payment Processing | Executes card-originated financial movement and settlement. |
| Limits and Exposure Management | Provides authorization limits and credit exposure constraints. |
| Fee Engine | Calculates card fees and transaction charges. |
| Integration | Connects card processors, token services, fraud services, and networks. |
| Audit | Preserves authorization, clearing, dispute, and status evidence. |

### Limits and Exposure Management

Owns the definition, approval, utilization, availability, monitoring, and breach state of limits across customers, groups, facilities, products, accounts, overdrafts, cards, collateralized lending, and corporate entities.

Likely relationships:

| Related capability | Relationship |
|---|---|
| Customer Management | Supplies party, group, and relationship context. |
| Loan Management | Consumes limits during approval, disbursement, refinance, and restructure. |
| Savings Management / Account Management | Consumes overdraft and account limits. |
| Card Management | Consumes card authorization and credit limits. |
| Collateral Management | Supplies secured coverage and collateral utilization. |
| Workflow & Approval | Controls limit approval, override, extension, and exception handling. |
| Reporting | Publishes exposure snapshots and concentration views. |

### Product Design and Lifecycle

Extends Product Catalog from static product definition into the managed lifecycle of product construction, simulation, versioning, activation, mass change, retirement, product migration, and pricing/package composition.

Likely relationships:

| Related capability | Relationship |
|---|---|
| Configuration | Supplies effective-dated parameters and environment-specific configuration. |
| Fee Engine / Interest Engine | Supplies reusable pricing and calculation components. |
| Loan/Savings/Deposit/Card Management | Instantiate and enforce product behavior in live contracts. |
| Accounting | Validates product accounting treatment before activation. |
| Reporting | Supports product performance analysis and simulation results. |
| Workflow & Approval | Approves product versions and controlled changes. |

### Customer Onboarding / KYC

Owns the onboarding journey from prospect capture through due diligence, identity evidence collection, screening handoff, risk classification, acceptance, rejection, and conversion into an active customer record.

Likely relationships:

| Related capability | Relationship |
|---|---|
| Customer Management | Receives accepted customer master and relationship facts. |
| Identity & Security | Handles user credentials and authentication, not customer due diligence. |
| Financial Crime Interface | Performs or coordinates screening, sanctions, AML, fraud, and adverse-media checks. |
| Workflow & Approval | Coordinates exceptions and enhanced due diligence approvals. |
| Audit | Preserves onboarding evidence and decisions. |

## Defer or Treat as Evaluation Dimensions

| Topic | Recommended treatment | Reason |
|---|---|---|
| Cloud-native deployment | Evaluation dimension | Important for vendor selection, but not a business capability. |
| SaaS, bank-hosted, on-prem deployment | Evaluation dimension | Product fit and operating model concern. |
| Ecosystem / partner marketplace | Evaluation dimension | Relevant to extensibility and implementation, not canonical banking ownership. |
| Vendor regional coverage | Evaluation dimension first | Regionalization affects capabilities, but vendor country count is not itself a capability. |
| AI or agentic banking | Defer | Current public signals are too broad; wait for concrete business operation evidence. |
| Wealth management | Defer or future domain expansion | Important for universal banking, but may sit outside the initial core banking scope. |

## Suggested Next Work Package

1. Approve or revise the first-wave modification list.
2. Create canonical chapter templates for Card Management, Limits and Exposure Management, and Customer Onboarding / KYC.
3. Decide whether Product Catalog should be expanded in place or split into Product Design and Product Catalog.
4. Revise Payment Processing to include orchestration, scheme connectivity, exceptions, settlement integration, and liquidity hooks.
5. Update the capability index, relationship index, commands/events index, glossary, and architecture diagram after the new boundaries are stable.

