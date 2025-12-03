# Amazon Inspector

---

## What It Is
Amazon Inspector is a fully managed, automated vulnerability management service that continuously scans AWS workloads—EC2 instances, ECR container images, and Lambda functions—for software vulnerabilities and unintended network exposure. It helps maintain security posture and compliance by identifying, prioritizing, and recommending fixes for risks.

---

## Key Features

### Automated, Continuous Scanning
• Continuously detects:  
  – OS vulnerabilities (CVEs)  
  – Application-level vulnerabilities  
  – Network exposure to the internet  
  – Container image vulnerabilities in Amazon ECR  
  – Lambda function code vulnerabilities  

### Deep AWS Integration

#### EC2
• Scans installed packages and OS  
• Assesses network reachability (public exposure)

#### Amazon ECR
• Automatically scans container images  
• Continuous scanning on image push

#### AWS Lambda
• Scans function code packages for known vulnerabilities  

### Findings and Scoring
• Generates detailed findings including:  
  – CVE information  
  – CVSS-based severity score  
  – Recommended remediation instructions  
• Findings prioritized based on exploitability and exposure

### AWS Organizations Integration
• Central management of vulnerability scans across multiple accounts  
• Unified findings and reporting  

### Automated Remediation Workflows
• Findings can be sent to:  
  – AWS Security Hub  
  – Amazon EventBridge  
  – Custom automation pipelines (e.g., auto patching, ticket creation)  

---

## Key Benefits
• Fully automated, no manual setup or scheduling  
• Continuous vulnerability monitoring  
• Integrated with developer and CI/CD workflows  
• Helps meet compliance requirements (PCI DSS, CIS, etc.)  

---

## Pricing
• Pay-as-you-go model based on:  
  – EC2 instance scans  
  – ECR container image scans  
  – Lambda function scans  
• No upfront costs  

---

## Use Cases
• Ensuring EC2 instances are patched for latest CVEs  
• Scanning container images prior to production deployment  
• Identifying vulnerable Lambda dependencies  
• Meeting enterprise and regulatory security requirements  

---

## Security & Compliance
• Supports continuous vulnerability management  
• Integrates with AWS Security Hub for central visibility  
• Encourages proactive remediation across workloads  

---

## Exam Tips
• Inspector = **vulnerability scanning**, not threat detection  
• Scans EC2, ECR container images, and Lambda functions  
• Findings include CVE data, severity, remediation  
• Fully automated—no manual assessments  
• Integrates with Security Hub, EventBridge, and Organizations  

---

## Quick Summary
Amazon Inspector is an automated vulnerability management service that continuously scans EC2 instances, container images, and Lambda functions for software vulnerabilities and network exposure, offering prioritized findings and remediation guidance to maintain security and compliance across your AWS workloads.

