# AWS Fargate Cheat Sheet

---

## What It Is
• Serverless compute engine for running containers without managing servers or EC2 clusters.  
• Works with **Amazon ECS** and **Amazon EKS** to provide on-demand, right-sized compute capacity.

---

## Key Features
• Serverless compute for containers  
• Deep integration with ECS & EKS  
• No EC2 provisioning or scaling required  
• Per-second billing based on vCPU + memory  
• Automatic scaling based on tasks/pods  
• Integrated with IAM, VPC, CloudWatch, X-Ray, Secrets Manager  

---

## How It Works
• You define **task definitions** (ECS) or **pod specs** (EKS)  
• Specify CPU/memory  
• Fargate launches tasks/pods with dedicated ENIs  
• Logging/metrics available in CloudWatch  
• You focus on containers—AWS handles the infra  

---

## Integration with ECS
• Runs ECS tasks without EC2 instances  
• Tasks receive ENIs in your VPC (**awsvpc mode**)  
• Compatible with ALB/NLB  
• Works with ECS Service Auto Scaling  
• Supports ECS Capacity Providers for hybrid EC2 + Fargate  

---

## Integration with EKS
• Runs Kubernetes pods without EC2 nodes  
• Configure **Fargate Profiles** to select which pods run on Fargate  
• Each pod gets ENI for isolated networking  
• Fully integrated with Kubernetes scheduling & autoscaling  

---

## Task Definitions
• Specify container image, CPU, memory, networking, IAM roles  
• Supports Linux containers  
• Integrates with Secrets Manager & Parameter Store  
• CloudWatch Logs supported natively  

---

## Networking
• Uses **awsvpc** networking mode  
• Each task/pod gets a separate ENI + private IP  
• Supports SGs & NACLs  
• Fine-grained isolation between containers  
• Supports AWS PrivateLink  

---

## Security
• IAM Roles for Tasks/Pods  
• Data encrypted in transit & at rest  
• Secrets Manager + SSM Parameter Store support  
• VPC-level isolation for workloads  

---

## Monitoring & Logging
• CloudWatch Logs + CloudWatch Metrics  
• ECS/EKS metrics integrated  
• Supports AWS X-Ray for tracing  
• EventBridge integrates with Fargate service events  

---

## Scaling
• Fully automatic scaling  
• ECS:
  - Service Auto Scaling rules  
• EKS:
  - Horizontal Pod Autoscaler (HPA)  
• Precise resource allocation per task/pod  

---

## Pricing
• Pay for **requested CPU + memory per second**  
• Fargate Spot available for discounted workloads  
• Extra charges for LB, data transfer, and storage  

---

## Use Cases
• Microservices  
• Event-driven architectures  
• CI/CD pipeline workloads  
• Batch & scheduled jobs  
• Containerizing legacy apps  
• Kubernetes workloads without node management  

---

## Benefits
• Zero server management  
• Granular billing, cost-efficient  
• Strong task/pod isolation  
• Deep AWS ecosystem integration  
• Seamless scaling with no infra overhead  

---

## Exam Tips
• Fargate = no EC2 instances required  
• Works with ECS & EKS  
• Uses **awsvpc** mode (ENI per task/pod)  
• Pay based on vCPU + memory  
• Use IAM roles for tasks/pods  
• Works with ECS Auto Scaling & EKS HPA  
• Use Secrets Manager/Parameter Store for credentials  

---

## Quick Summary
AWS Fargate is a fully managed serverless compute engine for ECS and EKS that eliminates EC2 cluster management. It provides secure, scalable, and cost-efficient container execution with per-task/pod resource isolation and automatic scaling.
