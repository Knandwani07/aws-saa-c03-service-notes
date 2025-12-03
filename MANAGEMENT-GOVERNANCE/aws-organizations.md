# AWS Organizations

---

## What It Is

AWS Organizations is a free service that lets you centrally govern, secure, and manage multiple AWS accounts at scale. It provides consolidated billing, policy-based controls, and an organizational structure for enforcing governance across accounts.

---

## Key Benefits

• Centralized billing and cost management  
• Simplified account creation and lifecycle management  
• Policy-based governance using Service Control Policies (SCPs)  
• Organize accounts into Organizational Units (OUs)  
• Enforce consistent security and compliance  
• Integrates with AWS Control Tower, IAM Identity Center, AWS RAM, and more  

---

## Core Concepts

### 1. Organization
• A collection of AWS accounts under a single management account  
• Can include hundreds or thousands of member accounts  

### 2. Management Account
• Formerly the “Master Account”  
• Full control over the organization  
• Pays the consolidated bill for all member accounts  

### 3. Member Accounts
• Accounts that belong to the organization  
• Managed and restricted via policies applied by the management account  

### 4. Organizational Units (OUs)
• Logical groupings of accounts  
• Can be nested hierarchically  
• SCPs can be applied at OU level for broad governance  

---

## Features and Capabilities

### Consolidated Billing
• Single bill for all accounts  
• Share volume discounts across accounts  
• Track usage at both org and account level  
• No extra cost  

### Service Control Policies (SCPs)
• Define maximum permissions allowed for accounts/OUs  
• Work with IAM: SCP = boundary, IAM = permissions  
• Can allow/deny AWS actions and services  
• Default is FullAWSAccess  
• Examples: deny specific regions, block resource deletion  

### IAM Identity Center (AWS SSO) Integration
• Centralized access management across accounts  
• Assign user roles and permissions  
• Supports SAML and external identity providers  

### Account Creation and Invitation
• Create accounts programmatically or via console  
• Invite existing standalone accounts  
• Enforce governance on join  

### Tagging Support
• Tag AWS accounts for cost allocation and tracking  

---

## Policy Types

• **Service Control Policies (SCPs)** – restrict allowed services/actions  
• **Tag Policies** – enforce consistent resource tagging  
• **Backup Policies** – enforce AWS Backup configurations org-wide  
• **AI Services Opt-Out Policies** – control ML data usage by AWS AI services  

---

## Integration with AWS Services

• **AWS Control Tower** – builds landing zones on top of Organizations  
• **AWS Resource Access Manager (RAM)** – share resources across accounts  
• **AWS Budgets** – track org-level spending  
• **AWS Config** – aggregate configuration data  
• **AWS CloudTrail** – centralized logging for all accounts  

---

## Security and Access Control

• SCPs enforce organization-wide permission guardrails  
• IAM policies operate within SCP boundaries  
• Management account controls all OUs and accounts  
• CloudTrail records org-level API activity  

---

## Best Practices

• Structure OUs by environment (prod/dev/test)  
• Apply SCPs using least privilege principles  
• Enable consolidated billing to maximize volume discounts  
• Enforce Tag Policies for consistency  
• Aggregate and audit with Config + CloudTrail  
• Use AWS Budgets for cost governance  

---

## Pricing

• AWS Organizations is free  
• You only pay for services used by member accounts  
• No charge for consolidated billing or policy enforcement  

---

## Limitations

• SCPs restrict permissions but do not grant them  
• Some AWS services don’t fully support all Organizations features  
• SCP changes take effect immediately  
• An AWS account can belong to only one organization  

---

## Common Use Cases

• Multi-account governance for large organizations  
• Centralized security enforcement using SCPs  
• Isolated dev/test/prod accounts  
• Cost allocation and shared billing  
• Cross-account resource sharing via AWS RAM  

---

## Exam Tips

• SCPs = permission boundaries (NOT permissions)  
• Management account = full administrative control  
• Consolidated billing = shared discounts + centralized invoicing  
• OUs apply policies to groups of accounts  
• Integrates with Control Tower, RAM, IAM Identity Center  
• Tag Policies enforce standardized tagging org-wide  
• Backup Policies automate backups across accounts  

---

## Quick Summary

AWS Organizations lets you centrally manage, secure, and govern multiple AWS accounts using OUs, SCPs, consolidated billing, and integrations with AWS Control Tower, IAM Identity Center, and AWS RAM. It provides enterprise-wide governance, cost control, and consistent security across environments.

