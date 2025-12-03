# Amazon Elastic Container Service (Amazon ECS)

Amazon ECS is a fully managed container orchestration service that makes it easy to deploy, manage, and scale containerized applications using Docker. It eliminates the need to install and operate your own container orchestration software or manage clusters of virtual machines.

---

## What It Is

• Fully managed container orchestration  
• Supports Docker containers  
• Deep integration with AWS services (IAM, CloudWatch, VPC, ALB, Service Discovery)  
• Runs on EC2 instances or AWS Fargate for serverless containers  
• Supports Windows and Linux workloads  
• Integrated service discovery using AWS Cloud Map  
• Rolling updates and deployment controls  
• Task placement strategies and constraints  

---

## Key Features

• Fully managed and scalable container orchestration  
• Supports Docker containers  
• Integrates deeply with core AWS services  
• Can run on EC2 or Fargate  
• Offers rolling deployments and update controls  
• Service discovery with AWS Cloud Map  
• Multi-platform support (Linux + Windows)  
• Supports task placement constraints and strategies  

---

## Launch Types

• EC2 Launch Type  
  o Run container workloads on a cluster of EC2 instances you manage  
  o Full control over instance types, AMIs, networking  
  o Suitable for predictable, steady workloads  

• Fargate Launch Type  
  o Serverless, no EC2 management  
  o Specify CPU and memory at task level  
  o AWS manages provisioning, scaling, patching  
  o Ideal for variable or bursty workloads  

---

## Clusters

• Logical grouping of tasks or services  
• Can include EC2 instances with ECS agent installed  
• Managed using ECS Console, CLI, or API  
• Supports CloudFormation for IaC provisioning  

---

## Tasks and Task Definitions

• Task Definition  
  o Blueprint for running containers  
  o Specifies Docker images, CPU, memory, networking, IAM roles, environment variables  
  o Supports multiple containers in a single task  

• Task  
  o Instantiation of a Task Definition  
  o Runs on EC2 or Fargate  

---

## Services

• Manage long-running tasks  
• Maintain desired count of running tasks  
• Supports rolling updates and blue/green deployments (via CodeDeploy)  
• Integrated with Elastic Load Balancing  
• Auto-scaling support via CloudWatch metrics  

---

## Capacity Providers

• Define how ECS runs tasks across launch types  
• Control scaling policies and weighting  
• Support EC2 Spot for cost optimization  

---

## Networking

• Integrated with Amazon VPC  
• Supports awsvpc networking mode for task-level ENIs  
• Security Groups and NACLs for traffic control  
• Load balancing via ALB, NLB, or CLB  

---

## Storage

• Supports Amazon EFS for persistent shared storage  
• Data volumes defined in task definitions  
• Ephemeral storage available per task  

---

## Monitoring and Logging

• CloudWatch Logs integration  
• Container log collection  
• CloudWatch metrics for CPU, memory, custom metrics  
• X-Ray integration for tracing  

---

## Security

• IAM roles for tasks, services, and clusters  

• Task Role  
  o Provides AWS API permissions to containers in the task  

• Task Execution Role  
  o Allows pulling images, writing logs, managing secrets  

• Supports KMS encryption  
• Private container registries supported via Secrets Manager  

---

## Integration with Other AWS Services

• AWS Fargate  
• Elastic Load Balancing  
• AWS App Mesh  
• Amazon CloudWatch  
• AWS X-Ray  
• AWS CodePipeline and CodeDeploy  
• Amazon ECR  
• Secrets Manager and Parameter Store  

---

## Pricing

• ECS has no additional charge  
• Pay for compute resources used  
  o EC2 instances  
  o Fargate vCPU + memory per second  

• Standard AWS charges apply for ALB, ECR, CloudWatch, etc.  

---

## Use Cases

• Microservices applications  
• Batch processing  
• Hybrid EC2 + Fargate workloads  
• Migrating Docker workloads to AWS  
• Event-driven container execution  

---

## Exam Tips

• ECS supports EC2 and Fargate launch types  
• Task Definition = blueprint; Task = running instance  
• Services manage scaling, load balancing, deployments  
• awsvpc networking = ENI per task  
• IAM Task Role + Task Execution Role = secure access  
• Capacity Providers support On-Demand, Spot, and Fargate  
• Fargate = serverless containers  
• ECS integrates with ALB, EFS, Secrets Manager, CloudWatch, X-Ray  

---

## Quick Summary

Amazon ECS is AWS’s fully managed container orchestration service supporting Docker workloads. It offers flexible deployment with EC2 and Fargate launch types, deep AWS integration for security and monitoring, and tools for scaling and managing container-based applications in production.

