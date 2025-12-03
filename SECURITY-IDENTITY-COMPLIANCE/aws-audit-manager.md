# AWS Audit Manager

---

## What It Is
AWS Audit Manager is a fully managed service that **automates evidence collection**, helping organizations assess AWS resource usage against compliance standards. It reduces manual audit effort, supports continuous monitoring, and keeps your environment audit-ready.

---

## Key Features
• Automated evidence collection across AWS services  
• Prebuilt frameworks for major compliance standards (CIS, GDPR, PCI DSS, HIPAA, SOC 2)  
• Create custom frameworks for internal or industry-specific needs  
• Maps AWS resources and configurations directly to compliance controls  
• Continuous compliance monitoring  
• Secure, organized evidence storage for auditors  

---

## Assessment Frameworks
• Prebuilt frameworks for compliance (HIPAA, PCI DSS, CIS, ISO 27001, GDPR, etc.)  
• Customizable frameworks for internal governance  
• Controls define evidence to collect and how it is evaluated  
• Automatic mapping of AWS resources to controls ensures relevant evidence capture  

---

## Assessments
• Assessments are created from frameworks  
• Scope defined by selecting AWS accounts, services, and controls  
• Automated evidence collection based on controls  
• Continuous assessments show ongoing compliance posture rather than point-in-time snapshots  

---

## Evidence Collection
• Automated evidence from AWS Config, CloudTrail, Security Hub, and other services  
• Manual evidence upload for external or custom requirements  
• Time-stamped evidence grouped by control for easy auditor access  
• Supports exporting evidence to Amazon S3  
• Includes configuration data, policies, logs, and API activity  

---

## Continuous Auditing
• Monitors environments continuously for compliance drift  
• Identifies noncompliant changes as they occur  
• Reduces last-minute audit rush  
• Enables early remediation of compliance issues  

---

## Integrations
• **AWS Organizations** → Multi-account assessments  
• **AWS CloudTrail** → API activity logging  
• **AWS Config** → Configuration tracking  
• **AWS Security Hub** → Security findings  
• **Amazon S3** → Evidence storage and exports  

---

## Security and Access Control
• Evidence encrypted at rest and in transit  
• IAM-based access control for assessments and evidence  
• KMS support for encryption key management  
• Fine-grained access for auditors, reviewers, and team members  

---

## Reporting and Exporting
• Generate downloadable evidence reports  
• Export all evidence to S3 in structured folders by control/assessment  
• Share with external auditors without exposing AWS accounts  

---

## Supported Compliance Frameworks
• PCI DSS  
• CIS AWS Foundations Benchmark  
• HIPAA  
• GDPR  
• SOC 2  
• ISO 27001  
• Custom frameworks  

---

## Pricing
• Billed **per active assessment per month**  
• Additional S3 storage costs apply for retained evidence  
• Pricing depends on volume of collected evidence and assessment scope  

---

## Use Cases
• Preparing for external audits (SOC 2, PCI DSS, ISO 27001, HIPAA)  
• Automating compliance evidence collection  
• Continuous compliance monitoring in multi-account setups  
• Internal risk and security assessments  
• Improving audit readiness by organizing and standardizing evidence  

---

## Exam Tips
• AWS Audit Manager automates compliance evidence gathering  
• Supports prebuilt + custom frameworks  
• Integrates with Config, CloudTrail, Security Hub for automated evidence  
• Evidence is time-stamped, encrypted, and exportable  
• Designed for continuous compliance, not just one-time audits  
• Works seamlessly with AWS Organizations  
• IAM + KMS secure access and encryption  

---

## Quick Summary
AWS Audit Manager simplifies risk and compliance processes by automating evidence collection, providing prebuilt and customizable frameworks, and enabling continuous audit readiness. It securely organizes and exports evidence, reducing manual work and making audits faster, easier, and more reliable.

