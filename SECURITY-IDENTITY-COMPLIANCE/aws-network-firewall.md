# AWS Network Firewall

---

## What It Is
AWS Network Firewall is a fully managed, scalable, and highly available firewall service for Amazon VPC. It provides customizable **stateful and stateless** traffic filtering, deep packet inspection, domain filtering, and centralized policy management to protect inbound, outbound, and VPC-to-VPC traffic.

---

## Key Features
• Managed, scalable, and highly available firewall service  
• Supports **stateless** and **stateful** inspection rules  
• Deep packet inspection (DPI) with **Suricata-compatible** rule sets  
• Domain list rule groups for DNS-based filtering  
• Centralized management via **AWS Firewall Manager**  
• Automatic scaling based on traffic volume  
• Logging outputs to **Amazon S3**, **CloudWatch Logs**, or **Kinesis Firehose**  
• High availability within each Availability Zone  

---

## Components
• **Firewall** – Defines policies, logging, and inspection settings  
• **Firewall Policy** – Contains rule groups and traffic handling settings  
• **Rule Groups** – Stateless and stateful rules for traffic inspection  
• **Stateless Rules** – Header-based filtering without session awareness  
• **Stateful Rules** – Track connection state for advanced filtering  
• **Domain List Rules** – Allow/deny DNS-based traffic by domain  
• **Logging Configuration** – Controls delivery of alert and flow logs  

---

## Traffic Flow
• Deployed at VPC ingress/egress or between VPCs using Transit Gateway  
• Traffic routed to firewall endpoints via route tables  
• Supports GWLB (Gateway Load Balancer) for appliance-style deployments  
• Performs inspection before routing traffic to its destination  

---

## Use Cases
• Inbound/outbound VPC traffic filtering  
• Blocking known malicious IPs or domains  
• Preventing data exfiltration  
• Deep packet inspection for malware or signature-based threats  
• Centralized firewall policy enforcement across multiple accounts  
• East–West (VPC-to-VPC) and North–South (internet-bound) traffic inspection  

---

## Deployment Options
• **VPC-level deployment** for distributed architectures  
• **Transit Gateway integration** for centralized inspection  
• **Firewall Manager integration** for multi-account enforcement  
• Automatically scales horizontally to handle throughput  
• Deploy across multiple AZs for resilience  

---

## Logging & Monitoring
• Log types: **Flow logs**, **Alert logs**  
• Destinations: **S3**, **CloudWatch Logs**, **Kinesis Firehose**  
• CloudWatch metrics for packet/byte counters  
• CloudWatch Alarms for anomaly detection and traffic monitoring  

---

## Integration with AWS Services
• **AWS Firewall Manager** – Centralized multi-account policy enforcement  
• **AWS Transit Gateway** – East–West and North–South inspection  
• **Amazon VPC** – Ingress/egress filtering  
• **AWS Security Hub** – Findings aggregation and compliance mapping  

---

## Pricing
• Billed per **firewall endpoint hour**  
• Additional charges for **traffic processing**  
• Separate pricing for **stateful and stateless** rule evaluations  
• Logging storage costs (S3, CloudWatch Logs, Firehose)

---

## Best Practices
• Use Firewall Manager for multi-account governance  
• Segment VPC architectures for better traffic control  
• Regularly update Suricata rule sets  
• Enable logging for auditing and compliance  
• Deploy firewalls across multiple AZs for HA  

---

## Exam Tips
• Network Firewall = **stateful + stateless** filtering at VPC level  
• Uses **Suricata rules** for DPI  
• Integrates with **Firewall Manager** and **Transit Gateway**  
• Ideal for centralized inspection across many VPCs  
• Logs delivered to **S3, CloudWatch Logs, Firehose**  
• Fully managed and automatically scales with traffic  

---

## Quick Summary
AWS Network Firewall is a fully managed, scalable firewall that delivers customizable stateful and stateless traffic inspection for VPCs. With Suricata rule support, deep packet inspection, domain filtering, Firewall Manager integration, and strong logging capabilities, it provides robust protection against network threats across single or multi-account AWS environments.
