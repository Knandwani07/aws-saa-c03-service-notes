# Amazon Route 53

---

## What It Is
Amazon Route 53 is a **highly available, scalable, authoritative DNS and domain registration service**. It routes end-user requests to AWS or on-premises resources, supports global traffic management, and provides DNS health checks with automatic failover.

---

## Key Features
• Authoritative DNS service  
• Domain registration (many TLDs supported)  
• Health checks + DNS failover  
• Advanced routing policies (latency, weighted, geolocation, failover, etc.)  
• Alias records for AWS integrations  
• IPv4 + IPv6 support  
• Integration with ELB, CloudFront, API Gateway, S3, Global Accelerator  

---

## Routing Policies
• **Simple Routing** – Single record → single value  
• **Weighted Routing** – Split traffic by percentage across resources  
• **Latency-based Routing** – Sends users to the region with lowest latency  
• **Failover Routing** – Active-passive HA routing  
• **Geolocation Routing** – Route based on user’s geographic origin  
• **Geoproximity Routing (Traffic Flow)** – Route based on geographic distance + bias  
• **Multivalue Answer Routing** – Return multiple healthy IPs for client-side LB  

---

## Domain Registration
• Register and manage domains directly in Route 53  
• WHOIS privacy protection  
• Auto-renew options  
• Easy integration with hosted zones  

---

## Health Checks & DNS Failover
• Monitors endpoints using HTTP/HTTPS/TCP  
• Failover to backup endpoints when primary becomes unhealthy  
• Can monitor **CloudWatch alarms**  
• Alias records support health check–based failover  

---

## Alias Records
• Route 53–specific record type  
• Points to AWS resources **without extra DNS lookup**  
• Free DNS queries for alias records  
• Supports apex/root domain  
• Works with:
  - ELB (ALB/NLB/CLB)  
  - CloudFront  
  - API Gateway  
  - S3 static websites  
  - Global Accelerator  
  - VPC endpoint services  

---

## Integration with AWS Services
• ELB → Load balancers  
• S3 → Static site hosting  
• CloudFront → CDN  
• Global Accelerator → Static IP performance routing  
• API Gateway → API endpoints  

---

## High Availability & Scalability
• Global DNS infrastructure (edge locations worldwide)  
• 100% availability SLA  
• Automatically scales to massive DNS query volumes  

---

## Security
• DNSSEC support for domain registration + hosted zones  
• IAM for access control  
• CloudTrail logs API calls  
• Private hosted zones for VPC-internal DNS resolution  

---

## Traffic Flow
• Visual editor for complex routing logic  
• Versioned traffic policies  
• Supports:
  - Geoproximity  
  - Latency  
  - Weighted  
  - Failover combinations  

---

## Private Hosted Zones
• DNS resolution **inside VPCs** only  
• Multiple VPCs can share a private hosted zone  
• Perfect for internal service discovery  

---

## Pricing
• Per hosted zone (monthly)  
• Per DNS query  
• Health checks are billed separately  
• Alias record queries to AWS endpoints = **no cost**  

---

## Use Cases
• Global DNS hosting  
• Highly available websites with DNS failover  
• Latency-optimized routing for global users  
• Load balancing with weighted records  
• Private DNS for internal microservices  
• Managing domain registration + DNS in one service  

---

## Exam Tips
• Alias records → Required for apex domain → AWS resources  
• Weighted routing → Split traffic  
• Latency-based routing → Best performance for users  
• Failover routing → Active-passive HA  
• Geolocation vs Geoproximity:
  - Geolocation → User’s location  
  - Geoproximity → Distance + bias  
• Private hosted zones → VPC-internal DNS  
• DNSSEC → Protects against spoofing  
• Route 53 integrates with ELB, CloudFront, Global Accelerator  

---

## Quick Summary
Amazon Route 53 is AWS’s global DNS and domain registration service. It provides highly available DNS resolution, advanced routing policies, alias integration with AWS resources, DNS health checks with failover, and private hosted zones—all critical for building resilient, globally distributed architectures.

