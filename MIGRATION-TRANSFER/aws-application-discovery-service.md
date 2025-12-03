# AWS Application Discovery Service

---

## What It Is
AWS Application Discovery Service helps enterprises **identify, analyze, and understand on-premises servers, applications, and dependencies** before migrating to AWS. It collects configuration, usage, and performance data to support migration planning, grouping, and cost estimation, feeding insights directly into **AWS Migration Hub**.

---

## Key Features

• Automatic discovery of on-premises servers and applications  
• Collects configuration, performance, and usage data  
• Maps application dependencies and network connections  
• Integrates with AWS Migration Hub for migration planning  
• Supports agent-based and agentless discovery  
• Enables accurate TCO and migration readiness analysis  

---

## Discovery Methods

### 1. Agent-Based Discovery
• Install lightweight agents on each on-prem server  
• Collects deep metrics: CPU, memory, disk I/O, network, processes  
• Captures dependency and process-level details  
• Ideal for complex, multi-tier workloads  
• Sends encrypted data securely to AWS  

### 2. Agentless Discovery (AWS Agentless Collector)
• Deploys a virtual appliance in **VMware vCenter**  
• Discovers VM configurations, usage, and network flows  
• Requires no software installation on individual VMs  
• Best for large VMware environments  

---

## Data Collected

• Server metadata (hostname, IP, OS, CPU, RAM, disks)  
• Performance metrics (CPU, RAM, I/O, throughput)  
• Application/process details and running services  
• Network connections and dependency mapping  
• Long-term usage trends and workload patterns  

---

## Integration with AWS Migration Hub

• Central visualization of discovered servers, applications, and dependencies  
• Helps group servers into applications for migration planning  
• Provides migration recommendations and progress tracking  
• Data can be exported for deeper analysis  

---

## Security

• All communication encrypted via TLS/HTTPS  
• IAM roles and policies control access to discovery data  
• Data stays in your chosen region unless configured otherwise  
• Discovery data can be deleted anytime  

---

## Integration with Other AWS Services

• **AWS Migration Hub** – Dashboard for planning and tracking  
• **Migration Evaluator** – TCO analysis using discovery metrics  
• **AWS MGN** – Lift-and-shift server migration  
• **AWS DMS** – Database migration  

---

## Pricing

• Free to use (agents and collectors included)  
• Standard AWS storage/data transfer charges may apply  

---

## Use Cases

• Pre-migration assessment for on-premises workloads  
• Application dependency mapping for multi-tier architectures  
• Identifying underutilized resources for cost optimization  
• Supporting rehost/replatform migration strategies  
• Building performance baselines  

---

## Best Practices

• Run discovery **2–4 weeks** to capture accurate patterns  
• Use agent-based discovery for deeper insight  
• Combine agentless + agent-based for complete visibility  
• Group servers into applications before migration  
• Export data regularly from Migration Hub  
• Restrict IAM access and enforce encryption  

---

## Exam Tips

• Used during **Assessment & Discovery** phase (not actual migration)  
• Agent-based = deep performance + dependency data  
• Agentless = VMware environments, broad inventory  
• Integrates tightly with Migration Hub  
• Helps with TCO, dependency mapping, and migration planning  
• Free service with no extra licensing  

---

## Quick Summary
AWS Application Discovery Service automates the discovery of on-premises servers, applications, and dependencies to enable accurate, data-driven migration planning. It integrates with AWS Migration Hub, supports both agent-based and agentless discovery, and provides detailed insights for cost estimation, architecture planning, and workload grouping without manual effort.

