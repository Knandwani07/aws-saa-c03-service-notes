# AWS Backup

---

## What It Is
AWS Backup is a fully managed service that centralizes, automates, and monitors backups across AWS services and on-premises environments. It provides policy-based scheduling, secure backup vaults, compliance reporting, and cross-region/cross-account backup capabilities.

---

## Key Features
• Centralized backup automation and management  
• Policy-driven backup plans with schedules and retention rules  
• Encrypted backup vaults with fine-grained access control  
• Cross-region and cross-account backup replication  
• Backup activity monitoring, reporting, and auditing  
• AWS Organizations integration for multi-account governance  
• Hybrid backup support via AWS Storage Gateway  
• Backup Vault Lock for immutable WORM backups  

---

## Supported AWS Services
• Amazon EBS  
• Amazon RDS (including Aurora)  
• DynamoDB  
• Amazon EFS  
• Amazon FSx  
• Amazon EC2  
• AWS Storage Gateway volumes  
• VMware Cloud on AWS via Gateway  

---

## Backup Plans
• Define automated schedules and backup frequency  
• Use tags to include resources automatically  
• Lifecycle rules for warm → cold storage transitions  
• Retention policies to manage data lifecycle  
• Standardized backup orchestration across accounts  

---

## Backup Vaults
• Logical containers storing backups  
• Encrypted using AWS KMS keys  
• IAM-based access control  
• Cross-account sharing support  
• **Vault Lock** enforces Write-Once-Read-Many (WORM) immutability  

---

## Lifecycle Management
• Automate cold storage transition for older backups  
• Auto-expire backups to control storage costs  
• Improve compliance with structured retention timelines  

---

## Cross-Region & Cross-Account Backup
• Replicate backups to other AWS Regions for disaster recovery  
• Share or copy backups across AWS accounts  
• Strengthens resilience and compliance for mission-critical workloads  

---

## Monitoring & Reporting
• Job status, activity logs, failures, and history in AWS Backup console  
• CloudTrail logs all backup API activity  
• CloudWatch logs + metrics + alarms  
• Compliance reports showing coverage and adherence to plans  

---

## AWS Organizations Integration
• Centralized backup policy enforcement  
• Delegated admin to manage organization-wide backup settings  
• Apply templates and best practices at scale  

---

## Security & Encryption
• KMS-based encryption at rest  
• TLS encryption in transit  
• IAM roles/policies for access governance  
• Vault Lock protects against deletes and tampering  

---

## Pricing
• Based on backup storage (warm + cold tiers)  
• Charges for lifecycle transitions to cold storage  
• Additional cost for cross-region copy operations  
• Pay-as-you-go, no upfront commitments  

---

## Use Cases
• Automated, centralized backups for cloud workloads  
• Cross-region DR strategy  
• Compliance enforcement (e.g., HIPAA, PCI, SOX)  
• Hybrid backup for on-prem workloads via Storage Gateway  
• Immutable backups for ransomware defense  

---

## Best Practices
• Tag all resources for automatic backup inclusion  
• Use Vault Lock for high-security or regulatory workloads  
• Enable cross-region replication for DR  
• Monitor using CloudWatch + CloudTrail  
• Test restore procedures regularly  

---

## Exam Tips
• AWS Backup = centralized backup + automation across AWS services  
• Vault Lock enables WORM, tamper-proof retention  
• Supports cross-region and cross-account replication  
• Backup Vaults store encrypted snapshots with access control  
• Fully integrated with AWS Organizations for governance  
• CloudWatch + CloudTrail provide visibility and auditability  

---

## Quick Summary
AWS Backup offers centralized, policy-driven, secure backup management across AWS and on-prem environments. It features encrypted vaults, immutable backups, lifecycle automation, cross-region/cross-account replication, compliance reporting, and integrated multi-account governance ensuring resilient, compliant, and automated data protection at scale.

