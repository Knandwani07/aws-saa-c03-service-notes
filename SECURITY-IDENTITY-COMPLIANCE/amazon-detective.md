# Amazon Detective

---

## What It Is
Amazon Detective is a fully managed security investigation service that automatically collects, correlates, and analyzes security data from AWS logs and threat detection tools. It uses ML, statistics, and graph-based analytics to help you investigate suspicious activities and security incidents faster.

---

## Key Features
• Automatic ingestion of CloudTrail, VPC Flow Logs, GuardDuty findings, and Security Hub data  
• Builds a **behaviour graph** that maps relationships between AWS resources and events  
• Interactive visualizations for EC2 instances, IAM users/roles, IP addresses, accounts, and more  
• Retains up to **12 months** of historical security data  
• No agents, sensors, or custom log pipelines required  
• Helps quickly identify root causes and trace attacker behaviour  
• Continuously updates as new activity occurs  
• Tight integration with GuardDuty for investigation of security findings  

---

## How It Works
• Ingests logs from supported AWS sources  
• Normalizes and links the data into a graph model  
• Surfaces entities (IAM users, EC2 instances, IPs, etc.) and all their relationships  
• Investigators can browse entity profiles, timelines, activity heatmaps, and relationships  
• Provides comparisons of normal vs anomalous behaviour over time  

---

## Supported Data Sources
• AWS CloudTrail (API activity)  
• Amazon VPC Flow Logs (network metadata)  
• Amazon GuardDuty (threat detection findings)  
• AWS Security Hub (security alerts and context)  

---

## Entity Types Analysed
• AWS accounts  
• IAM users and roles  
• EC2 instances  
• IP addresses  
• Kubernetes clusters (when using GuardDuty for EKS)  

---

## Security Use Cases
• Investigate suspicious logins or unauthorized access  
• Trace lateral movement across EC2 or Kubernetes workloads  
• Diagnose unusual network behavior seen in VPC Flow Logs  
• Validate misconfigurations or privilege escalation attempts  
• Review pre-event and post-event behaviour for GuardDuty findings  
• Identify long-term behavioural anomalies and persistent threats  

---

## Access and Permissions
• Integrates with AWS Organizations for multi-account investigations  
• Delegated administrator account can view behaviour across all member accounts  
• IAM policies control access to Detective data and dashboards  
• CloudTrail logs all API activity for auditing  

---

## Pricing
• Billed based on the **volume of ingested data** from CloudTrail, VPC Flow Logs, and GuardDuty  
• No charge for queries, visualizations, or analysis  
• Includes automatic 12-month data retention  

---

## Best Practices
• Enable **GuardDuty + Detective** together for full detection + investigation workflow  
• Use with **Security Hub** to centralize security findings  
• Provide read-only roles to security analysts  
• Monitor IAM users, EC2 instances, and critical resources regularly  
• Use time-based comparisons to identify deviations in behaviour  

---

## Exam Tips
• Detective is for **investigation**, not detection  
• Uses **behaviour graphs** built from CloudTrail, VPC Flow Logs, GuardDuty  
• Helps identify root cause and relationships between entities  
• Automatically ingests and correlates data — no manual data collection  
• Complements GuardDuty and Security Hub, doesn’t replace them  
• Not real-time alerting → it’s a post-alert analysis tool  

---

## Quick Summary
Amazon Detective simplifies security investigations by automatically building a behaviour graph from CloudTrail, VPC Flow Logs, and GuardDuty findings. It provides interactive visualizations that reveal relationships, anomalies, and root causes, helping security teams investigate faster and more accurately without manual log analysis.

