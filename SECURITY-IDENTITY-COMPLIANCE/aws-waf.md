# AWS WAF

---

## What It Is
• A **Web Application Firewall** that protects applications from common exploits and malicious HTTP/S traffic.  
• Lets you **allow, block, or count** web requests based on rules you define.  
• Works at **Layer 7 (HTTP/S)** to protect APIs, websites, and edge workloads.

---

## Key Features

### 1. Web ACL (Access Control List)
• The main container that holds WAF rules and actions.  
• Can be attached to:
  - Amazon CloudFront  
  - Application Load Balancer (ALB)  
  - Amazon API Gateway  
  - AWS AppSync  
  - AWS App Runner  

---

### 2. Rules & Rule Groups
• Define how incoming web traffic is inspected and filtered.  
• Rule types include:
  - **IP match** (allow/block IPs or ranges)  
  - **String match** (headers, body, URI, query strings)  
  - **Geo match** (block/allow by country)  
  - **Regex pattern sets**  
  - **Size constraints**  
  - **Rate-based rules**  
• **Managed Rule Groups**:
  - AWS provides prebuilt rules (SQLi, XSS protection).  
  - Marketplace vendors offer curated security rule groups.

---

### 3. Rate-Based Rules
• Automatically block clients exceeding a request threshold.  
• Useful for throttling bots, scrapers, and abusive clients.

---

### 4. Bot Control
• Detect and block unwanted automated traffic.  
• Supports CAPTCHA and silent challenge modes.  
• AWS-managed intelligence for bot patterns.

---

### 5. Custom Responses
• Serve custom error messages or pages when requests are blocked.

---

### 6. Logging & Metrics
• Send full WAF logs to **Amazon Kinesis Data Firehose**.  
• View metrics and create alarms in **Amazon CloudWatch**.

---

## Pricing
You pay for:
• Number of Web ACLs  
• Number of rules within ACLs  
• Number of requests inspected  

---

## Security & Compliance
• Helps meet PCI DSS, GDPR, and security best practices.  
• Protects against **OWASP Top 10** vulnerabilities such as SQLi and XSS.  

---

## Use Cases
• Blocking SQL injection and cross-site scripting attacks.  
• Throttling traffic spikes or bot attacks using rate-based rules.  
• Geoblocking specific regions.  
• Protecting APIs via API Gateway and AppSync.  
• Providing global edge security with CloudFront.

---

## AWS WAF vs AWS Shield
| Service | Purpose |
|--------|---------|
| **AWS WAF** | Application-layer (Layer 7) filtering with custom rules |
| **AWS Shield** | DDoS protection (Layer 3/4 + limited L7) |

**Use together for complete protection**:  
• Shield mitigates DDoS → WAF blocks bad HTTP/S requests.

---

## Exam Tips
• WAF = **Layer 7 protection** using Web ACLs.  
• Attach Web ACLs to CloudFront, ALB, API Gateway, AppSync, App Runner.  
• Use **Managed Rule Groups** for fast protection.  
• **Rate-based rules** for blocking abusive or high-volume IPs.  
• Logging via **Kinesis Firehose**, metrics via **CloudWatch**.  
• Commonly combined with **Shield** & **Firewall Manager**.

---

## Quick Summary
AWS WAF is a flexible, highly configurable Layer 7 firewall that protects web applications from attacks like SQLi, XSS, bots, and excessive request flooding. With rule groups, rate limiting, logging, and deep AWS integration, it delivers strong, customizable edge and application security.

