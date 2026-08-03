---
id: commands-and-events-index
title: Commands and Business Events Index
category: Reference
status: reference
---

# Commands and Business Events Index

This index is representative rather than exhaustive. Operations should be refined into full specifications with authorization, preconditions, invariants, state transitions, financial consequences, idempotency, and error outcomes.

## Commands

| Command | Capability |
|---|---|
| Close Accounting Period | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Create Manual Journal | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Define Accounting Rule | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Generate Journal | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Generate Provisioning Entries | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Post Journal | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Reverse Journal | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Run Accrual | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Acknowledge Operational Alert | [Administration](../05-platform-capabilities/22-administration.md) |
| Advance Business Date | [Administration](../05-platform-capabilities/22-administration.md) |
| Provision Tenant | [Administration](../05-platform-capabilities/22-administration.md) |
| Restore Environment | [Administration](../05-platform-capabilities/22-administration.md) |
| Set Maintenance Mode | [Administration](../05-platform-capabilities/22-administration.md) |
| Start Scheduled Task | [Administration](../05-platform-capabilities/22-administration.md) |
| Terminate Session | [Administration](../05-platform-capabilities/22-administration.md) |
| Trigger Backup | [Administration](../05-platform-capabilities/22-administration.md) |
| Create Evidence Package | [Audit](../05-platform-capabilities/23-audit.md) |
| Dispose Expired Records | [Audit](../05-platform-capabilities/23-audit.md) |
| Export Audit Evidence | [Audit](../05-platform-capabilities/23-audit.md) |
| Place Legal Hold | [Audit](../05-platform-capabilities/23-audit.md) |
| Record Audit Event | [Audit](../05-platform-capabilities/23-audit.md) |
| Seal Record | [Audit](../05-platform-capabilities/23-audit.md) |
| Search Audit | [Audit](../05-platform-capabilities/23-audit.md) |
| Advance Business Date | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Cancel Job | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Pause Job | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Reprocess Failed Items | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Restart Job | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Resume Job | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Schedule Job | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Start Job | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Liquidate Collateral | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Pledge Collateral | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Record Insurance | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Record Valuation | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Register Collateral | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Release Collateral | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Revalue Collateral | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Substitute Collateral | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Activate Version | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Advance Number Sequence | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Approve Configuration | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Create Configuration Draft | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Create Lookup Value | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Rollback Version | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Schedule Activation | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Validate Configuration | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Activate Customer | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Add Address | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Add Identifier | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Close Customer | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Create Customer | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Submit Customer | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Transfer Customer | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Update Profile | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Assess Write-Off Eligibility | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Classify Contract | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Define Scheme | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Mark Cured | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Open Collection Case | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Record Collection Activity | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Record Promise to Pay | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Close Deposit | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Fund Deposit | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Open Fixed Deposit | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Open Recurring Deposit | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Post Interest | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Quote Premature Closure | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Record Contribution | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Renew Deposit | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Set Maturity Instruction | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Assess Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Capitalize Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Define Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Pay Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Refund Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Reverse Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Schedule Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Waive Charge | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Activate GL Account | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Block Account | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Carry Forward Balance | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Close Period | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Create GL Account | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Map Statement Line | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Open Period | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Post Journal | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Assign Role | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Authenticate | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Create User | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Delegate Authority | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Lock User | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Refresh Session | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Reset Credential | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Revoke Role | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Consume Message | [Integration](../05-platform-capabilities/19-integration.md) |
| Export Data | [Integration](../05-platform-capabilities/19-integration.md) |
| Import Data | [Integration](../05-platform-capabilities/19-integration.md) |
| Publish Event | [Integration](../05-platform-capabilities/19-integration.md) |
| Register Connector | [Integration](../05-platform-capabilities/19-integration.md) |
| Register Webhook | [Integration](../05-platform-capabilities/19-integration.md) |
| Reprocess Dead Letter | [Integration](../05-platform-capabilities/19-integration.md) |
| Retry Exchange | [Integration](../05-platform-capabilities/19-integration.md) |
| Accrue Interest | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Calculate Interest | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Define Rate Plan | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Generate Posting Instruction | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Recalculate Period | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Supersede Rate | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Approve Loan | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Close Loan | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Disburse Loan | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Foreclose Loan | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Make Repayment | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Record Recovery | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Reschedule Loan | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Reverse Transaction | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Submit Application | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Waive Charge | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Write Off Loan | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Cancel Pending Notification | [Notification](../05-platform-capabilities/18-notification.md) |
| Create Template | [Notification](../05-platform-capabilities/18-notification.md) |
| Request Notification | [Notification](../05-platform-capabilities/18-notification.md) |
| Retry Delivery | [Notification](../05-platform-capabilities/18-notification.md) |
| Schedule Reminder | [Notification](../05-platform-capabilities/18-notification.md) |
| Suppress Notification | [Notification](../05-platform-capabilities/18-notification.md) |
| Activate Office | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Assign Staff | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Configure Working Days | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Create Fund | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Create Office | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Create Staff | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Define Holiday | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Move Office | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Authorize Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Create Standing Instruction | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Execute Transfer | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Initiate Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Record Settlement | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Return Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Reverse Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Submit to Clearing | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Execute Command | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Generate Identifier | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Index Resource | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Manage Reference Data | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Publish Business Event | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Run Query | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Store Document | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Version Document | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Activate Product | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Add Charge | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Approve Product Version | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Configure Accounting | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Create Product Draft | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Define Eligibility | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Retire Product | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Approve Report | [Reporting](../04-information-capabilities/16-reporting.md) |
| Archive Report | [Reporting](../04-information-capabilities/16-reporting.md) |
| Define Report | [Reporting](../04-information-capabilities/16-reporting.md) |
| Distribute Output | [Reporting](../04-information-capabilities/16-reporting.md) |
| Export Data | [Reporting](../04-information-capabilities/16-reporting.md) |
| Generate Statement | [Reporting](../04-information-capabilities/16-reporting.md) |
| Run Report | [Reporting](../04-information-capabilities/16-reporting.md) |
| Schedule Report | [Reporting](../04-information-capabilities/16-reporting.md) |
| Activate Account | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Assess Charge | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Close Account | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Deposit Funds | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Mark Dormant | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Open Account | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Place Hold | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Post Interest | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Release Hold | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Reverse Transaction | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Withdraw Funds | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Allocate Dividend | [Share Management](../01-business-capabilities/08-share-management.md) |
| Apply for Shares | [Share Management](../01-business-capabilities/08-share-management.md) |
| Approve Share Account | [Share Management](../01-business-capabilities/08-share-management.md) |
| Close Share Account | [Share Management](../01-business-capabilities/08-share-management.md) |
| Declare Dividend | [Share Management](../01-business-capabilities/08-share-management.md) |
| Pay Dividend | [Share Management](../01-business-capabilities/08-share-management.md) |
| Purchase Shares | [Share Management](../01-business-capabilities/08-share-management.md) |
| Redeem Shares | [Share Management](../01-business-capabilities/08-share-management.md) |
| Approve Request | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Cancel Workflow | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Complete Task | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Delegate Authority | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Escalate Task | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Reassign Task | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Reject Request | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Return Request | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Start Workflow | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Activate Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Approve Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Block Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Close Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Issue Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Open Card Dispute | [Card Management](../01-business-capabilities/25-card-management.md) |
| Record Authorization Hold | [Card Management](../01-business-capabilities/25-card-management.md) |
| Record Clearing Advice | [Card Management](../01-business-capabilities/25-card-management.md) |
| Release Authorization Hold | [Card Management](../01-business-capabilities/25-card-management.md) |
| Renew Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Replace Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Request Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Suspend Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Tokenize Card | [Card Management](../01-business-capabilities/25-card-management.md) |
| Update Card Controls | [Card Management](../01-business-capabilities/25-card-management.md) |
| Activate Limit | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Approve Limit | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Approve Limit Override | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Close Limit | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Define Limit Type | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Propose Limit | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Recalculate Exposure | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Record Limit Breach | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Record Utilization | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Release Exposure | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Renew Limit | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Reserve Exposure | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Suspend Limit | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Add Applicant Party | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Approve Onboarding | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Convert to Customer | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Expire Onboarding Case | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Record Screening Result | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Reject Onboarding | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Request Remediation | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Request Screening | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Start Onboarding | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Submit Evidence | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Configure Product Bundle | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Configure Product Limits | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Define Product Migration | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Migrate Product Contracts | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Simulate Product | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Supersede Product Version | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Validate Product Version | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Execute Bulk Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Recall Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Reconcile Settlement | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Register Direct Debit Mandate | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Repair Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Route Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Validate Payment | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |

## Business Events

| Business event | Capability |
|---|---|
| Accounting Period Closed | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Accrual Recognized | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Journal Generated | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Journal Posted | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Journal Reversed | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Provisioning Posted | [Accounting](../03-financial-infrastructure/09-accounting.md) |
| Backup Completed | [Administration](../05-platform-capabilities/22-administration.md) |
| Business Date Advanced | [Administration](../05-platform-capabilities/22-administration.md) |
| Maintenance Started | [Administration](../05-platform-capabilities/22-administration.md) |
| Operational Alert Raised | [Administration](../05-platform-capabilities/22-administration.md) |
| Privileged Session Terminated | [Administration](../05-platform-capabilities/22-administration.md) |
| Recovery Completed | [Administration](../05-platform-capabilities/22-administration.md) |
| Tenant Provisioned | [Administration](../05-platform-capabilities/22-administration.md) |
| Audit Export Performed | [Audit](../05-platform-capabilities/23-audit.md) |
| Audit Record Captured | [Audit](../05-platform-capabilities/23-audit.md) |
| Evidence Package Created | [Audit](../05-platform-capabilities/23-audit.md) |
| Integrity Seal Applied | [Audit](../05-platform-capabilities/23-audit.md) |
| Legal Hold Applied | [Audit](../05-platform-capabilities/23-audit.md) |
| Retention Disposal Completed | [Audit](../05-platform-capabilities/23-audit.md) |
| Business Date Advanced | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Job Completed | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Job Failed | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Job Restarted | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Job Started | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Step Completed | [Batch Processing](../05-platform-capabilities/20-batch-processing.md) |
| Collateral Liquidated | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Collateral Pledged | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Collateral Registered | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Collateral Released | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Collateral Substituted | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| LTV Threshold Breached | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Valuation Recorded | [Collateral Management](../02-policy-capabilities/14-collateral-management.md) |
| Configuration Approved | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Configuration Became Effective | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Configuration Rolled Back | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Exchange Rate Published | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Feature Flag Changed | [Configuration](../05-platform-capabilities/21-configuration.md) |
| Customer Activated | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Customer Closed | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Customer Created | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Customer Profile Changed | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Customer Transferred | [Customer Management](../01-business-capabilities/01-customer-management.md) |
| Collection Case Opened | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Contract Cured | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Contract Entered Delinquency | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Delinquency Bucket Changed | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Promise to Pay Broken | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Write-Off Eligible | [Delinquency Management](../02-policy-capabilities/13-delinquency-management.md) |
| Contribution Received | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Deposit Activated | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Deposit Matured | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Deposit Prematurely Closed | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Deposit Renewed | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Installment Missed | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Interest Posted | [Deposit Management](../01-business-capabilities/07-deposit-management.md) |
| Charge Assessed | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Charge Became Due | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Charge Capitalized | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Charge Paid | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Charge Refunded | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Charge Reversed | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Charge Waived | [Fee Engine](../02-policy-capabilities/12-fee-engine.md) |
| Balance Carried Forward | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| GL Account Activated | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Journal Posted to GL | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Period Closed | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Statement Mapping Changed | [General Ledger](../03-financial-infrastructure/15-general-ledger.md) |
| Authentication Failed | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Credential Reset | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Delegation Granted | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Role Assigned | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| User Activated | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| User Locked | [Identity & Security](../05-platform-capabilities/03-identity-and-security.md) |
| Dead Letter Created | [Integration](../05-platform-capabilities/19-integration.md) |
| External Request Received | [Integration](../05-platform-capabilities/19-integration.md) |
| Import Completed | [Integration](../05-platform-capabilities/19-integration.md) |
| Integration Failed | [Integration](../05-platform-capabilities/19-integration.md) |
| Integration Message Published | [Integration](../05-platform-capabilities/19-integration.md) |
| Webhook Delivered | [Integration](../05-platform-capabilities/19-integration.md) |
| Interest Accrued | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Interest Calculated | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Interest Posting Requested | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Interest Recalculated | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Rate Became Effective | [Interest Engine](../02-policy-capabilities/11-interest-engine.md) |
| Loan Approved | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Loan Became Delinquent | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Loan Closed | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Loan Disbursed | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Loan Rescheduled | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Loan Submitted | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Loan Written Off | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Recovery Received | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Repayment Posted | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Schedule Recalculated | [Loan Management](../01-business-capabilities/05-loan-management.md) |
| Notification Delivered | [Notification](../05-platform-capabilities/18-notification.md) |
| Notification Failed | [Notification](../05-platform-capabilities/18-notification.md) |
| Notification Requested | [Notification](../05-platform-capabilities/18-notification.md) |
| Notification Sent | [Notification](../05-platform-capabilities/18-notification.md) |
| Notification Suppressed | [Notification](../05-platform-capabilities/18-notification.md) |
| Reminder Triggered | [Notification](../05-platform-capabilities/18-notification.md) |
| Calendar Changed | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Fund Created | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Office Activated | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Office Reorganized | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Staff Assigned | [Organization Management](../01-business-capabilities/02-organization-management.md) |
| Payment Authorized | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Executed | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Initiated | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Rejected | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Returned | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Reversed | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Settled | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Business Event Published | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Command Accepted | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Document Stored | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Reference Data Changed | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Search Index Updated | [Platform Services](../05-platform-capabilities/24-platform-services.md) |
| Product Activated | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Retired | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Terms Changed | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Version Approved | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Report Distributed | [Reporting](../04-information-capabilities/16-reporting.md) |
| Report Failed | [Reporting](../04-information-capabilities/16-reporting.md) |
| Report Generated | [Reporting](../04-information-capabilities/16-reporting.md) |
| Report Requested | [Reporting](../04-information-capabilities/16-reporting.md) |
| Sensitive Export Performed | [Reporting](../04-information-capabilities/16-reporting.md) |
| Statement Produced | [Reporting](../04-information-capabilities/16-reporting.md) |
| Account Became Dormant | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Account Closed | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Deposit Posted | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Hold Placed | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Interest Posted | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Savings Account Activated | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Transaction Reversed | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Withdrawal Posted | [Savings Management](../01-business-capabilities/06-savings-management.md) |
| Dividend Allocated | [Share Management](../01-business-capabilities/08-share-management.md) |
| Dividend Declared | [Share Management](../01-business-capabilities/08-share-management.md) |
| Share Account Activated | [Share Management](../01-business-capabilities/08-share-management.md) |
| Share Account Closed | [Share Management](../01-business-capabilities/08-share-management.md) |
| Shares Issued | [Share Management](../01-business-capabilities/08-share-management.md) |
| Shares Redeemed | [Share Management](../01-business-capabilities/08-share-management.md) |
| Request Approved | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Request Rejected | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Task Assigned | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Task Escalated | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Workflow Cancelled | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Workflow Completed | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Workflow Started | [Workflow & Approval](../05-platform-capabilities/17-workflow-and-approval.md) |
| Authorization Hold Recorded | [Card Management](../01-business-capabilities/25-card-management.md) |
| Authorization Hold Released | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Activated | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Approved | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Blocked | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Closed | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Controls Changed | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Dispute Opened | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Issued | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Renewed | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Replaced | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Requested | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Suspended | [Card Management](../01-business-capabilities/25-card-management.md) |
| Card Tokenized | [Card Management](../01-business-capabilities/25-card-management.md) |
| Clearing Advice Received | [Card Management](../01-business-capabilities/25-card-management.md) |
| Exposure Recalculated | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Exposure Released | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Exposure Reserved | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Activated | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Approved | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Breached | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Closed | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Override Approved | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Proposed | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Renewed | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Suspended | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Limit Type Defined | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Utilization Recorded | [Limits and Exposure Management](../02-policy-capabilities/26-limits-and-exposure-management.md) |
| Applicant Party Added | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Customer Converted | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Evidence Submitted | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Onboarding Approved | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Onboarding Case Expired | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Onboarding Rejected | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Onboarding Started | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Remediation Requested | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Screening Requested | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Screening Result Recorded | [Customer Onboarding / KYC](../01-business-capabilities/27-customer-onboarding-and-kyc.md) |
| Product Contracts Migrated | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Draft Created | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Simulated | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Version Superseded | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Product Version Validated | [Product Catalog](../01-business-capabilities/04-product-catalog.md) |
| Bulk Payment Executed | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Direct Debit Mandate Registered | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Recalled | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Reconciled | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Repaired | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Routed | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Submitted to Scheme | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
| Payment Validated | [Payment Processing](../03-financial-infrastructure/10-payment-processing.md) |
