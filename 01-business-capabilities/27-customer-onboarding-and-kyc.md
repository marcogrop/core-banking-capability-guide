---
id: customer-onboarding-and-kyc
title: "Customer Onboarding / KYC"
capability_number: 27
category: "Business Capability"
architectural_layer: "Business Layer"
primary_record: "Onboarding case, due-diligence evidence, screening decisions, and conversion outcome"
criticality: "High"
status: draft
source: Core Banking Capability Reference Guide, CBCM Evolution Draft
---

# Customer Onboarding / KYC

> **Capability summary:** Manages the journey from prospect capture through identity evidence collection, due diligence, screening handoff, risk classification, approval, rejection, and conversion into an active customer record.

| Attribute | Value |
|---|---|
| Capability number | 27 |
| Category | Business Capability |
| Architectural layer | Business Layer |
| Primary record | Onboarding case, due-diligence evidence, screening decisions, and conversion outcome |
| Criticality | High |

## Purpose and Scope

- Capture prospect, applicant, beneficial-owner, signatory, and related-party onboarding information.
- Collect and validate identity, address, tax, ownership, consent, and eligibility evidence.
- Coordinate KYC, KYB, sanctions, PEP, adverse-media, fraud, and AML screening handoffs.
- Manage onboarding decisions, enhanced due diligence, expiry, remediation, rejection, and conversion into a customer master.

## Why It Matters

- Customer onboarding determines whether the institution may establish a banking relationship.
- KYC evidence, screening outcomes, and decision rationale must be traceable independently from ordinary customer profile maintenance.
- Separating onboarding from Customer Management prevents incomplete or rejected prospects from polluting the authoritative customer master.

## Domain Model

| **Aggregate or Core Concept** | **Responsibility** |
|---|---|
| **Onboarding Case** | End-to-end onboarding lifecycle, requested products, applicants, evidence status, and decision state. |
| **Applicant Party** | Natural person, organization, beneficial owner, signatory, controller, or related party under review. |
| **Due-Diligence Evidence** | Documents, declarations, attestations, verification results, consent, and expiry state. |
| **Screening Referral** | Request and response context for sanctions, PEP, adverse media, fraud, AML, or other checks. |
| **Onboarding Decision** | Acceptance, rejection, remediation, enhanced review, risk rating, and conversion outcome. |

### Supporting Entities

- Beneficial Owner
- Authorized Signatory
- Identity Document
- Address Evidence
- Tax Declaration
- Consent Record
- Risk Assessment
- Remediation Task
- Evidence Expiry

### Value Objects and Policy Concepts

- Applicant Type
- Verification Status
- Risk Rating
- Screening Result
- Evidence Type
- Onboarding Channel
- Decision Reason
- Review Deadline

## Lifecycle and Representative Workflows

> **Typical lifecycle:** Started -> Evidence Pending -> Screening -> Enhanced Review -> Approved or Rejected -> Converted or Expired

1. Retail onboarding: capture applicant details, collect evidence, perform checks, resolve exceptions, approve, and create the customer master.
2. Business onboarding: capture organization, ownership, signatories, controlling persons, tax information, and authority evidence before approval.
3. Remediation: detect expired or insufficient evidence, request additional information, suspend completion, and record the final outcome.

## Relationships with Other Capabilities

| **Related capability** | **Interaction** |
|---|---|
| [**Customer Management**](01-customer-management.md) | Receives accepted customer, party relationship, contact, and classification facts. |
| [**Organization Management**](02-organization-management.md) | Supplies servicing office, channel, staff, and assignment context. |
| [**Product Catalog**](04-product-catalog.md) | Supplies requested product eligibility and onboarding requirements. |
| [**Identity & Security**](../05-platform-capabilities/03-identity-and-security.md) | May create or link digital identities after the customer or applicant is eligible. |
| [**Workflow & Approval**](../05-platform-capabilities/17-workflow-and-approval.md) | Coordinates enhanced due diligence, exceptions, and approval decisions. |
| [**Integration**](../05-platform-capabilities/19-integration.md) | Connects identity verification, document verification, registry, tax, sanctions, AML, and fraud services. |
| [**Audit**](../05-platform-capabilities/23-audit.md) | Preserves evidence, screening, decisions, and customer-conversion lineage. |
| [**Reporting**](../04-information-capabilities/16-reporting.md) | Produces onboarding funnel, rejection, remediation, and compliance operational reports. |

## Distinctive Aspects and Peculiarities

- A prospect, applicant, party, digital user, and active customer are related but distinct concepts.
- KYC/KYB status may expire or require remediation after customer activation.
- Rejected or abandoned onboarding cases should preserve evidence and decision history subject to retention policy.
- Screening outcomes often require human review, explainability, and evidence lineage.
- Beneficial ownership and signatory authority are part of onboarding even when they are later referenced by Customer Management.

## Representative Commands and Business Events

### Commands

- Start Onboarding
- Add Applicant Party
- Submit Evidence
- Request Screening
- Record Screening Result
- Request Remediation
- Approve Onboarding
- Reject Onboarding
- Convert to Customer
- Expire Onboarding Case

### Business Events

- Onboarding Started
- Applicant Party Added
- Evidence Submitted
- Screening Requested
- Screening Result Recorded
- Remediation Requested
- Onboarding Approved
- Onboarding Rejected
- Customer Converted
- Onboarding Case Expired

## Key Invariants and Design Guardrails

- A customer is not activated from onboarding unless mandatory evidence, screening, and approval conditions are satisfied or explicitly waived.
- Screening results retain source, timestamp, scope, and decision rationale.
- Evidence expiry and remediation requirements remain visible after customer conversion.
- Rejected onboarding cases cannot be silently converted without a new or reopened decision process.
- Customer Management receives only the authoritative customer facts, not every transient onboarding artifact.

> **Boundary:** Customer Onboarding / KYC owns onboarding cases, due-diligence evidence, screening referrals, and conversion decisions. Customer Management owns the accepted customer master and relationship history after conversion.

