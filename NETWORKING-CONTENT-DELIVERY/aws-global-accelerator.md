# AWS Global Accelerator

---

## What It Is
AWS Global Accelerator is a global networking service that improves **performance, availability, and resilience** for applications by routing traffic over the AWS global backbone instead of the public internet.

---

## Key Features
• Provides **two static IPs** that act as a fixed entry point  
• Routes TCP & UDP traffic over AWS’s private network  
• Automatic health checks + instant failover  
• Improves global latency via AWS edge locations  
• Supports traffic shifting and multi-region architectures  

---

## How It Works
1. Users connect to the **static IPs** of the accelerator  
2. Traffic enters the closest AWS **edge location**  
3. Routed across AWS backbone to the optimal region  
4. Health checks ensure only healthy endpoints receive traffic  
5. Automatic rerouting during failures  

---

## Static IP Addresses
• Accelerator creates **two static IPs** in different network zones  
• Option to **bring your own IP (BYOIP)**  
• Simplifies firewall whitelisting and DNS configuration  

---

## Core Components

### **Accelerator**
• Top-level resource  
• Includes one or more listeners  

### **Listener**
• Defines allowed ports & protocols (TCP/UDP)  
• Each listener sends traffic to one or more endpoint groups  

### **Endpoint Group**
• Mapped to a specific **AWS Region**  
• Contains endpoints + health checks  
• **Traffic Dial** controls regional traffic percentage  

### **Endpoints**
• Supported endpoint types:
  - ALB  
  - NLB  
  - EC2 Instances  
  - Elastic IP addresses  
• Global Accelerator can front regional ALBs  

---

## Health Checks
• Global Accelerator constantly checks endpoint health  
• Routes traffic **only to healthy endpoints**  
• Customizable protocol, port, interval, thresholds  

---

## Traffic Distribution

### **Traffic Dial**
• Control % of traffic sent to each region  
• Useful for:
  - Blue/green deploys  
  - Failover tests  
  - Gradual migration  

### **Client IP Preservation**
• Preserves original client IP  
• Supported when using NLB endpoints  

---

## Routing and Performance
• Uses AWS’s **private global network**  
• Reduces:
  - Latency  
  - Jitter  
  - Packet loss  
• Routes user traffic through closest AWS edge location  
• Finds best healthy endpoint instantly  

---

## Failover and High Availability
• Continuous health monitoring  
• Quick failover to healthy regions or endpoints  
• Prevents downtime during outages  

---

## Pricing
• Fixed **monthly fee per accelerator**  
• Data transfer:
  - Accelerated traffic (over AWS backbone)  
  - Non-accelerated traffic standard pricing  

---

## Use Cases
• Global web applications  
• Disaster recovery with multi-region failover  
• Real-time gaming (UDP support)  
• IoT with predictable latency  
• Multi-region active-active deployments  
• Controlled traffic shifting / gradual releases  

---

## Security
• Built-in **AWS Shield Standard** (DDoS protection)  
• Works with WAF (when using ALB/NLB)  
• Static IPs simplify firewall rules  
• TLS handled at ALB/NLB layer  

---

## Comparison: Global Accelerator vs CloudFront

| Feature | Global Accelerator | CloudFront |
|--------|--------------------|------------|
| Primary Use | Global performance & failover for applications | CDN for cached/static/dynamic content |
| Caching | ❌ No | ✔️ Yes |
| Static IPs | ✔️ Yes | ❌ No |
| Protocols | TCP & UDP | HTTP & HTTPS |
| Routing Layer | L4 (network) | L7 (application) |
| Latency Improvement | AWS backbone routing | Edge caching |

---

## Integration with AWS Services
• ALB, NLB, EC2, Elastic IP endpoints  
• AWS Certificate Manager (via ALB/NLB)  
• AWS WAF (when using ALB)  
• CloudWatch for monitoring health and performance  
• AWS Shield Standard for DDoS protection  

---

## Exam Tips
• Global Accelerator ≠ CloudFront → No caching  
• Provides **static IPs**, multi-region failover, TCP/UDP support  
• Uses traffic dial for controlled rollout  
• Best for latency-sensitive global apps  
• Routes traffic over AWS’s private backbone  
• Health checks drive routing decisions  

---

## Quick Summary
AWS Global Accelerator improves performance and availability for global applications by routing traffic over AWS’s private network, not the public internet. It provides static IPs, automatic failover, intelligent routing, and multi-region traffic control—ideal for high-performance, globally distributed systems.

