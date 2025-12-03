# AWS Secrets Manager

---

## What It Is
• Managed AWS service for **securely storing, managing, and retrieving secrets** such as database credentials, API keys, OAuth tokens, and more.  
• Provides **automatic rotation**, **fine-grained access controls**, **audit logging**, and **runtime retrieval** to eliminate hardcoded secrets.

---

## Key Features

### 1. Secure Storage
• Secrets encrypted at rest using **AWS KMS**  
• Supports customer-managed CMKs  
• Secrets are encrypted automatically on creation

### 2. Automatic Rotation
• Built-in **automatic rotation** via AWS Lambda  
• Prebuilt rotation templates for **RDS, Aurora, Redshift**  
• Zero-downtime rotation supported  

### 3. Fine-Grained Access Control
• IAM policies + resource-based policies to restrict access  
• IAM condition keys allow partial access to specific secret fields  

### 4. Audit & Monitoring
• Integrated with **AWS CloudTrail** to log every read/write action  
• CloudWatch metrics & alarms for activity monitoring  

### 5. Cross-Account Access
• Supported via resource-based policies  
• Useful in multi-account environments  

### 6. SDK & CLI Integration
• Retrieve secrets at runtime using:
  - AWS SDKs  
  - AWS CLI  
  - Secrets Manager API  
• Eliminates hardcoded credentials in code or environment variables

---

## Use Cases
• Secure, auto-rotated **RDS database credentials**  
• Replace **hardcoded secrets** in applications  
• Manage **third-party API keys**  
• Share secrets between **multiple AWS accounts/environments**  

---

## Secrets Manager vs Parameter Store

| Feature | Secrets Manager | Parameter Store (Standard Tier) |
|--------|-----------------|---------------------------------|
| Rotation | **Automatic (Lambda-integrated)** | Manual |
| Secret Types | Sensitive secrets | Config + secrets |
| Pricing | Paid | Standard = Free, Advanced = Paid |
| API Rate Limit | High throughput | Lower |
| Encryption | KMS | KMS |

---

## Security
• Secrets encrypted with **AWS KMS**  
• IAM policies + resource policies control access  
• Rotation handled by Lambda functions  
• CloudTrail logs all access attempts  

---

## Pricing
• Cost per **secret stored per month**  
• Cost per **10,000 API calls**  
• Lambda rotation functions billed separately  

---

## Exam Tips
• Use **Secrets Manager** when you need **automatic secret rotation**  
• Never hardcode secrets—retrieve via API/SDK  
• Parameter Store is cheaper for non-critical configs  
• Secrets Manager integrates directly with **RDS** for rotation  
• Access is controlled by **IAM + resource policies**  
• KMS handles encryption and key management  

---

## Quick Summary
AWS Secrets Manager securely stores and automatically rotates sensitive secrets such as API keys and database credentials. It provides encryption with KMS, IAM access control, CloudTrail auditing, seamless application integration, and cross-account sharing—making it ideal for secure secret lifecycle management in modern AWS architectures.

