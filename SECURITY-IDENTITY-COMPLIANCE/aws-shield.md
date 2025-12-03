# AWS Shield

---

## What It Is
• Managed **Distributed Denial of Service (DDoS) protection** service for AWS workloads.  
• Protects against network/transport layer attacks (Layer 3/4) and application-layer attacks (Layer 7).  
• Provides automatic, always-on detection and mitigation for public-facing AWS resources.

---

## Key Features

### 1. AWS Shield Standard
• **Free**, enabled for all AWS customers by default.  
• Protects against common, frequently occurring DDoS attacks.  
• Automatically defends services such as:
  - Amazon CloudFront  
  - Amazon Route 53  
  - Elastic Load Balancers (ALB/NLB)  
  - AWS Global Accelerator  
• Always-on detection + inline automated mitigation.  
• No configuration required.

---

### 2. AWS Shield Advanced
• **Paid**, enhanced DDoS protection for mission-critical applications.  
• Protects against sophisticated and high-volume attacks.  
• Includes:
  - **24×7 AWS DDoS Response Team (DRT)** access  
  - Advanced, customizable attack mitigation  
  - Real-time metrics and visibility  
  - Layer 7 protections when used with AWS WAF  
  - **DDoS Cost Protection** to offset unexpected scaling charges  
  - Global threat intelligence dashboard  
  - Protection for additional resources (EIPs, EC2, Global Accelerator, CloudFront, ALB, NLB)

---

## Integrated AWS Services
• Amazon CloudFront  
• Amazon Route 53  
• AWS Global Accelerator  
• Elastic Load Balancers (ALB/NLB)  
• EC2 with Elastic IPs  
• AWS edge infrastructure  

---

## Pricing
• **Shield Standard**: Free for all customers.  
• **Shield Advanced**: Monthly subscription + additional data transfer-related costs.

---

## Security & Compliance
• Minimizes downtime, latency, and performance degradation during DDoS attacks.  
• Helps meet compliance frameworks requiring resilience and availability.  
• Supports audits with detailed attack diagnostics (Shield Advanced).

---

## AWS Shield vs AWS WAF
| Service | Purpose |
|--------|---------|
| **AWS Shield** | DDoS protection (L3/L4 + some L7) |
| **AWS WAF** | Application-layer filtering & custom rules (L7) |

**Used together:**  
• Shield Advanced mitigates DDoS → WAF filters malicious HTTP/S traffic.

---

## Use Cases
• Protect high-availability websites from DDoS attacks.  
• Prevent downtime and service degradation for public applications.  
• Reduce financial risk during large-scale attacks.  
• Meet regulatory or business continuity requirements.

---

## Exam Tips
• Shield Standard = **free**, automatic DDoS protection for all AWS customers.  
• Shield Advanced = **paid**, offers:
  - 24/7 DDoS Response Team  
  - Cost protection  
  - Real-time attack visibility  
  - Extended L7 protection with WAF  
• Shield integrates deeply with CloudFront, Route 53, and ALB/NLB.  
• For strong L7 protection, **pair Shield Advanced with WAF**.

---

## Quick Summary
AWS Shield delivers managed DDoS protection to keep your applications highly available and resilient. Shield Standard provides free baseline protection, while Shield Advanced offers enterprise-grade DDoS defenses including expert support, detailed analytics, and cost protection—for mission-critical workloads.

