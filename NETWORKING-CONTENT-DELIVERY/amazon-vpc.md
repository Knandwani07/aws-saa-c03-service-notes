# Amazon VPC

---

## What It Is
Amazon Virtual Private Cloud (VPC) lets you create a **logically isolated virtual network** within AWS. You control IP ranges, subnets, routing, gateways, and security enabling secure, scalable architectures for applications, hybrid networks, and multi-account environments.

---

## Key Features
• Full control over IP ranges (IPv4/IPv6)  
• Create public, private, and VPN-only subnets  
• Custom route tables for traffic control  
• Internet Gateway + NAT for outbound internet access  
• Security Groups (stateful) + Network ACLs (stateless)  
• VPC Peering, PrivateLink, and Transit Gateway support  
• Integrates with ECS, RDS, Directory Service, Lambda, and more  

---

## Subnets
• Subnet = a slice of VPC CIDR  
• **Public subnets** → route to Internet Gateway  
• **Private subnets** → no direct internet route  
• Spread subnets across AZs for high availability  
• Subnet CIDR blocks must not overlap  

---

## Route Tables
• Define how traffic flows within/outside the VPC  
• Each subnet associates with exactly **one** route table  
• Routes point to IGW, NAT Gateway, Transit Gateway, VGW, etc.

---

## Internet Gateway (IGW)
• Highly available gateway for public internet access  
• Each VPC supports **one** IGW  
• Required for instances in public subnets to reach the internet  

---

## NAT Gateway / NAT Instance
• Provide **outbound-only internet access** for private subnets  
• NAT Gateway = managed, HA within a single AZ  
• NAT Instance = self-managed EC2, legacy option  

---

## Elastic IP Addresses
• Static public IPv4 addresses  
• Commonly used with NAT Gateways, bastion hosts, etc.

---

## VPC Peering
• Private VPC-to-VPC connectivity on AWS backbone  
• No transitive peering—you must create direct links  
• Works intra-Region and cross-Region  
• Update route tables + security groups for connectivity  

---

## AWS Transit Gateway
• Hub-and-spoke model for many VPCs and on-prem networks  
• Supports transitive routing (unlike peering)  
• Scales for enterprise multi-VPC networks  

---

## AWS PrivateLink
• Private, service-to-service connectivity using ENIs  
• No need for public IPs or traversing the public internet  
• Supports exposing internal applications securely

---

## VPC Endpoints
### • Interface Endpoints (PrivateLink)
• Connect privately to AWS services via ENIs  
• Used for services like SSM, SNS, EC2 API, etc.

### • Gateway Endpoints
• Only for **S3 and DynamoDB**  
• Route table–based, no ENI required  

---

## VPN Connections
• Encrypted IPsec tunnels from on-prem to AWS VPC  
• Uses **Virtual Private Gateway (VGW)** on AWS side  
• Uses **Customer Gateway** on on-prem side  
• Supports BGP for dynamic routing  

---

## Carrier Gateway
• Networking gateway for **AWS Outposts**  
• Connects Outposts to carrier networks

---

## Security Groups
• Instance-level virtual firewall  
• **Stateful** (return traffic allowed automatically)  
• Rules allow traffic only (no explicit deny)

---

## Network ACLs (NACLs)
• Subnet-level firewall  
• **Stateless** (return traffic must be explicitly allowed)  
• Supports allow/deny rules  
• Rules evaluated by ascending rule number  

---

## Flow Logs
• Capture IP traffic metadata for ENIs, subnets, or VPC  
• Sent to CloudWatch Logs or S3  
• Used for diagnostics, auditing, and security analysis  

---

## IPv6 Support
• Native support for IPv6  
• No need for NAT—IPv6 is globally routable  
• SGs and NACLs filter IPv6 traffic  

---

## VPC Sharing
• Share subnets across accounts in an AWS Organization  
• Centralize networking while decentralizing resource ownership  

---

## Elastic Network Interfaces (ENIs)
• Virtual NICs attached to EC2 instances  
• Support multiple IPs, SGs, failover networking  
• Used for HA appliances and multi-homed instances  

---

## Pricing
• VPC itself is free  
• You pay for:  
  – NAT Gateway  
  – VPC endpoints  
  – Transit Gateway  
  – VPN connections  
  – Cross-AZ traffic  
  – Peering traffic (in some cases)

---

## Use Cases
• Secure web applications with public/private subnet design  
• Hybrid cloud IPsec tunnels and Direct Connect  
• Multi-VPC architectures with centralized networking  
• PrivateLink-based service sharing  
• Secure partner access via endpoints  

---

## Exam Tips
• IGW required for public subnet internet access  
• NAT Gateway = private subnet outbound access  
• SGs are **stateful**, NACLs are **stateless**  
• VPC Peering has **no transitive routing**  
• Transit Gateway allows scalable transitive routing  
• PrivateLink = private connectivity to services  
• Gateway Endpoints = S3 + DynamoDB only  
• Flow Logs used for traffic troubleshooting  
• IPv6 routing doesn’t require NAT  

---

## Quick Summary
Amazon VPC provides **complete control over your AWS networking**, including subnets, routing, gateways, and security. It supports private connectivity to on-prem systems, inter-VPC architectures, and secure access to AWS services—all while giving you deep visibility and segmentation options for building robust cloud networks.

