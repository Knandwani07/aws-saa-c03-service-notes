# Amazon CloudFront

---

## What It Is
Amazon CloudFront is a **global Content Delivery Network (CDN)** that caches and delivers content from **edge locations** worldwide, improving latency and performance for static and dynamic websites, APIs, media, and applications.

---

## Core Concepts

### **Edge Locations**
• Global network of caching servers  
• Serve content from the closest location to reduce latency  
• Cache frequently requested objects for faster delivery  

### **Regional Edge Caches**
• Sits between origins and edge locations  
• Ideal for larger, less frequently accessed content  
• Reduces load on origin servers  

### **Origins**
• Source locations where CloudFront fetches content  
• Supported origins:  
  – Amazon S3  
  – EC2 instances  
  – Elastic Load Balancers  
  – Custom HTTP/HTTPS endpoints  

### **Distributions**
• Define how CloudFront behaves  
• Types:  
  – Web distributions (static/dynamic content)  
  – RTMP (deprecated)  

---

## How It Works
1. A viewer requests content  
2. CloudFront routes to nearest edge location  
3. If cached → served immediately (cache hit)  
4. If not → fetch from origin, cache it, then serve (cache miss)  
5. Cache refreshed before TTL expiry  

---

## Caching and TTL

### **Cache-Control Headers**
• Controls how CloudFront caches objects  

### **TTL Settings**
• Minimum TTL  
• Default TTL (typically 24h)  
• Maximum TTL  
• Configurable per object or distribution  

### **Cache Invalidation**
• Remove objects before TTL expires  
• Supports wildcards  
• Available via console, CLI, API  

---

## Security Features

### **SSL/TLS**
• HTTPS support (viewer ↔ CloudFront, CloudFront ↔ origin)  
• ACM integration for free certificates  
• Supports SNI and dedicated IP SSL  

### **Origin Access Control (OAC)**
• Secures S3 origins by blocking direct access  
• Replaces OAI with SigV4-authenticated requests  

### **Signed URLs / Signed Cookies**
• Control access to private content  
• Signed URLs → per-object  
• Signed Cookies → bulk content access  

### **Field-Level Encryption**
• Encrypt sensitive data (PII, card info) at the edge  
• Only origin can decrypt  

### **Geo Restriction**
• Allowlist or blocklist countries  
• Supports licensing and compliance  

### **AWS WAF Integration**
• Protect against common web exploits  
• Custom rule sets + rate-limiting  

### **AWS Shield Standard**
• Built-in DDoS protection at no cost  

---

## Content Customization

### **Lambda@Edge**
• Runs Node.js/Python at edge  
• Use cases:  
  – Auth logic  
  – A/B testing  
  – Redirects / rewrites  
  – Personalization  

### **CloudFront Functions**
• Lightweight JavaScript  
• Sub-millisecond execution  
• Use cases:  
  – Header manipulation  
  – URL rewrites  
  – Cache key normalization  

---

## Logging & Monitoring

### **Standard Logs**
• Delivered to S3  
• Includes IP, URLs, user-agents, etc.

### **Real-Time Logs**
• Kinesis Data Streams output  
• Near-instant log consumption  

### **CloudWatch Metrics**
• Requests  
• Cache hit/miss  
• 4xx/5xx errors  
• Data transfer  

### **CloudTrail**
• Tracks API calls for auditing  

---

## Price Classes
• **Price Class 100** → US + EU + Canada (cheapest)  
• **Price Class 200** → Most regions  
• **Price Class All** → All edge locations (best performance, highest cost)  

---

## Compression
• Automatic gzip/brotli compression  
• Reduces file size and latency  
• Must enable in distribution settings  

---

## Origin Groups
• Active-passive origin failover  
• Switches to backup origin if primary returns errors  

---

## Integration with AWS Services
• **Amazon S3** – Static hosting & media  
• **AWS WAF** – Web protection  
• **AWS Shield** – DDoS mitigation  
• **Lambda@Edge / CF Functions** – Custom logic  
• **AWS ACM** – SSL certificates  
• **Route 53** – DNS routing  
• **Global Accelerator** – Dynamic content routing  
• **CloudWatch** – Metrics  
• **CloudTrail** – Auditing  

---

## Exam Tips
• CloudFront = **global CDN for low latency**  
• **OAC** is recommended for securing S3 origins  
• Signed URLs/Cookies for private content  
• Field-Level Encryption for sensitive data  
• Lambda@Edge = complex logic | CF Functions = lightweight logic  
• Regional Edge Caches reduce origin load  
• Use origin groups for failover  
• Cache invalidation forces immediate updates  
• Pricing based on:  
  – Data transfer out  
  – Request count  
  – Price class  

---

## Quick Summary
Amazon CloudFront is a **high-performance global CDN** that accelerates delivery of static and dynamic content via edge caching, built-in security (WAF, Shield, OAC), advanced customizations (Lambda@Edge, CloudFront Functions), and tight AWS service integrations. It ensures fast, secure, scalable delivery of websites, APIs, videos, and applications worldwide.

