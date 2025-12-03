# AWS Security Hub

---

## What It Is
• Centralized AWS security service that **aggregates, organizes, and prioritizes security findings** from AWS services and third-party security tools.  
• Provides a **single dashboard** (“single pane of glass”) to understand and improve your AWS security posture.

---

## Key Features

### 1. Aggregated Security Findings
• Collects findings from:
  - AWS services: GuardDuty, Inspector, Macie, Firewall Manager, IAM Access Analyzer, Config  
  - Third-party partner tools (via ASFF format)  
• Normalizes all findings into **AWS Security Finding Format (ASFF)** for consistency.

### 2. Security Standards & Best Practices
• Built-in automated compliance checks for:
  - **CIS AWS Foundations Benchmark**  
  - **AWS Foundational Security Best Practices**  
  - **PCI DSS v3.2.1**  
• Flags non-compliant resources with detailed findings and remediation guidance.

### 3. Consolidated Dashboard
• Central view of:
  - Active findings  
  - Compliance results  
  - Severity trends  
• Supports filtering, grouping, and prioritization of findings.

### 4. Automated Response & Remediation
• Deep integration with **Amazon EventBridge**  
• Enables automated workflows (e.g., auto-fix public S3 buckets, close risky security groups)  
• Supports custom remediation via Lambda, Systems Manager Automation, etc.

### 5. Cross-Account & Multi-Region Aggregation
• View findings from **multiple AWS accounts** in an AWS Organization  
• Consolidate findings across **multiple regions** into a single administrator account  
• Ideal for enterprise-level security operations

---

## Integrates With
• Amazon GuardDuty  
• Amazon Inspector  
• Amazon Macie  
• AWS Firewall Manager  
• AWS IAM Access Analyzer  
• AWS Systems Manager  
• AWS Config  
• Third-party tools via ASFF  

---

## Security & Compliance
• Helps organizations meet ongoing audit and compliance requirements  
• Standardized findings include:
  - Severity  
  - Resource details  
  - Recommended remediation steps  
• Supports continuous compliance posture monitoring  

---

## Pricing
• Based on:
  - Number of **security checks** performed  
  - Volume of **ingested findings**  
• No upfront cost  

---

## Use Cases
• Centralizing security findings across accounts  
• Automating compliance checks for CIS, PCI DSS, AWS Best Practices  
• Enabling automated incident response playbooks  
• Executive-level visibility into overall AWS security posture  

---

## Exam Tips
• Security Hub = **central dashboard** aggregating AWS + partner security findings  
• Supports CIS, PCI DSS, and AWS Best Practices checks  
• Uses **ASFF (AWS Security Finding Format)**  
• Integrates with EventBridge for automated remediation  
• Multi-account & multi-region visibility via AWS Organizations  
• Not a threat detection tool—**it aggregates**, while GuardDuty detects  

---

## Quick Summary
AWS Security Hub provides a unified, automated, and comprehensive view of your AWS security posture. It aggregates findings from AWS security services and partner tools, evaluates compliance against industry standards, and enables automated remediation — making it a key service for centralized cloud security management.

