# AWS Outposts

AWS Outposts is a fully managed hybrid-cloud service that extends AWS infrastructure, services, APIs, and tools directly into your on-premises or edge environment.  
It effectively brings an AWS Availability Zone into your data centre for low-latency, data-residency, and hybrid application needs.

---

## What It Is

• Run AWS services locally (EC2, EBS, ECS/EKS, etc.) on your premises  
• Managed AWS hardware (racks/servers/switches) — no low-level maintenance needed  
• Same AWS APIs, tooling, and DevOps workflows as the cloud  
• Supports low-latency processing, data residency, and edge applications  
• Hybrid networking extends your VPC on-prem using LGW (rack) or LNI (server)  

---

## Form Factors / Configurations

• Outposts Racks — full 42U racks with compute, storage, networking, installed by AWS  
• Outposts Servers — compact 1U/2U servers for retail, branch offices, and edge sites  
• Each requires on-prem readiness: power, cooling, weight load, cabling, and network  

---

## How It Works

• Outpost is “homed” to a specific AWS Region and AZ — extending that AZ into your site  
• Outpost Subnet — a VPC subnet mapped directly to the Outpost hardware  
• Local Gateway (LGW) — for racks, used to route between Outpost and on-prem network  
• Local Network Interface (LNI) — for servers, provides direct on-prem connectivity  
• Service Link — encrypted communication between Outpost and the parent AWS Region  

---

## Supported Services & Capabilities

• Compute: EC2, ECS, EKS  
• Storage: EBS (and limited S3 depending on Outposts generation)  
• Networking: VPC extension, routing to on-prem, integration with Direct Connect/Internet  
• Data residency and ultra-low-latency edge workloads  

---

## Pricing

• Term-based pricing (typically 3-year contract) for Outpost infrastructure  
• You pay for:  
  – Outpost hardware contract  
  – AWS services consumed on the Outpost (EC2/EBS/etc.)  
  – Data transfer for Service Link traffic  
• You are not charged for:  
  – Some data transfers from Outpost → parent Region  

---

## Use Cases

• Ultra-low latency systems (manufacturing lines, real-time control systems)  
• Data residency/compliance situations requiring on-prem data storage  
• Migrating legacy apps that require on-prem dependencies  
• Retail/branch/edge environments needing local compute with AWS consistency  

---

## Best Practices

• Validate whether hybrid is truly required — Outposts has cost & complexity  
• Right-size compute and storage capacity for workload + growth  
• Ensure physical readiness: power, cooling, rack space, network paths  
• Extend VPC carefully — design routing, LGW/LNI integration properly  
• Use consistent CloudWatch, IAM, and DevOps tooling across cloud + Outpost  
• Monitor Service Link health — link loss may impact functionality  
• Evaluate cost trade-offs — cloud-only may be cheaper unless residency/latency is critical  

---

## Exam Tips

• Outposts = AWS infrastructure **on-premises**  
• Same AWS APIs, Console, and IaC — treat as an extension of an AZ  
• Know Racks vs Servers and what each supports  
• Key networking: Outpost Subnet, LGW (rack), LNI (server)  
• Best use cases: latency-sensitive, data-residency, edge deployments  
• Pricing includes hardware term + service usage + Service Link transfer  
• Only specific AWS services run locally — verify service eligibility  
• Outpost subnets behave like standard VPC subnets with extended routing  

---

## Quick Summary

AWS Outposts brings AWS hardware and services directly to your data centre or edge site, enabling true hybrid cloud.  
You get local EC2, EBS, and container services with consistent AWS APIs and tooling, ideal for low-latency, compliant, or edge environments — but it requires proper on-site infrastructure, networking, and cost consideration.

