# Amazon Elastic Kubernetes Service (Amazon EKS)

---

## What It Is

Amazon EKS is a fully managed Kubernetes service that simplifies deploying, managing, and scaling containerized applications using Kubernetes on AWS. It eliminates the need to install, operate, and maintain your own Kubernetes control plane.

---

## Key Features

• Fully managed, highly available Kubernetes control plane  
• Runs upstream, open-source Kubernetes for compatibility  
• Automatic scaling and patching of control plane  
• Integrated with AWS services like IAM, VPC, ALB, CloudWatch, ECR  
• Supports EC2 and AWS Fargate as compute options  
• Native Kubernetes tools (kubectl, Helm) work seamlessly  
• Multi-AZ deployments for high availability  

---

## Control Plane

• Managed by AWS with automatic scaling and redundancy  
• Runs across multiple Availability Zones for high availability  
• Managed API server and etcd with automatic patching and backups  
• AWS handles upgrades of the Kubernetes control plane  

---

## Worker Nodes

• EC2 Launch Type  
 - Self-managed or managed node groups  
 - Control over instance types and AMIs  

• AWS Fargate Launch Type  
 - Serverless, runs Kubernetes pods without managing EC2 instances  
 - Specify CPU and memory at pod level  

• Managed Node Groups  
 - AWS provisions and manages EC2 nodes  
 - Integrated with Auto Scaling  

---

## Networking

• Uses Amazon VPC for cluster networking  
• Supports Kubernetes CNI (Container Network Interface) with VPC-native networking  
• Each pod gets its own ENI and private IP  
• Security Groups and NACLs for traffic control  
• AWS Load Balancer Controller for managing ALB/NLB integration  

---

## Security

• IAM integration for Kubernetes RBAC  
• IAM Roles for Service Accounts (IRSA) for granular permissions  
• Supports Kubernetes RBAC for cluster-level access control  
• Encryption at rest using AWS KMS  
• Encryption in transit using TLS  
• Integration with AWS Secrets Manager and AWS Parameter Store for managing secrets  

---

## Storage

• Supports Amazon EBS for persistent volumes  
• Supports Amazon EFS for shared storage between pods  
• Supports FSx for Lustre for high-performance workloads  
• Dynamic provisioning of persistent volumes using Kubernetes Storage Classes  

---

## Logging and Monitoring

• Integrated with Amazon CloudWatch for logs and metrics  
• Container Insights for detailed monitoring of cluster resources and applications  
• Supports AWS X-Ray for tracing  
• Fluent Bit and CloudWatch Logs for log collection  

---

## Cluster Autoscaler

• Automatically adjusts the number of nodes in your cluster based on pending pods  
• Supports scaling EC2 instances in managed node groups  

---

## Kubernetes Versions

• AWS regularly updates supported Kubernetes versions  
• Ability to choose versions for clusters  
• Control plane and worker nodes can be upgraded independently  

---

## Integration with AWS Services

• AWS IAM for authentication and authorization  
• AWS ALB/NLB for ingress  
• Amazon ECR for container image storage  
• AWS App Mesh for service mesh and observability  
• AWS Fargate for serverless pods  
• AWS CloudFormation and eksctl for infrastructure as code  

---

## Pricing

• Charged per EKS cluster per hour  
• Pay for EC2 instances or Fargate pods used as worker nodes  
• Standard AWS charges apply for other integrated services (EBS, ALB, CloudWatch)  

---

## Use Cases

• Deploying and managing microservices applications  
• Hybrid workloads with EC2 and Fargate  
• Batch processing and ML workflows on Kubernetes  
• Migrating existing Kubernetes workloads to AWS  
• Building multi-AZ, highly available applications  

---

## Exam Tips

• EKS control plane is managed by AWS and runs across multiple AZs  
• Supports EC2 and Fargate launch types for worker nodes  
• VPC CNI provides pod-level ENIs and IP addresses  
• IAM Roles for Service Accounts allow fine-grained permissions for pods  
• AWS Load Balancer Controller automates ALB/NLB integration for services  
• Supports encryption at rest with KMS and in transit with TLS  
• Managed Node Groups simplify worker node lifecycle management  
• EFS integration enables persistent, shared storage between pods  
• eksctl simplifies cluster provisioning and management  
• Best for running standard Kubernetes workloads with AWS integrations  

---

## Quick Summary

Amazon EKS is a fully managed Kubernetes service providing a production-ready control plane, integrated AWS security and networking, and support for both EC2 and Fargate worker nodes. It allows organizations to run standard Kubernetes applications on AWS with high availability, scalability, and ease of management.

