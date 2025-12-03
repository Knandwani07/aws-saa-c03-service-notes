# AWS Transit Gateway

---

## What It Is
AWS Transit Gateway is a **scalable, central network hub** that connects multiple VPCs and on-premises networks through a single gateway. It removes the complexity of full-mesh VPC peering and enables clean, centralized routing for large hybrid and multi-VPC environments.

---

## Key Features
• Central hub for VPC ↔ VPC and hybrid connectivity  
• Replaces many-to-many VPC peering with a hub-and-spoke design  
• Supports **thousands** of VPC attachments  
• Regional service with **inter-Region peering**  
• Elastic, fully managed scaling  
• Integrates with VPN and Direct Connect  

---

## Attachments
### • VPC Attachments  
Connect VPCs to the Transit Gateway using subnet associations + routing.  

### • VPN Attachments  
Site-to-Site VPN with BGP or static routing for hybrid connections.  

### • Direct Connect Gateway Attachments  
Hybrid connectivity from on-prem via Direct Connect → Transit Gateway → multiple VPCs (even cross-Region).

### • Peering Attachments  
Connect Transit Gateways in different AWS Regions for global private networking.

---

## Routing
• Managed via **Transit Gateway route tables**  
• Each attachment can associate with a route table  
• Route tables decide **which networks can communicate**  
• Supports segmentation/isolation for multi-tenant or multi-environment setups  

---

## Inter-Region Peering
• Private, low-latency connection between TGWs in different Regions  
• Traffic stays on AWS’s private backbone (not the public internet)  
• Used for global enterprise architectures

---

## Bandwidth & Performance
• Tens of Gbps of throughput  
• Fully managed scaling and fault tolerance  
• Suitable for large-scale enterprise networking

---

## Multicast Support
• Native IGMP multicast support  
• Used in financial trading, live data feeds, media distribution, etc.

---

## Security & Access Control
• Share Transit Gateway across accounts with **AWS Resource Access Manager (RAM)**  
• IAM controls API-level permissions  
• No internet traversal unless you explicitly route traffic  
• CloudTrail logs API access and configuration changes  

---

## Integrations
• **Direct Connect Gateway** for dedicated hybrid connectivity  
• **Site-to-Site VPN** for encrypted hybrid tunnels  
• **AWS RAM** for cross-account sharing  
• **Network Firewall / security VPCs** for centralized inspection  

---

## Pricing
• Per-attachment hourly cost  
• Per-GB data processing charges  
• Separate charges for inter-Region TGW peering  

---

## Use Cases
• Hub-and-spoke multi-VPC architecture  
• Simplifying complex VPC mesh peering  
• Hybrid cloud architectures with multiple VPCs  
• Multi-Region private connectivity  
• Centralizing inspection using security VPCs  
• Large enterprise networks needing scalable routing

---

## Exam Tips
• Transit Gateway = central router for multi-VPC + hybrid networking  
• Route tables decide which attachments can talk to each other  
• Supports VPC, VPN, Direct Connect, and peering attachments  
• Inter-Region TGW peering = private global routing  
• Use RAM to share TGW with multiple AWS accounts  
• Replaces VPC peering for large-scale topologies  
• Supports multicast workloads  

---

## Quick Summary
AWS Transit Gateway is a **high-performance, central networking hub** that connects VPCs, on-premises networks, and multi-Region architectures through a single, scalable gateway. It simplifies routing, supports hybrid and global connectivity, and provides clean, secure, manageable network designs for enterprise-scale environments.

