# Amazon Elastic Container Registry (Amazon ECR)

---

## What It Is

Amazon ECR is a fully managed container image registry that makes it easy to store, manage, share, and deploy container images and artifacts. It integrates with AWS services like ECS, EKS, and AWS Lambda, as well as open-source tools.

---

## Key Features

• Fully managed, highly available registry  
• Supports Docker and Open Container Initiative (OCI) images  
• Integrated with ECS, EKS, Lambda, CodeBuild, CodeDeploy, CodePipeline  
• Push and pull images using standard Docker CLI or AWS CLI  
• Supports image scanning for vulnerabilities  
• Repository-level permissions with AWS IAM  
• Lifecycle policies for automated image cleanup  
• Supports replication across regions for DR and latency optimization  
• Encryption at rest with AWS KMS and in transit with TLS  
• Cross-account access with resource policies  

---

## Repositories

• Stores container images in private or public repositories  
• Private repositories for controlled access  
• Public repositories for open sharing without authentication  
• Each repository stores multiple image versions identified by tags  

---

## Authentication

• AWS CLI or SDK for authentication  
• IAM policies control user and role access to repositories  
• ECR Credential Helper for Docker CLI integration  
• Supports temporary credentials via AWS IAM roles  

---

## Image Management

• Push images to ECR from build systems or local machines  
• Pull images to ECS, EKS, Fargate, or other Docker environments  
• Supports multi-architecture images  
• Image tags for versioning and organizing images  
• Immutable tags can be enforced to prevent overwrites  

---

## Image Scanning

• Built-in vulnerability scanning using Common Vulnerabilities and Exposures (CVE) database  
• Can scan on image push or on-demand  
• Provides detailed findings for remediation  
• Integrated with AWS Security Hub for consolidated findings  

---

## Replication

• Supports cross-region replication of images  
• Automatic replication to one or more AWS regions  
• Simplifies DR, compliance, and global deployment needs  
• Managed via repository settings and policies  

---

## Lifecycle Policies

• Automates cleanup of unused or old images  
• Rules based on image count, age, or tags  
• Reduces storage costs and clutter  

---

## Encryption

• Images encrypted at rest using AWS KMS  
• Encryption in transit via HTTPS/TLS  
• Supports customer-managed KMS keys  

---

## Logging and Monitoring

• Amazon CloudWatch integration for monitoring actions  
• AWS CloudTrail records API calls for auditing  
• EventBridge integration for image push notifications  

---

## Integration with AWS Services

• Amazon ECS and EKS for container orchestration  
• AWS Fargate for serverless container deployment  
• AWS CodePipeline, CodeBuild, CodeDeploy for CI/CD  
• AWS Lambda for container-based functions  

---

## Pricing

• Charged based on data storage (per GB-month)  
• Data transfer costs for image pulls outside the region  
• Scanning fees per image scan  
• Free tier includes 500MB storage per month for private repositories  

---

## Public Repositories

• Host public container images with no authentication required for pulls  
• Ideal for sharing software, tools, or base images publicly  
• Integrates with the AWS Container Registry website for browsing  

---

## Use Cases

• Storing private Docker images for ECS, EKS, Fargate  
• Hosting public images for open-source projects  
• Integrating secure, managed image storage in CI/CD pipelines  
• Enabling multi-region deployments with cross-region replication  
• Ensuring security with built-in vulnerability scanning  

---

## Exam Tips

• Supports both private and public repositories  
• IAM policies and resource policies manage access  
• Vulnerability scanning can be on-push or on-demand  
• Cross-region replication for DR and global distribution  
• Integrated with ECS, EKS, Fargate, CodePipeline, Lambda  
• Lifecycle policies help automate image cleanup  
• Encryption at rest with KMS and in transit with TLS  
• Use ECR Credential Helper or AWS CLI for authentication  

---

## Quick Summary

Amazon ECR is a fully managed, secure, scalable container image registry that integrates with AWS container services and CI/CD workflows. It simplifies storing, managing, and sharing container images with built-in security, replication, and automation features for modern containerized application development.
