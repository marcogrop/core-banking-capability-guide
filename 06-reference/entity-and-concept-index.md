---
id: entity-index
title: Entity and Concept Index
category: Reference
status: reference
---

# Entity and Concept Index

The entries below identify conceptual aggregates, supporting entities, value objects, and policy concepts. They are not physical database-table definitions.

| Entity or concept | Type | Capability | Description |
|---|---|---|---|
| Access Policy | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Account Application | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Account Charge | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Account Dimension | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Account Type | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Accounting Mapping | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Accounting Period Check | Supporting entity | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Accounting Profile | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Accounting Rule | Aggregate or core concept | [Accounting](../03-financial-infrastructure/09-accounting.md) | Mapping from a business event and context to debit and credit journal lines. |
| Accrual Period | Aggregate or core concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Time window, balance basis, and calculated interest result. |
| Accrual Record | Aggregate or core concept | [Accounting](../03-financial-infrastructure/09-accounting.md) | Time-based recognition item awaiting or supporting posting. |
| Action | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Activation Date | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Actor | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Actor Type | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Address | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Amount | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Amount | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Annual Rate | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| API Client | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| API Contract | Aggregate or core concept | [Integration](../05-platform-capabilities/19-integration.md) | Versioned synchronous interface and policy. |
| Appraisal Document | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Approval Record | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Approval Reference | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Arrears Snapshot | Aggregate or core concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Past-due components and days-past-due result for an as-of date. |
| As-of Date | Value object or policy concept | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Assignee Scope | Value object or policy concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Assignment Rule | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Attachment Reference | Supporting entity | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Audit Record | Aggregate or core concept | [Audit](../05-platform-capabilities/23-audit.md) | Immutable statement of an action, event, or decision. |
| Authentication Factor | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Authentication Method | Value object or policy concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Authorization | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Available Balance | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Backup Policy | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Balance Basis | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Balance Hold or Lien | Aggregate or core concept | [Savings Management](../01-business-capabilities/06-savings-management.md) | Reservation that reduces available funds without necessarily changing ledger balance. |
| Balance Segment | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Balance Snapshot | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Batch Job Definition | Aggregate or core concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Versioned set of steps, dependencies, parameters, and policies. |
| Beneficiary | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Branch | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Business Calendar | Aggregate or core concept | [Organization Management](../01-business-capabilities/02-organization-management.md) | Working-day and holiday model applied by financial operations. |
| Business Date | Aggregate or core concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Institutional operating date used by financial logic. |
| Business Date | Value object or policy concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Business Date | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Business Date | Value object or policy concept | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Business Date Control | Aggregate or core concept | [Administration](../05-platform-capabilities/22-administration.md) | Current date, cut-off, close, and advance status. |
| Business Date State | Value object or policy concept | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Business Event | Aggregate or core concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) | Immutable fact that a meaningful state change occurred. |
| Calculation Base | Supporting entity | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Calculation Method | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Calendar Adjustment Rule | Value object or policy concept | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Capacity Metric | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Capitalization Record | Supporting entity | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Carry-Forward Record | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Causation ID | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Center | Aggregate or core concept | [Customer Management](../01-business-capabilities/01-customer-management.md) | Operational grouping of customer groups, often used in microfinance field operations. |
| Change Reason | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Change Set | Aggregate or core concept | [Audit](../05-platform-capabilities/23-audit.md) | Before-and-after representation of a controlled data change. |
| Channel | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Channel | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Channel | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Channel Preference | Aggregate or core concept | [Notification](../05-platform-capabilities/18-notification.md) | Permitted or preferred communication methods. |
| Charge Association | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Charge Component | Supporting entity | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Charge Definition | Aggregate or core concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Reusable fee or penalty policy and calculation basis. |
| Charge Definition | Aggregate or core concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Reusable fee or penalty definition. |
| Charge Instance | Aggregate or core concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Contract-specific assessed obligation and lifecycle state. |
| Charge Trigger | Aggregate or core concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Event or condition that creates an assessment. |
| Chart of Accounts | Aggregate or core concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Hierarchical account structure and classification model. |
| Checkpoint | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Cheque Detail | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Classification Date | Value object or policy concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Collateral Asset | Aggregate or core concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Independent asset record with type, ownership, identifiers, and lifecycle. |
| Collateral Link | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Collateral Monitoring Record | Aggregate or core concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Insurance, document, inspection, or expiry status. |
| Collateral Type | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Collection Activity | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Collection Case | Aggregate or core concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Operational recovery context linked to a delinquent contract. |
| Command Envelope | Aggregate or core concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) | Request to change state with actor, correlation, idempotency, and timing context. |
| Comment | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Compounding Frequency | Value object or policy concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Compounding Period | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Confidentiality Level | Value object or policy concept | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Configuration Item | Aggregate or core concept | [Configuration](../05-platform-capabilities/21-configuration.md) | Named value or structured object within a defined scope. |
| Configuration Version | Aggregate or core concept | [Configuration](../05-platform-capabilities/21-configuration.md) | Approved value set with effective dates and status. |
| Connector | Aggregate or core concept | [Integration](../05-platform-capabilities/19-integration.md) | Configuration and protocol adapter for an external system. |
| Consent | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Consent | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Contact Point | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Contribution Frequency | Value object or policy concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Contribution Schedule | Aggregate or core concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Required recurring installments and compliance status. |
| Correlation ID | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Correlation ID | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Correlation ID | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Correlation ID | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Correlation ID | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Correlation Trace | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Credential | Aggregate or core concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Authentication secret, key, certificate, or federated identity binding. |
| Credential Expiry | Value object or policy concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Credential Reference | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Credit | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Cure Date | Value object or policy concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Currency | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Currency | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Currency | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Currency Balance | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Currency Configuration | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Currency Definition | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Currency Precision | Value object or policy concept | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Currency Rule | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Customer | Aggregate or core concept | [Customer Management](../01-business-capabilities/01-customer-management.md) | Authoritative record for an individual or legal entity, including status and institutional ownership. |
| Customer Charge | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Customer Identifier | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Customer Note | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Customer Relationship | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Customer Type | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Cut-Off Window | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Dashboard Tile | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Data Lineage Record | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Data Type | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Data Version | Value object or policy concept | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Dataset or Read Model | Aggregate or core concept | [Reporting](../04-information-capabilities/16-reporting.md) | Curated source optimized for a reporting purpose. |
| Day-Count Convention | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Days Past Due | Value object or policy concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Days Past Due | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Dead-Letter Record | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Debit | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Debit or Credit | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Decision | Aggregate or core concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Approval, rejection, return, or exception outcome. |
| Decision Type | Value object or policy concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Default Value | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Delegation | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Delegation | Aggregate or core concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Time-bounded transfer of responsibility. |
| Delinquency Classification | Aggregate or core concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Contract-level current bucket, start date, and basis. |
| Delinquency History | Aggregate or core concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Immutable sequence of classifications and cures. |
| Delinquency Range | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Delinquency Scheme | Aggregate or core concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Ordered ranges and business rules used to classify exposure. |
| Delivery Attempt | Aggregate or core concept | [Notification](../05-platform-capabilities/18-notification.md) | Provider request, status, response, and retry metadata. |
| Delivery Guarantee | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Delivery Receipt | Supporting entity | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Delivery Status | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Deposit Product | Aggregate or core concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Template for fixed or recurring contractual deposits and maturity rules. |
| Deposit Term | Aggregate or core concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Contractual duration, lock-in, rate, and maturity conditions. |
| Device Context | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Dimension | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Direction | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Disbursement Tranche | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Distribution Channel | Value object or policy concept | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Distribution Schedule | Aggregate or core concept | [Reporting](../04-information-capabilities/16-reporting.md) | When and to whom scheduled outputs are delivered. |
| Dividend Allocation | Aggregate or core concept | [Share Management](../01-business-capabilities/08-share-management.md) | Member-level entitlement and payment status. |
| Dividend Declaration | Aggregate or core concept | [Share Management](../01-business-capabilities/08-share-management.md) | Approved distribution period, amount, eligibility, and calculation rule. |
| Dividend Rate | Value object or policy concept | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Document or File Object | Aggregate or core concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) | Stored binary or structured evidence referenced by domains. |
| Document Version | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Dormancy Record | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Due Date | Supporting entity | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Due Date | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Due Date | Value object or policy concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Dynamic Data Record | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Dynamic Field Definition | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Effective Date | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Effective Period | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Effective Period | Value object or policy concept | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Effective Period | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Eligibility Date | Value object or policy concept | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Eligibility Rule | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Eligibility Rule | Supporting entity | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Eligible Value | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Endpoint | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Environment | Value object or policy concept | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Error Detail | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Escalation Rule | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Event Time | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Evidence Package | Aggregate or core concept | [Audit](../05-platform-capabilities/23-audit.md) | Collected records supporting an investigation or control. |
| Evidence Reference | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Exchange Rate | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Execution Parameter | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Expiry Time | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Export Job | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| External Identifier | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| External Reference | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Failure Count | Value object or policy concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Failure Item | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Feature Flag | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Fee | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Fee Schedule | Aggregate or core concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Recurring or date-based assessment plan. |
| File Checksum | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Fiscal Period | Aggregate or core concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Open or closed accounting interval. |
| Fixed Amount | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Fixed Deposit Account | Aggregate or core concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Term contract funded by a principal amount and held to maturity. |
| Floating Rate | Aggregate or core concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Effective-dated reference rate and spread model. |
| Frequency | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Frequency | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Frequency | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Fund | Aggregate or core concept | [Organization Management](../01-business-capabilities/02-organization-management.md) | Named source or pool of funds used for portfolio attribution and reporting. |
| Fund Code | Value object or policy concept | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Funding Transaction | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| GL Account | Aggregate or core concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Individual asset, liability, equity, income, or expense account. |
| Grace Period | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Grace Period | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Group | Aggregate or core concept | [Customer Management](../01-business-capabilities/01-customer-management.md) | Collective customer structure used for group lending, joint liability, or community-based operations. |
| Guarantee Link | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Haircut | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Haircut | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Health Indicator | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Health Status | Value object or policy concept | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Held Amount | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Holiday | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Idempotency Key | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Idempotency Key | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Idempotency Record | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Identifier | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Image or Document Reference | Supporting entity | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Import or Export Job | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Index Observation | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Installment | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Installment Contribution | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Insurance Policy | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Integration Message | Aggregate or core concept | [Integration](../05-platform-capabilities/19-integration.md) | Inbound or outbound payload with correlation, schema, and processing state. |
| Integrity Seal | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Interest | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Interest Accrual | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Interest Period | Aggregate or core concept | [Savings Management](../01-business-capabilities/06-savings-management.md) | Calculation and posting context for account interest. |
| Interest Posting Instruction | Aggregate or core concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Amount and target date to be applied by the owning contract domain. |
| Interest Rule | Aggregate or core concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Calculation policy applied by a product or contract. |
| Interest Rule | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Job Instance | Aggregate or core concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | A scheduled or manually started execution for a business date. |
| Job Lock | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Job Status | Value object or policy concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Journal Entry | Aggregate or core concept | [Accounting](../03-financial-infrastructure/09-accounting.md) | Balanced accounting document containing one or more lines. |
| Journal Line | Supporting entity | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Language | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Ledger Balance | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Ledger Balance | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Ledger Posting | Aggregate or core concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Posted debit or credit line with source and period context. |
| Legal Form | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Lien | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Liquidation Record | Aggregate or core concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Recovery action and proceeds from disposal or enforcement. |
| Loan | Aggregate or core concept | [Loan Management](../01-business-capabilities/05-loan-management.md) | Active credit contract and primary aggregate for balances, obligations, and lifecycle state. |
| Loan Application | Aggregate or core concept | [Loan Management](../01-business-capabilities/05-loan-management.md) | Pre-contract request containing requested terms, applicant data, and decision history. |
| Loan Charge | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Loan Officer Assignment | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Loan Officer Assignment | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Loan Product | Aggregate or core concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Template for lending terms, schedules, allocation, charges, and accounting. |
| Loan Transaction | Aggregate or core concept | [Loan Management](../01-business-capabilities/05-loan-management.md) | Immutable financial event such as disbursement, repayment, refund, waiver, or write-off. |
| Loan-to-Value | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Locale | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Locale | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Lock-in Period | Value object or policy concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Login Attempt | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Lookup or Code Table | Aggregate or core concept | [Configuration](../05-platform-capabilities/21-configuration.md) | Governed list of extensible reference values. |
| Maintenance Mode | Value object or policy concept | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Maintenance Window | Aggregate or core concept | [Administration](../05-platform-capabilities/22-administration.md) | Planned restriction of platform operations. |
| Maker-Checker Pair | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Manual Journal | Aggregate or core concept | [Accounting](../03-financial-infrastructure/09-accounting.md) | Authorized non-automated accounting adjustment. |
| Mapping Definition | Aggregate or core concept | [Integration](../05-platform-capabilities/19-integration.md) | Transformation between external and canonical structures. |
| Market Value | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Maturity Amount | Value object or policy concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Maturity Date | Value object or policy concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Maturity Instruction | Aggregate or core concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Customer or product instruction for payout, transfer, partial renewal, or full renewal. |
| Maximum | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Maximum Holding | Value object or policy concept | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Media Type | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Message Status | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Metadata Definition | Aggregate or core concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) | Description of configurable fields and entity extensions. |
| Metric | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Minimum | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Minimum and Maximum | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Minimum Balance | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Minimum Holding | Value object or policy concept | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Missed Installment | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Nominal Value | Value object or policy concept | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Nominee | Supporting entity | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Normal Balance | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Notification Request | Aggregate or core concept | [Notification](../05-platform-capabilities/18-notification.md) | Intent to communicate, including event, recipients, priority, and template. |
| Number Sequence | Aggregate or core concept | [Configuration](../05-platform-capabilities/21-configuration.md) | Controlled generator for business identifiers. |
| Office | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Office Assignment | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Office Hierarchy | Aggregate or core concept | [Organization Management](../01-business-capabilities/02-organization-management.md) | Tree of organizational units with controlled parent-child relationships. |
| Office Type | Value object or policy concept | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Opening Balance | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Operational Alert | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Operational Environment | Aggregate or core concept | [Administration](../05-platform-capabilities/22-administration.md) | Deployment context and controlled configuration promotion path. |
| Operational Task | Aggregate or core concept | [Administration](../05-platform-capabilities/22-administration.md) | Privileged action with state, actor, and evidence. |
| Outcome | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Output Artifact | Aggregate or core concept | [Reporting](../04-information-capabilities/16-reporting.md) | Generated statement, file, dashboard dataset, or regulatory package. |
| Output Format | Value object or policy concept | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Outstanding Amount | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Overdraft Facility | Aggregate or core concept | [Savings Management](../01-business-capabilities/06-savings-management.md) | Authorized negative-balance limit and pricing terms. |
| Overdraft Limit | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Overdue Fees | Value object or policy concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Overdue Interest | Value object or policy concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Overdue Principal | Value object or policy concept | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Override | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Owner | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Partition | Aggregate or core concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Independent slice of a large workload. |
| Password History | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Past-Due Component | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Payment | Aggregate or core concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | End-to-end payment lifecycle and current processing state. |
| Payment Allocation | Supporting entity | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Payment Allocation | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Payment Detail | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Payment Instruction | Aggregate or core concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Payer, payee, amount, currency, purpose, timing, and routing request. |
| Payment Method | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Payment Status | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Penalty | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Penalty | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Penalty Trigger | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Percentage | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Period | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Permission | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Permission Scope | Value object or policy concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Pledge | Aggregate or core concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Legal or operational assignment of collateral to an exposure, including priority and secured amount. |
| Posting Batch | Supporting entity | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Posting Batch | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Posting Date | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Posting Date | Value object or policy concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Posting Frequency | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Posting Period | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Posting Profile | Aggregate or core concept | [Accounting](../03-financial-infrastructure/09-accounting.md) | Product or operation-specific collection of accounting mappings. |
| Precedence | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Preferred Language | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Premature Closure Quote | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Principal | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Priority | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Priority | Value object or policy concept | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Priority | Value object or policy concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Processed Count | Value object or policy concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Product Mix Rule | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Product Version | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Promise to Pay | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Protocol | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Provider Configuration | Supporting entity | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Provisioning Category | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Provisioning Entry | Supporting entity | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Query Contract | Aggregate or core concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) | Read request and projection result. |
| Rate Floor or Cap | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Rate History | Aggregate or core concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Immutable sequence of effective rate changes. |
| Rate Plan | Aggregate or core concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Fixed or floating rate definition with effective periods. |
| Reason | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Recalculation Context | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Recipient Resolution | Aggregate or core concept | [Notification](../05-platform-capabilities/18-notification.md) | Resolved address, role, consent, and language context. |
| Reconciliation Item | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Reconciliation Reference | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Recorded Time | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Recovery Objective | Value object or policy concept | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Recovery Payment | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Recovery Point | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Recurring Deposit Account | Aggregate or core concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Term contract funded through scheduled periodic contributions. |
| Redemption Request | Supporting entity | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Reference Data Set | Aggregate or core concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) | Shared governed codes and values. |
| Region | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Release Request | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Renewal Option | Value object or policy concept | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Renewal Record | Supporting entity | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |  |
| Repayment Frequency | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Repayment Rule | Supporting entity | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Repayment Schedule | Aggregate or core concept | [Loan Management](../01-business-capabilities/05-loan-management.md) | Contractual sequence of installments and due components. |
| Report Definition | Aggregate or core concept | [Reporting](../04-information-capabilities/16-reporting.md) | Query, layout, parameters, security, and output configuration. |
| Report Parameter | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Report Run | Aggregate or core concept | [Reporting](../04-information-capabilities/16-reporting.md) | Execution request with as-of time, parameters, status, and evidence. |
| Reschedule Request | Aggregate or core concept | [Loan Management](../01-business-capabilities/05-loan-management.md) | Controlled proposal to amend future obligations or contractual terms. |
| Resource Reference | Supporting entity | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Restart Point | Value object or policy concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Retention Class | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Retention Policy | Aggregate or core concept | [Audit](../05-platform-capabilities/23-audit.md) | Rules for preservation, legal hold, archival, and disposal. |
| Retry Attempt | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Retry Policy | Supporting entity | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Retry Record | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Return | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Reversal | Supporting entity | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Reversal Link | Supporting entity | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Risk Grade | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
| Role | Aggregate or core concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Reusable bundle of permissions and optional organizational scope. |
| Role Assignment | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Rounding Result | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Rounding Rule | Value object or policy concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |  |
| Rounding Scale | Value object or policy concept | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Rule Set | Aggregate or core concept | [Configuration](../05-platform-capabilities/21-configuration.md) | Configurable decision logic with version and context. |
| Savings Account | Aggregate or core concept | [Savings Management](../01-business-capabilities/06-savings-management.md) | Open-ended deposit contract and primary balance-owning aggregate. |
| Savings Product | Aggregate or core concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Template for transactional deposit accounts, interest, overdraft, and fees. |
| Savings Transaction | Aggregate or core concept | [Savings Management](../01-business-capabilities/06-savings-management.md) | Immutable deposit, withdrawal, transfer, fee, interest, or reversal event. |
| Schedule | Supporting entity | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Schedule Variation | Supporting entity | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Scheduler Control | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Schema Version | Supporting entity | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Schema Version | Value object or policy concept | [Integration](../05-platform-capabilities/19-integration.md) |  |
| Schema Version | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Scope | Supporting entity | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Search Index Entry | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Secured Amount | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Self-Service User Link | Supporting entity | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Sensitivity | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Sensitivity | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Session | Aggregate or core concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Time-bounded authenticated context with device and channel information. |
| Session Control | Supporting entity | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Session Risk | Value object or policy concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Settlement Date | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Settlement Record | Aggregate or core concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | External or internal evidence of clearing and final settlement. |
| Share Account | Aggregate or core concept | [Share Management](../01-business-capabilities/08-share-management.md) | Customer or member relationship to issued institutional shares. |
| Share Certificate Reference | Supporting entity | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Share Holding | Aggregate or core concept | [Share Management](../01-business-capabilities/08-share-management.md) | Quantity and value of active shares, potentially organized into purchase lots. |
| Share Product | Aggregate or core concept | [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Template for member equity, issuance, redemption, and dividend constraints. |
| Share Purchase Lot | Supporting entity | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Share Quantity | Value object or policy concept | [Share Management](../01-business-capabilities/08-share-management.md) |  |
| Share Transaction | Aggregate or core concept | [Share Management](../01-business-capabilities/08-share-management.md) | Purchase, additional purchase, redemption, adjustment, or reversal. |
| SLA | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Source Event | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Source Reference | Supporting entity | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Source System | Value object or policy concept | [Audit](../05-platform-capabilities/23-audit.md) |  |
| Spread | Supporting entity | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |  |
| Staff Assignment | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Staff Member | Aggregate or core concept | [Organization Management](../01-business-capabilities/02-organization-management.md) | Operational person assigned to one or more offices and business responsibilities. |
| Staff Status | Value object or policy concept | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Stage | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Standing Instruction | Aggregate or core concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Recurring future payment instruction. |
| Standing Instruction Link | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Start and End Time | Value object or policy concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |  |
| Statement Mapping | Aggregate or core concept | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Relationship from GL accounts to reporting lines and financial statements. |
| Statement Period | Supporting entity | [Reporting](../04-information-capabilities/16-reporting.md) |  |
| Status | Value object or policy concept | [Customer Management](../01-business-capabilities/01-customer-management.md) |  |
| Step Execution | Aggregate or core concept | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Status, counters, checkpoints, and errors for a job step. |
| Subscription or Webhook | Aggregate or core concept | [Integration](../05-platform-capabilities/19-integration.md) | Registered recipient for published events. |
| Substitution Request | Supporting entity | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Suppression Record | Supporting entity | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Task | Aggregate or core concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Unit of human or automated work with assignee and due date. |
| Task Status | Value object or policy concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Tax Component where applicable | Supporting entity | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Template | Aggregate or core concept | [Notification](../05-platform-capabilities/18-notification.md) | Versioned content for a channel and locale. |
| Template Variable | Supporting entity | [Notification](../05-platform-capabilities/18-notification.md) |  |
| Tenant | Aggregate or core concept | [Administration](../05-platform-capabilities/22-administration.md) | Isolated institution or business unit with its operational context. |
| Tenant Scope | Value object or policy concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Tenant Status | Value object or policy concept | [Administration](../05-platform-capabilities/22-administration.md) |  |
| Time Context | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Timezone | Value object or policy concept | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Transaction Limit | Supporting entity | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Transaction Trace | Aggregate or core concept | [Audit](../05-platform-capabilities/23-audit.md) | Correlated path across business, payment, accounting, GL, and integration records. |
| Transfer | Aggregate or core concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Linked debit and credit legs for an internal or external movement. |
| Transition | Supporting entity | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Trial Balance | Supporting entity | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |  |
| Trigger Event | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| User Account | Aggregate or core concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Security principal used to authenticate and authorize a person or system. |
| User Status | Value object or policy concept | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |  |
| Validation Constraint | Value object or policy concept | [Configuration](../05-platform-capabilities/21-configuration.md) |  |
| Validation Result | Supporting entity | [Platform Services](../05-platform-capabilities/24-platform-services.md) |  |
| Valuation | Aggregate or core concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Effective-dated appraisal and eligible value. |
| Valuation Date | Value object or policy concept | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |  |
| Value Date | Value object or policy concept | [Accounting](../03-financial-infrastructure/09-accounting.md) |  |
| Value Date | Value object or policy concept | [Loan Management](../01-business-capabilities/05-loan-management.md) |  |
| Value Date | Value object or policy concept | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |  |
| Value Date | Value object or policy concept | [Savings Management](../01-business-capabilities/06-savings-management.md) |  |
| Waiver or Refund | Aggregate or core concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Authorized adjustment with reason and financial treatment. |
| Waiver Reason | Value object or policy concept | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |  |
| Workflow Definition | Aggregate or core concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Versioned graph of stages, tasks, transitions, and conditions. |
| Workflow Instance | Aggregate or core concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Execution state for a specific business case. |
| Workflow Version | Value object or policy concept | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |  |
| Working-Day Rule | Supporting entity | [Organization Management](../01-business-capabilities/02-organization-management.md) |  |
| Write-Off Eligibility | Supporting entity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |  |
