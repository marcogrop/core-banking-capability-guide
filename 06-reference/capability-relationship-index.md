---
id: capability-relationship-index
title: Capability Relationship Index
category: Reference
status: reference
---

# Capability Relationship Index

This index collects the directional collaboration descriptions defined by each capability chapter.

| Owning capability | Related capability or group | Interaction |
|---|---|---|
| [Customer Management](../01-business-capabilities/01-customer-management.md) | Organization Management | Assigns the servicing office, center, and responsible staff. |
| [Customer Management](../01-business-capabilities/01-customer-management.md) | Identity & Security | May link a customer to a self-service digital identity, but does not authenticate the person itself. |
| [Customer Management](../01-business-capabilities/01-customer-management.md) | Product Catalog | Supplies eligibility context and segmentation attributes used during product selection. |
| [Customer Management](../01-business-capabilities/01-customer-management.md) | Loan / Savings / Deposit / Share Management | Contracts reference the customer master as holder, borrower, member, guarantor, or beneficiary. |
| [Customer Management](../01-business-capabilities/01-customer-management.md) | Notification | Uses verified contact points, language, consent, and channel preferences. |
| [Customer Management](../01-business-capabilities/01-customer-management.md) | Reporting and Audit | Consume the customer reference to produce consolidated views and trace changes. |
| [Organization Management](../01-business-capabilities/02-organization-management.md) | Customer Management | Customers are owned and serviced through an office or center. |
| [Organization Management](../01-business-capabilities/02-organization-management.md) | Identity & Security | Roles and permissions are often constrained by office scope. |
| [Organization Management](../01-business-capabilities/02-organization-management.md) | Loan and Deposit Domains | Contracts record branch, officer, and fund attribution. |
| [Organization Management](../01-business-capabilities/02-organization-management.md) | Batch Processing | Uses business calendars and organization cut-off rules. |
| [Organization Management](../01-business-capabilities/02-organization-management.md) | Accounting and Reporting | Aggregate postings and performance by office, staff, region, and fund. |
| [Organization Management](../01-business-capabilities/02-organization-management.md) | Administration | Operates the organization model but does not replace it. |
| [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Organization Management | Constrains access by office, region, staff assignment, or tenant. |
| [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Workflow & Approval | Uses authenticated actors, roles, and delegation to assign and approve tasks. |
| [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Administration | Manages privileged operations and security configuration. |
| [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Audit | Records authentication, authorization, role changes, and privileged actions. |
| [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | All Business Capabilities | Receive a verified actor and authorization decision but still enforce their own invariants. |
| [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) | Integration | Authenticates external clients, service accounts, and identity providers. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Interest Engine | Supplies calculation methods, rate plans, day-count, and posting conventions. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Fee Engine | Supplies charge definitions, triggers, schedules, and waiver rules. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Limits and Exposure Management | Supplies limit types, facility rules, overdraft rules, utilization behavior, and product-level exposure constraints. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Accounting | Consumes product-to-ledger mappings and posting profiles. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Loan / Savings / Deposit / Share / Card Management | Instantiate contracts or access instruments from effective product versions. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Customer Onboarding / KYC | Uses product eligibility and due-diligence requirements during onboarding. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Configuration | Provides institution-wide defaults, feature flags, and code tables. |
| [Product Catalog](../01-business-capabilities/04-product-catalog.md) | Reporting | Uses product hierarchy and versions as primary analytical dimensions. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Customer Management | Identifies borrowers, co-borrowers, guarantors, and related parties. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Product Catalog | Provides contractual defaults and limits for origination. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Interest Engine and Fee Engine | Calculate time-based and event-based obligations. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Payment Processing | Executes disbursement and repayment movements. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Delinquency Management | Classifies arrears and supplies collection and provisioning context. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Collateral Management | Maintains pledged security and loan-to-value metrics. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Accounting and General Ledger | Record disbursement, accrual, repayment, write-off, and recovery effects. |
| [Loan Management](../01-business-capabilities/05-loan-management.md) | Workflow & Approval | Coordinates credit decisions, exceptions, restructures, and waivers. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Customer Management | Identifies holders, joint holders, signatories, and beneficiaries. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Product Catalog | Supplies balance rules, interest, overdraft, fees, and limits. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Payment Processing | Executes transfers, cash movements, and external payments. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Interest Engine and Fee Engine | Calculate interest, maintenance fees, overdraft pricing, and penalties. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Accounting and General Ledger | Record deposit liabilities, cash movement, fees, and interest expense. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Batch Processing | Runs interest posting, dormancy, charges, and statement cycles. |
| [Savings Management](../01-business-capabilities/06-savings-management.md) | Notification and Reporting | Produce alerts, statements, and customer views. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Customer Management | Identifies depositors, joint holders, nominees, and beneficiaries. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Product Catalog | Defines term options, rates, penalties, and maturity behavior. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Interest Engine and Fee Engine | Calculate contractual returns and early-termination consequences. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Payment Processing | Moves initial funding, contributions, maturity proceeds, and refunds. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Batch Processing | Runs accrual, maturity, renewal, and missed-installment detection. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Accounting and General Ledger | Record deposit liabilities and interest expense. |
| [Deposit Management](../01-business-capabilities/07-deposit-management.md) | Notification | Sends contribution reminders, maturity notices, and renewal confirmations. |
| [Share Management](../01-business-capabilities/08-share-management.md) | Customer Management | Identifies members, joint holders, and nominees. |
| [Share Management](../01-business-capabilities/08-share-management.md) | Product Catalog | Defines share classes, nominal value, limits, and dividend eligibility. |
| [Share Management](../01-business-capabilities/08-share-management.md) | Payment Processing | Collects purchases and pays redemptions or dividends. |
| [Share Management](../01-business-capabilities/08-share-management.md) | Accounting and General Ledger | Record equity issuance, redemption, and distributions. |
| [Share Management](../01-business-capabilities/08-share-management.md) | Workflow & Approval | Coordinates dividend declaration and restricted redemptions. |
| [Share Management](../01-business-capabilities/08-share-management.md) | Reporting | Produces member registers, capital reports, and dividend statements. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | Product Catalog | Defines product accounting mappings and posting profiles. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | Loan / Savings / Deposit / Share Management | Publish financial events and maintain operational subledgers. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | Payment Processing | Publishes cash and settlement events. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | Fee and Interest Engines | Provide calculated financial components. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | General Ledger | Receives validated journals and maintains ledger balances. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | Batch Processing | Runs accrual, provisioning, aggregation, and scheduled posting. |
| [Accounting](../03-financial-infrastructure/09-accounting.md) | Audit and Reporting | Trace source-to-entry lineage and produce accounting reports. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Savings Management | Provides source and destination account state and balances. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Loan, Deposit, Share, and Card Management | Receive repayments, disbursements, contributions, maturity proceeds, card-originated movements, and issuer settlement context. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Limits and Exposure Management | Supplies limit, overdraft, exposure, and authorization constraints where payment movement consumes availability. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Accounting and General Ledger | Record cash, settlement, suspense, and transfer entries. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Integration | Connects payment gateways, switches, clearing systems, banks, processors, fraud services, and scheme endpoints. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Batch Processing | Executes standing instructions, bulk files, settlement cycles, and reconciliation. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Notification | Communicates payment status and exceptions. |
| [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) | Audit | Maintains end-to-end transaction trace. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Product Catalog | Selects interest methods and parameters for products. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Loan Management | Uses the engine for scheduled and accrued lending interest. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Savings and Deposit Management | Use the engine for payable interest and overdraft interest. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Accounting | Recognizes accrued and posted interest. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Batch Processing | Runs periodic accrual and posting jobs. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Configuration | Provides calendars, precision, and institution-wide conventions. |
| [Interest Engine](../02-policy-capabilities/11-interest-engine.md) | Reporting and Audit | Require reproducible calculation detail. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Product Catalog | Associates charge definitions with products and lifecycle events. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Loan / Savings / Deposit / Share Management | Own contract-specific charge instances and apply outcomes. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Delinquency Management | May trigger penalties from arrears status. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Payment Processing | Collects or refunds assessed amounts. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Accounting | Recognizes fee income, receivables, waivers, refunds, and capitalization. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Workflow & Approval | Authorizes exceptional waivers, refunds, and overrides. |
| [Fee Engine](../02-policy-capabilities/12-fee-engine.md) | Notification | Communicates assessments and due dates. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Loan Management | Provides contractual due amounts, repayments, schedule changes, and write-off state. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Fee Engine | May assess overdue penalties from classification changes. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Workflow & Approval | Coordinates collection actions, exceptions, restructures, and write-off decisions. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Accounting | Uses classification for provisioning and impairment entries. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Reporting | Produces arrears, migration, vintage, cure, and recovery analytics. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Batch Processing | Runs periodic classification and portfolio updates. |
| [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) | Notification | Sends reminders and arrears communications subject to policy. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Customer Management | Identifies owners, borrowers, and related parties. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Loan Management | References collateral pledges and secured exposure. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Product Catalog | Defines eligible collateral types and LTV policies. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Workflow & Approval | Coordinates valuation approval, substitution, release, and enforcement. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Accounting | Records liquidation proceeds and impairment effects. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Reporting | Produces collateral coverage, concentration, expiry, and valuation reports. |
| [Collateral Management](../02-policy-capabilities/14-collateral-management.md) | Document Management in Platform Services | Stores appraisals, titles, insurance, and legal evidence. |
| [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Accounting | Generates balanced journals and posting instructions. |
| [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | All Financial Domains | Provide source events through Accounting rather than posting directly where possible. |
| [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Reporting | Builds financial statements and management reports from GL data. |
| [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Administration | Controls period operations and privileged ledger maintenance. |
| [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Audit | Traces every posting to source, actor, rule, and reversal. |
| [General Ledger](../03-financial-infrastructure/15-general-ledger.md) | Integration | Exports ledger data to consolidation, treasury, tax, or enterprise finance systems. |
| [Reporting](../04-information-capabilities/16-reporting.md) | All Business and Financial Capabilities | Provide authoritative source data and events. |
| [Reporting](../04-information-capabilities/16-reporting.md) | General Ledger | Provides financial balances and statement foundations. |
| [Reporting](../04-information-capabilities/16-reporting.md) | Batch Processing | Runs scheduled and high-volume report generation. |
| [Reporting](../04-information-capabilities/16-reporting.md) | Identity & Security | Controls row, field, tenant, and report access. |
| [Reporting](../04-information-capabilities/16-reporting.md) | Notification | Distributes statements and report completion notices. |
| [Reporting](../04-information-capabilities/16-reporting.md) | Audit | Records who generated, accessed, or exported sensitive information. |
| [Reporting](../04-information-capabilities/16-reporting.md) | Integration | Publishes outputs to regulators, BI platforms, or data warehouses. |
| [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Identity & Security | Provides users, roles, permissions, and delegation eligibility. |
| [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Organization Management | Provides assignment scope by office, region, team, and staff. |
| [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Loan, Customer, Product, Accounting, Collateral, and Administration Domains | Expose requests and commands that may require approval. |
| [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Notification | Alerts assignees, requesters, and escalation recipients. |
| [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Audit | Preserves task, decision, actor, and evidence history. |
| [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) | Configuration | Defines thresholds, routing policies, and feature enablement. |
| [Notification](../05-platform-capabilities/18-notification.md) | Customer Management | Provides contact points, language, consent, and customer relationships. |
| [Notification](../05-platform-capabilities/18-notification.md) | Identity & Security | Provides internal users and secure in-app recipients. |
| [Notification](../05-platform-capabilities/18-notification.md) | All Business Capabilities | Publish events and request confirmations, alerts, and reminders. |
| [Notification](../05-platform-capabilities/18-notification.md) | Workflow & Approval | Generates task and escalation notifications. |
| [Notification](../05-platform-capabilities/18-notification.md) | Integration | Connects external email, SMS, push, and messaging providers. |
| [Notification](../05-platform-capabilities/18-notification.md) | Audit | Records sensitive or mandatory communications. |
| [Notification](../05-platform-capabilities/18-notification.md) | Configuration | Defines templates, provider selection, retry, and suppression policies. |
| [Integration](../05-platform-capabilities/19-integration.md) | All Domain Capabilities | Expose commands, queries, and events through stable application contracts. |
| [Integration](../05-platform-capabilities/19-integration.md) | Identity & Security | Authenticates clients and protects scopes and credentials. |
| [Integration](../05-platform-capabilities/19-integration.md) | Payment Processing | Connects payment rails and settlement services. |
| [Integration](../05-platform-capabilities/19-integration.md) | Notification | Connects communication providers. |
| [Integration](../05-platform-capabilities/19-integration.md) | Reporting | Exports data and regulatory packages. |
| [Integration](../05-platform-capabilities/19-integration.md) | Batch Processing | Executes large imports, exports, and reconciliation. |
| [Integration](../05-platform-capabilities/19-integration.md) | Audit | Tracks external requests, responses, and transformations. |
| [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Interest, Fee, Delinquency, Loan, Savings, Deposit, Accounting, Reporting | Provide batch operations and domain-specific commands. |
| [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Administration | Schedules, starts, pauses, restarts, and monitors jobs. |
| [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Configuration and Organization Management | Provide business date, calendars, cut-offs, and parameters. |
| [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Integration | Supports large imports, exports, and settlement files. |
| [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Audit | Records privileged interventions and execution history. |
| [Batch Processing](../05-platform-capabilities/20-batch-processing.md) | Notification | Alerts operators to failures and completion. |
| [Configuration](../05-platform-capabilities/21-configuration.md) | All Capabilities | Consume configuration but remain responsible for interpreting it within domain rules. |
| [Configuration](../05-platform-capabilities/21-configuration.md) | Product Catalog | Uses configuration defaults and may provide product-specific overrides. |
| [Configuration](../05-platform-capabilities/21-configuration.md) | Organization Management | Defines scope and calendars. |
| [Configuration](../05-platform-capabilities/21-configuration.md) | Workflow & Approval | Approves sensitive changes. |
| [Configuration](../05-platform-capabilities/21-configuration.md) | Administration | Operates configuration deployment and environment promotion. |
| [Configuration](../05-platform-capabilities/21-configuration.md) | Audit and Reporting | Record changes and expose effective values used in decisions. |
| [Administration](../05-platform-capabilities/22-administration.md) | Identity & Security | Protects privileged roles, sessions, and emergency access. |
| [Administration](../05-platform-capabilities/22-administration.md) | Batch Processing | Provides job operation and business-date workflows. |
| [Administration](../05-platform-capabilities/22-administration.md) | Configuration | Controls runtime and tenant settings. |
| [Administration](../05-platform-capabilities/22-administration.md) | Integration and Notification | Expose provider health and operational failures. |
| [Administration](../05-platform-capabilities/22-administration.md) | Audit | Records every privileged administrative action. |
| [Administration](../05-platform-capabilities/22-administration.md) | Reporting | Provides operational dashboards and service metrics. |
| [Administration](../05-platform-capabilities/22-administration.md) | All Business Capabilities | Are observed and controlled but not semantically owned by Administration. |
| [Audit](../05-platform-capabilities/23-audit.md) | All Capabilities | Publish auditable actions and references. |
| [Audit](../05-platform-capabilities/23-audit.md) | Identity & Security | Provides authenticated actor, session, and authorization context. |
| [Audit](../05-platform-capabilities/23-audit.md) | Workflow & Approval | Provides decision and evidence history. |
| [Audit](../05-platform-capabilities/23-audit.md) | Accounting and General Ledger | Provide financial lineage. |
| [Audit](../05-platform-capabilities/23-audit.md) | Integration | Provides external request, message, and provider trace. |
| [Audit](../05-platform-capabilities/23-audit.md) | Administration | Defines retention, access, export, and legal-hold operation. |
| [Audit](../05-platform-capabilities/23-audit.md) | Reporting | Provides controlled audit and compliance reports. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | All Capabilities | Use shared envelopes and services while retaining domain ownership. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | Identity & Security | Provides actor and authorization context. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | Integration | Exposes commands, queries, and events externally. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | Audit | Consumes correlation and causation context. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | Configuration | Defines reference data, metadata, and localization settings. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | Notification and Reporting | Use document, localization, and file services. |
| [Platform Services](../05-platform-capabilities/24-platform-services.md) | Administration | Operates storage, indexing, and shared technical services. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Customer Management | Identifies cardholders, authorized users, contact points, and party relationships. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Customer Onboarding / KYC | Provides onboarding status and due-diligence conditions required before card issuance. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Product Catalog | Defines card products, card fees, eligibility, controls, and linked account rules. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Savings Management | Provides linked deposit or transactional account state and available funds. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Loan Management | Provides credit-card, revolving-credit, or loan-backed contract context where applicable. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Limits and Exposure Management | Supplies card authorization limits, credit utilization, and breach decisions. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Fee Engine | Calculates card fees, transaction charges, and waivers. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Payment Processing | Executes card-originated financial movements, settlement, returns, and reversals. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Integration | Connects processors, token services, wallets, fraud services, and card networks. |
| [Card Management](../01-business-capabilities/25-card-management.md) | Audit | Preserves authorization, clearing, dispute, status, and processor evidence. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Customer Management | Supplies party, group, household, organization, and related-party context. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Product Catalog | Defines product-level limit rules, eligibility, and utilization behavior. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Loan Management | Consumes facility, drawdown, disbursement, refinance, and restructure limit decisions. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Savings Management | Consumes overdraft, hold, account, and available-balance limit decisions. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Card Management | Consumes card authorization, velocity, and credit-limit decisions. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Collateral Management | Supplies pledged coverage, LTV, valuation, and secured exposure context. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Workflow & Approval | Coordinates limit approval, renewal, breach, override, and exception handling. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Accounting | May consume exposure state for provisions, commitments, and risk-related postings. |
| [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) | Reporting | Produces exposure, concentration, utilization, breach, and facility reports. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Customer Management | Receives accepted customer, party relationship, contact, and classification facts. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Organization Management | Supplies servicing office, channel, staff, and assignment context. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Product Catalog | Supplies requested product eligibility and onboarding requirements. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Identity & Security | May create or link digital identities after the customer or applicant is eligible. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Workflow & Approval | Coordinates enhanced due diligence, exceptions, and approval decisions. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Integration | Connects identity verification, document verification, registry, tax, sanctions, AML, and fraud services. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Audit | Preserves evidence, screening, decisions, and customer-conversion lineage. |
| [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) | Reporting | Produces onboarding funnel, rejection, remediation, and compliance operational reports. |
