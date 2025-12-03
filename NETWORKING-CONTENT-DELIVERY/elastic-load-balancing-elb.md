# Amazon Elastic Load Balancer (ELB)

---

## What It Is
Elastic Load Balancing automatically distributes incoming traffic across multiple targets: EC2 instances, containers, Lambda functions, and IP addresses to improve **availability, scalability, and fault tolerance**. It’s fully managed and supports multi-AZ, auto-scaling architectures.

---

## Types of Load Balancers

### **1. Classic Load Balancer (CLB)**
• Legacy (EC2-Classic), still works in VPC  
• Operates at **Layer 4 & Layer 7**  
• Basic routing + simple health checks  
• Limited features → *not recommended for new systems*

### **2. Application Load Balancer (ALB)**
• Operates at **Layer 7 (HTTP/HTTPS)**  
• Host-based & path-based routing  
• Supports ECS, microservices, serverless  
• Routes to multiple target groups  
• Supports WebSockets & HTTP/2  
• Can authenticate users (OIDC, Cognito)  
• Integrates with **AWS WAF**

### **3. Network Load Balancer (NLB)**
• Operates at **Layer 4 (TCP, TLS, UDP)**  
• Ultra-low latency, high throughput  
• Handles **millions of requests/second**  
• Static IP or Elastic IP support  
• Preserves client IP  
• Supports TLS termination & PrivateLink

### **4. Gateway Load Balancer (GWLB)**
• Operates at **Layer 3**  
• Deploy & scale virtual appliances (firewalls, IDS/IPS)  
• Uses **GENEVE protocol**  
• Ideal for inserting traffic-inspection appliances

---

## Listeners and Rules
• Listeners check for client connection requests  
• ALB: can apply rules for host-based and path-based routing  
• NLB: forwards TCP/TLS/UDP traffic directly  
• GWLB: forwards traffic encapsulated using GENEVE  

---

## Target Groups
• Logical grouping of targets  
• Health checks configured per target group  
• Weighted routing supported  
• ALB target types → Instance, IP, Lambda  
• NLB target types → Instance, IP  

---

## Health Checks
• Detect unhealthy targets and stop sending traffic  
• Configurable protocol, path, interval, thresholds  
• Supports **HTTP, HTTPS, TCP, gRPC** (ALB)

---

## Cross-Zone Load Balancing
• Even distribution of traffic across AZs  
• **Enabled by default** → ALB & CLB  
• **Optional** → NLB  

---

## SSL/TLS Termination
• Offload encryption/decryption to ELB  
• Certificates from **AWS Certificate Manager (ACM)**  
• Supported on ALB & NLB  

---

## Sticky Sessions
• Session affinity using cookies  
• Supported by **ALB and CLB**  
• Useful for stateful applications  

---

## Security Features
• ACM for SSL/TLS certificates  
• Security Groups → ALB & CLB only  
• AWS WAF → ALB integration  
• Access logs to S3  
• IAM access controls  
• CloudTrail logs for auditing  

---

## Logging and Monitoring
• **Access Logs** → stored in S3  
• **CloudWatch metrics** → requests, latency, healthy host count  
• **CloudTrail** → API activity logging  
• ALB provides request tracing via `X-Amzn-Trace-Id`

---

## Integration with AWS Services
• Auto Scaling Groups  
• ECS (including service auto-registration)  
• Lambda (ALB only)  
• AWS Global Accelerator  
• Route 53 for DNS routing  
• ACM for TLS certificates  

---

## Pricing
• Billed for:  
  - Hours the load balancer runs  
  - Data processed  
• ALB & NLB include **LCU (Load Balancer Capacity Unit)** charges  
• GWLB → billed per GB processed  

---

## Use Cases
• **ALB** → Microservices, HTTP routing, serverless  
• **NLB** → Financial apps, gaming, TCP/UDP workloads  
• **GWLB** → Firewalls, security appliances  
• **CLB** → Legacy apps with basic routing  

---

## Exam Tips
• ALB = Layer 7, advanced routing, Lambda targets  
• NLB = Layer 4, ultra-low latency, static IP  
• GWLB = Deploy security appliances (Layer 3, GENEVE)  
• Sticky sessions → ALB & CLB  
• Cross-zone LB → Default on ALB/CLB, optional on NLB  
• WAF works only with ALB  
• NLB does *not* support security groups  
• Use ACM for certificate management  
• Health checks automatically remove bad targets  

---

## Quick Summary
Amazon ELB provides **highly available, scalable, and secure** traffic distribution across multiple compute targets. With ALB for Layer 7 routing, NLB for high-speed Layer 4 workloads, GWLB for network appliances, and CLB for legacy workloads, ELB enables resilient architectures tightly integrated with Auto Scaling, ECS, ACM, and WAF—all with minimal operational overhead.

