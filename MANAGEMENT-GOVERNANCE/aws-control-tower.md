# AWS Control Tower

---

## What It Is

AWS Control Tower is a fully managed service that helps you set up and govern a secure, multi-account AWS environment following AWS best practices. It automates account provisioning, enforces governance controls, and simplifies compliance through a preconfigured landing zone.

---

## Key Benefits

• Automated landing zone setup for multi-account environments  
• Applies guardrails for governance and compliance  
• Simplifies account provisioning with Account Factory  
• Integrates with AWS Organizations, AWS Config, Service Catalog, and CloudTrail  
• Enables centralized monitoring and policy enforcement  

---

## Core Concepts

### 1. Landing Zone

A preconfigured, secure AWS environment based on AWS best practices.

• Centralized logging  
• Account structure (management, audit, log archive accounts)  
• Networking configuration  
• Security baselines  

### 2. Account Factory

• Tool within Control Tower for automated account creation and provisioning  
• Uses AWS Service Catalog to deliver account blueprints  
• Customizes VPC settings, Region selections, and other options  

### 3. Guardrails

• Predefined governance policies that enforce rules or monitor compliance  

Two types:  
o Preventive – Uses Service Control Policies (SCPs) to block non-compliant actions  
o Detective – Uses AWS Config rules to detect and report violations  

Examples:  
o Prevent use of unapproved regions  
o Ensure CloudTrail is enabled  
o Require MFA for root users  

---

## Architecture Overview

• Built on top of:  
o AWS Organizations – account hierarchy management  
o Service Catalog – backend for Account Factory  
o CloudTrail – records activity logs  
o AWS Config – compliance tracking  
o CloudWatch & SNS – monitoring and notifications  

• Standard Accounts Created:  
o Management Account – central admin and billing  
o Audit Account – read-only access across accounts  
o Log Archive Account – centralized storage for logs  

---

## Account Structure

• Organizational Units (OUs) group accounts (e.g., dev, test, prod)  
• Guardrails applied at OU level  
• New accounts provisioned directly into designated OUs  

---

## Customizations for Control Tower (CfCT)

• Framework for extending and customizing the landing zone  
• Deploy CloudFormation templates across accounts and OUs  
• Supports lifecycle management for custom resources  

---

## Integration and Extension

• AWS Config Aggregator – centralized compliance view  
• CloudTrail Lake – centralized activity log analytics  
• IAM Identity Center – centralized workforce authentication  
• Support for custom SCPs beyond built-in guardrails  

---

## Security and Compliance

• IAM policies, SCPs, and Config rules enforce governance  
• Automatically configures:  
o CloudTrail logs stored in Log Archive account  
o AWS Config enabled across accounts  

• Helps satisfy compliance frameworks (CIS, NIST, etc.)  

---

## Use Cases

• Setting up multi-account AWS environments following best practices  
• Enforcing consistent security baselines  
• Governance for enterprises and regulated industries  
• Automated provisioning for dev/test/prod environments  

---

## Pricing

• Free to use Control Tower  
• You pay for underlying services used:  
o CloudTrail  
o AWS Config  
o S3  
o AWS Lambda  
o Other deployed resources  

---

## Limitations

• Limited SCP/guardrail customization in the console  
• Guardrails only apply to enrolled accounts  
• Some AWS Regions may not be supported  
• Some AWS services may not be aware of Control Tower  

---

## Exam Tips

• Landing Zones, Guardrails, and Account Factory are core pillars  
• Preventive guardrails = SCPs; detective guardrails = Config rules  
• Account Factory is built on AWS Service Catalog  
• Logs and compliance data stored in Log Archive and Audit accounts  
• Works closely with AWS Organizations  
• Know the three key accounts: Management, Audit, Log Archive  
• CfCT is used for advanced customizations  

---

## Quick Summary

AWS Control Tower provides automated setup, governance, and compliance for multi-account AWS environments through landing zones, guardrails, and account factory. It centralizes logging, enforces security baselines, and integrates tightly with AWS Organizations, IAM Identity Center, AWS Config, and CloudTrail to streamline large-scale cloud governance.

