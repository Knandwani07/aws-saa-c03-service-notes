# AWS Direct Connect

---

## What It Is
AWS Direct Connect is a **dedicated, private network connection** between your on-premises environment and AWS. It bypasses the public internet, offering **lower latency, higher reliability, predictable performance, and reduced data transfer costs**.

---

## Key Features
• Dedicated connectivity from on-prem to AWS  
• Low latency and consistent network performance  
• Port speeds ranging **from 50 Mbps up to 100 Gbps**  
• Traffic stays off the public internet for better security  
• Integrates with VPC using **Virtual Interfaces (VIFs)**  

---

## Connection Types

### **Dedicated Connections**
• Provisioned directly from AWS  
• Available at **1 Gbps, 10 Gbps, and 100 Gbps**  
• Delivered at AWS Direct Connect locations  

### **Hosted Connections**
• Provisioned via AWS Direct Connect Partners  
• Speed options from **50 Mbps to 10 Gbps**  
• Faster provisioning without needing your own hardware  

---

## Virtual Interfaces (VIFs)

### **Private VIF**
• Connects to VPC (VGW or Transit Gateway)  
• For accessing AWS private resources  

### **Public VIF**
• Access AWS public endpoints with AWS public IPs  
• Used for S3, DynamoDB, AWS APIs  

### **Transit VIF**
• Connects to **Transit Gateway**  
• Scales to support thousands of VPCs  

---

## Link Aggregation Groups (LAG)
• Combine multiple same-speed connections into one  
• Improves bandwidth and provides redundancy  
• Up to **4 connections** in a single LAG  
• Managed as one logical interface  

---

## Redundancy and Resiliency
• Recommended to deploy **redundant connections**  
• Use multiple Direct Connect locations for HA  
• Combine Direct Connect + VPN for backup over internet  
• SLA applies only when redundancy best practices are followed  

---

## Direct Connect Gateway
• Connect one Direct Connect connection to **multiple VPCs** across AWS Regions  
• Works globally (except China Regions)  
• Simplifies network architecture in multi-region deployments  

---

## Billing and Pricing
• Charged per **port-hour** based on connection speed  
• **Outbound data transfer** is cheaper compared to internet  
• **Inbound data transfer is free**  
• LAG billed as combined port hours  

---

## Use Cases
• High-volume data transfers (analytics, backups, migrations)  
• Hybrid architectures needing consistent latency  
• Financial services, gaming, and real-time workloads  
• Private access to AWS resources  
• Multi-region VPC connectivity via Direct Connect Gateway  

---

## Security
• Traffic never touches the public internet  
• Supports **MACsec encryption** (where available)  
• Can combine with VPN for encrypted, redundant paths  
• IAM controls access and auditing  

---

## Integration with AWS Services
• Amazon VPC  
• AWS Transit Gateway  
• Direct Connect Gateway  
• AWS VPN  
• Amazon CloudWatch (monitoring)  

---

## Exam Tips
• Direct Connect = **private, dedicated connection** to AWS  
• **Private VIF** → access VPC; **Public VIF** → access AWS public endpoints  
• Direct Connect Gateway = **multi-region VPC connection**  
• Redundancy recommended for SLA compliance  
• Can combine with VPN for **secure hybrid failover**  
• LAG = combine links for **more bandwidth + redundancy**  
• Outbound data transfer is **cheaper** than internet routing  

---

## Quick Summary
AWS Direct Connect provides **high-bandwidth, stable, and private connectivity** between on-premises and AWS. It improves performance, lowers costs, and integrates with services like VPC, Transit Gateway, and Direct Connect Gateway for flexible hybrid cloud architectures—ideal for enterprises that need speed, security, and reliability.

