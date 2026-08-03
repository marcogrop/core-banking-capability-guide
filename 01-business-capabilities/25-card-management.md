---
id: card-management
title: "Card Management"
capability_number: 25
category: "Business Capability"
architectural_layer: "Business Layer"
primary_record: "Card instrument, cardholder relationship, authorization controls, and card servicing history"
criticality: "High"
status: draft
source: Core Banking Capability Reference Guide, CBCM Evolution Draft
---

# Card Management

> **Capability summary:** Manages the lifecycle, controls, and servicing of card instruments linked to deposit, savings, prepaid, credit, or loan-backed accounts. It owns cardholder status, issuance, tokenization context, authorization controls, card limits, dispute context, and processor or network servicing evidence.

| Attribute | Value |
|---|---|
| Capability number | 25 |
| Category | Business Capability |
| Architectural layer | Business Layer |
| Primary record | Card instrument, cardholder relationship, authorization controls, and card servicing history |
| Criticality | High |

## Purpose and Scope

- Issue, activate, suspend, block, replace, renew, and close card instruments.
- Manage cardholder, authorized-user, token, physical-card, virtual-card, and card-account relationships.
- Maintain authorization controls, card limits, status restrictions, and card servicing cases.
- Coordinate card-originated holds, clearing outcomes, chargebacks, disputes, and processor traces.

## Why It Matters

- Cards are customer-facing access instruments with their own lifecycle and operational risk profile.
- Authorization, clearing, settlement, dispute, and account posting events often occur at different times.
- Separating card servicing from generic payments preserves clear ownership of cardholder controls and issuer evidence.

## Domain Model

| **Aggregate or Core Concept** | **Responsibility** |
|---|---|
| **Card Account Link** | Relationship between a card instrument and the funding, prepaid, overdraft, credit-card, or loan-backed account it can access. |
| **Card Instrument** | Physical, virtual, tokenized, debit, prepaid, charge, or credit card access instrument. |
| **Cardholder Profile** | Cardholder, authorized user, embossing, delivery, consent, and servicing preferences. |
| **Card Authorization Control** | Usage rules, velocity controls, channel restrictions, merchant restrictions, spend limits, and blocking state. |
| **Card Servicing Case** | Dispute, chargeback, replacement, fraud claim, status exception, or customer service process. |

### Supporting Entities

- Card Token
- Physical Card
- Virtual Card
- Authorization Hold
- Clearing Advice
- Chargeback Case
- Card Limit
- Processor Reference
- Card Fee Association

### Value Objects and Policy Concepts

- PAN Token
- Card Status
- Expiry Date
- Merchant Category
- Authorization Result
- Card Network
- Processor Trace
- Velocity Window

## Lifecycle and Representative Workflows

> **Typical lifecycle:** Requested -> Approved -> Issued -> Activated -> Active -> Suspended or Blocked -> Replaced or Renewed -> Closed

1. Card issuance: request a card, validate eligibility, create the card relationship, submit processor issuance, activate, and notify the cardholder.
2. Authorization and clearing: apply card controls, place holds when required, receive clearing details, release or convert holds, and pass financial movement to Payment Processing.
3. Servicing and disputes: block or replace a card, manage dispute or chargeback evidence, and preserve processor and customer communication history.

## Relationships with Other Capabilities

| **Related capability** | **Interaction** |
|---|---|
| [**Customer Management**](01-customer-management.md) | Identifies cardholders, authorized users, contact points, and party relationships. |
| [**Customer Onboarding / KYC**](27-customer-onboarding-and-kyc.md) | Provides onboarding status and due-diligence conditions required before card issuance. |
| [**Product Catalog**](04-product-catalog.md) | Defines card products, card fees, eligibility, controls, and linked account rules. |
| [**Savings Management**](06-savings-management.md) | Provides linked deposit or transactional account state and available funds. |
| [**Loan Management**](05-loan-management.md) | Provides credit-card, revolving-credit, or loan-backed contract context where applicable. |
| [**Limits and Exposure Management**](../02-policy-capabilities/26-limits-and-exposure-management.md) | Supplies card authorization limits, credit utilization, and breach decisions. |
| [**Fee Engine**](../02-policy-capabilities/12-fee-engine.md) | Calculates card fees, transaction charges, and waivers. |
| [**Payment Processing**](../03-financial-infrastructure/10-payment-processing.md) | Executes card-originated financial movements, settlement, returns, and reversals. |
| [**Integration**](../05-platform-capabilities/19-integration.md) | Connects processors, token services, wallets, fraud services, and card networks. |
| [**Audit**](../05-platform-capabilities/23-audit.md) | Preserves authorization, clearing, dispute, status, and processor evidence. |

## Distinctive Aspects and Peculiarities

- A card is an access instrument, not the account balance itself.
- Physical cards, virtual cards, wallet tokens, and account links can have different lifecycles.
- Authorization holds are not final settlement and must expire, clear, reverse, or convert to posted transactions.
- Card blocks, fraud restrictions, and lost or stolen status must take effect without mutating historical authorization evidence.
- Debit, prepaid, charge, and credit cards share some servicing concepts but differ in contract, exposure, and accounting behavior.

## Representative Commands and Business Events

### Commands

- Request Card
- Approve Card
- Issue Card
- Activate Card
- Suspend Card
- Block Card
- Replace Card
- Renew Card
- Tokenize Card
- Update Card Controls
- Record Authorization Hold
- Release Authorization Hold
- Record Clearing Advice
- Open Card Dispute
- Close Card

### Business Events

- Card Requested
- Card Approved
- Card Issued
- Card Activated
- Card Suspended
- Card Blocked
- Card Replaced
- Card Renewed
- Card Tokenized
- Card Controls Changed
- Authorization Hold Recorded
- Authorization Hold Released
- Clearing Advice Received
- Card Dispute Opened
- Card Closed

## Key Invariants and Design Guardrails

- A card cannot authorize access to an account or credit line unless the card, cardholder, product, and account link are eligible at authorization time.
- A card status change preserves the reason, actor, time, and processor or network trace where available.
- Authorization holds reconcile to clearing, expiry, reversal, or release outcomes.
- Card replacement and renewal preserve continuity between old and new instruments without reusing sensitive identifiers unsafely.
- Card servicing history remains visible after closure.

> **Boundary:** Card Management owns card instruments, cardholder servicing state, card controls, and card evidence. It does not own deposit balances, credit-contract balances, payment settlement, processor infrastructure, or the General Ledger.

