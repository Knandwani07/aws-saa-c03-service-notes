# AWS Wavelength

AWS Wavelength extends AWS compute and storage services into 5G networks by placing AWS infrastructure inside telecommunications datacenters. This allows developers to run applications closer to mobile users, achieving ultra-low latency while using the same AWS APIs, tools, and services as in a standard AWS Region.

---

## Key Features

• Run applications inside Wavelength Zones (extensions of an AWS Region)  
• Ultra-low latency for 5G, mobile, and edge devices  
• Deep integration with carriers (Verizon, Vodafone, KDDI, SK Telecom)  
• Use familiar AWS services: EC2, ECS, EKS, VPC, NLB, CloudWatch  
• Same AWS APIs, AMIs, IAM, and operational tooling  
• Traffic stays inside the 5G network path for minimal latency and jitter  
• Ideal for containers, microservices, ML inference, AR/VR, and gaming  

---

## Wavelength Zones

• Telecom-operated datacenters that extend an AWS Region  
• Appear as isolated subnets inside your VPC  
• Connected to the parent Region via secure, high-bandwidth links  
• Provide EC2 compute, EBS storage, VPC networking, NLB load balancing  
• Designed for ultra-low latency applications for mobile users in that geography  

---

## Supported Services

• Amazon EC2 (edge-optimized instance types)  
• Amazon EBS  
• Amazon VPC with Wavelength subnets  
• Network Load Balancer (NLB)  
• Amazon ECS / Amazon EKS  
• Amazon CloudWatch  
• AWS CloudFormation and AWS CLI  

---

## Networking

• Create a VPC in the parent Region and add Wavelength subnets  
• Carrier Gateways:  
  • Enable traffic between Wavelength instances and 5G mobile users  
  • No Internet Gateway inside Wavelength  
• Traffic path: Mobile Device → 5G Network → Wavelength Zone  
• Use NLB to expose workloads to users  
• Full support for Security Groups, NACLs, routing tables  

---

## Storage

• Amazon EBS for persistent block storage  
• Supports root volumes and data volumes  
• No S3 in Wavelength Zones (S3 resides in the parent Region)  
• S3 may be used for logs, backups, or content storage with higher latency  

---

## Compute

• EC2 instance families vary by carrier and location  
• Supports container workloads through ECS or EKS  
• Suited for compute-intensive applications requiring minimal latency  

---

## Use Cases

• Real-time gaming or game streaming  
• AR/VR immersive applications  
• Autonomous systems and robotics control  
• Live video analytics  
• ML inference at the edge  
• Smart cities and IoT backends  
• Telemedicine and remote patient monitoring  
• Connected vehicle (V2X) systems  

---

## Security

• Uses AWS IAM, KMS, Security Groups, and NACLs as in a standard Region  
• Wavelength subnets isolated within the VPC  
• Communication to parent Region secured over AWS backbone  
• No Internet Gateway — public access uses Carrier Gateway  

---

## Pricing

• EC2 instance usage in Wavelength Zones  
• EBS storage  
• Data transfer from Wavelength → parent Region  
• NLB usage  
• No additional surcharge for using Wavelength Zones  

---

## Deployment Flow

1. Create VPC in the associated AWS Region  
2. Add Wavelength Zone subnets  
3. Deploy EC2 / ECS / EKS workloads into Wavelength subnets  
4. Attach NLB for mobile user traffic  
5. Route traffic through Carrier Gateway  
6. Monitor using CloudWatch  

---

## Exam Tips

• Wavelength = AWS compute + storage at the telecom 5G edge  
• Latency reduction comes from staying inside the telecom network  
• Wavelength Zones use Carrier Gateways, not Internet Gateways  
• All resources still originate from the parent Region  
• Compute services available: EC2, ECS, EKS  
• Storage: EBS only  
• Use NLB for public traffic exposure  
• Best for ultra-low latency mobile applications  

---

## Quick Summary

AWS Wavelength brings AWS infrastructure into 5G networks to enable ultra-low latency application deployment. With Wavelength Zones extending your VPC, you can run EC2, ECS, EKS, and EBS workloads close to mobile users while using the same AWS APIs and tools. It is ideal for AR/VR, gaming, robotics, analytics, and other real-time edge applications.

