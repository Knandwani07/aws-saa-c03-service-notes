# AWS Service Catalog

---

## What It Is

AWS Service Catalog helps organizations create, manage, and distribute curated collections of approved AWS infrastructure “products” (CloudFormation stacks, apps, templates). Administrators define what is allowed; end-users get governed self-service provisioning with guardrails and constraints.

---

## Key Features

• Standardization of approved infrastructure via CloudFormation-based products  
• Self-service product discovery and launch with restricted parameters  
• Fine-grained governance using IAM + launch/template/tag constraints  
• Product versioning with active/inactive states  
• Portfolio sharing across multiple AWS accounts  
• Integration with AppRegistry for application metadata tracking  

---

## Core Concepts

### Product  
A CloudFormation template (or AWS Marketplace package) defining one or more AWS resources.

### Portfolio  
A collection of products with access rules, constraints, and inherited tags.

### Versions  
Multiple versions per product; admins control which are active or deprecated.

### Constraints  
• **Template constraints:** Restrict parameter inputs  
• **Launch constraints:** Define IAM role used during provisioning  
• **Notification constraints:** SNS notifications on stack events  
• **Tag update constraints:** Control tag modification by end-users  

### Service Actions  
Optional actions (e.g., SSM documents) that users can run on provisioned products.

### AppRegistry Integration  
Associate products and stacks with applications for metadata visibility and governance.

---

## Security, Governance & Cost

• IAM controls who can create/edit portfolios and who can launch products  
• Encryption at rest (S3, DynamoDB) and TLS for in-transit data  
• CloudTrail logging for all API operations  
• Pricing: Free for first 1,000 API calls/month; additional calls billed  
• Costs apply for underlying AWS resources deployed via CloudFormation  

---

## Use Cases

• Standardizing infrastructure deployments for developers across large organizations  
• Enforcing guardrails (networking, instance types, tagging, constraints)  
• Multi-account setups where approved portfolios must be shared organization-wide  
• Managing metadata and tracking applications via AppRegistry  
• Enabling governed self-service provisioning for DevOps teams  

---

## Best Practices

• Organize portfolios by environment or team  
• Use launch and template constraints to enforce compliance and cost control  
• Version products instead of editing in place; migrate old versions carefully  
• Tag portfolios and propagate tags to underlying resources  
• Integrate Service Catalog into CI/CD workflows for automated updates  
• Monitor usage and ensure products align with governance rules  

---

## Exam Tips

• CloudFormation = IaC  
• **Service Catalog = governance + distribution of IaC**  
• Look for keywords: “approved products,” “standard stacks,” “self-service with restrictions,” “multi-account distribution”  
• Know key terms: Product, Portfolio, Constraint, Version, Provisioned Product  
• Strong answer when the scenario combines **self-service + standardization + governance**  

---

## Quick Summary

AWS Service Catalog lets admins create and govern approved infrastructure products while enabling end-users to deploy them through controlled, self-service workflows. It enforces consistency, compliance, and cost governance across single or multi-account AWS environments ideal when the requirement emphasizes standardized, governed infrastructure provisioning.

