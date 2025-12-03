# Amazon GuardDuty

---

## What It Is
Amazon GuardDuty is a fully managed threat detection service that continuously monitors AWS accounts, workloads, and data for malicious or unauthorized activity using machine learning, anomaly detection, and integrated threat intelligence.

---

## Key Features

### 1. Continuous Threat Detection
• Monitors for:  
  – Unauthorized API calls  
  – Reconnaissance (port scanning, unusual logins)  
  – Malware activity  
  – Data exfiltration attempts  
  – Crypto-mining behaviour  

### 2. Data Sources Analysed
• **VPC Flow Logs** – network traffic analysis  
• **AWS CloudTrail Logs** – API activity monitoring  
• **DNS Logs** – domain lookup anomalies  
• **Kubernetes Audit Logs** – EKS cluster behaviour  
• **Malware Scanning** (optional) – scans EBS volumes for malware  

### 3. Threat Intelligence Feeds
• AWS threat intelligence  
• Third-party intel feeds  
• Detects known malicious IPs, domains, behaviours  

### 4. Findings
• Findings describe suspicious activity  
• Categorized into Low, Medium, High severity  
• Include remediation recommendations  

### 5. Security Hub Integration
• Findings sent to AWS Security Hub for unified visibility  
• Integrates with Amazon EventBridge for automation and alerts  

---

## Key Benefits
• Fully managed—no infrastructure or agents required  
• Continuous monitoring without affecting workload performance  
• Multi-account support via AWS Organizations  
• Actionable insights based on behavioural analytics and threat intel  

---

## Pricing
• Pay-as-you-go  
• Based on volume of:  
  – CloudTrail events analysed  
  – VPC Flow Logs analysed  
  – DNS requests analysed  
• Malware scans billed per GB scanned  
• No upfront cost or commitments  

---

## Use Cases
• Detect compromised EC2 instances running crypto-miners  
• Identify unusual API activity indicating account compromise  
• Detect data exfiltration attempts or DNS tunneling  
• Centralized threat monitoring for multi-account setups  

---

## Security & Compliance
• Supports AWS Organizations for centralized monitoring  
• Findings routed to CloudWatch Events / EventBridge  
• Helps satisfy compliance requirements for continuous monitoring  

---

## Exam Tips
• GuardDuty = **threat detection**, not a firewall or prevention tool  
• Analyses CloudTrail, VPC Flow Logs, DNS logs, and Kubernetes audit logs  
• No agents required  
• Integrates with Security Hub + EventBridge  
• Findings include severity and remediation guidance  
• Pricing based on analysed log volume  

---

## Quick Summary
Amazon GuardDuty is a managed threat detection service that continuously analyses AWS logs and network behaviour to identify malicious activity using machine learning and threat intelligence. It provides actionable security findings with no agents or infrastructure to manage, making it ideal for continuous monitoring across AWS environments.

