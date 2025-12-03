# AWS Batch

AWS Batch is a fully managed batch processing service that efficiently runs hundreds to thousands of batch computing jobs.  
It dynamically provisions optimal compute resources (EC2, Spot, Fargate) based on job volume, no manual cluster management required.

---

## What It Is

• Fully managed batch computing service  
• Automatically provisions compute resources based on job queue demand  
• Supports EC2, Spot Instances, and Fargate for cost optimization  
• Integrates with Amazon ECS for containerized workloads  
• Scales up/down automatically based on queued jobs  
• Supports single, array, and multi-node parallel jobs  
• Fine-grained job dependencies and priorities  
• Integrated with CloudWatch for logging and monitoring  
• No additional service cost — pay only for compute and storage  

---

## Core Components

• Job – A single unit of work submitted to AWS Batch  
• Job Definition – Template defining Docker image, vCPU, memory, IAM role, retries  
• Job Queue – Holds submitted jobs and determines their priority  
• Compute Environment – Defines compute resources (EC2, Spot, Fargate)  

---

## Job Types

• Single Job – Standard task  
• Array Job – Run up to 10,000 parallel job copies with different parameters  
• Multi-Node Parallel Job – Distributed HPC workloads across multiple EC2 instances  

---

## Job States

• SUBMITTED – Job placed in queue  
• PENDING – Waiting for dependencies or resources  
• RUNNABLE – Ready to run  
• STARTING – Compute resources being provisioned  
• RUNNING – Job executing  
• SUCCEEDED – Completed successfully  
• FAILED – Terminated with errors  

---

## Job Scheduling and Dependencies

• Priority determined by job queue + compute environment  
• Supports job dependencies (run after parent job succeeds)  
• Works with array and multi-node jobs  
• Retry strategies + timeouts for resilient execution  

---

## Compute Environments

• Managed Compute Environment  
– AWS handles provisioning and scaling  
– Supports On-Demand or Spot Instances  

• Unmanaged Compute Environment  
– You maintain ECS clusters manually  

• Supports multiple instance types, Spot Fleet, and On-Demand  
• Allocation strategies:  
– BEST_FIT  
– BEST_FIT_PROGRESSIVE  
– SPOT_CAPACITY_OPTIMIZED  

---

## Integration with Other AWS Services

• Amazon ECS – Runs containerized jobs  
• Amazon ECR – Pulls Docker images  
• Amazon CloudWatch Logs – Stores and monitors logs  
• SNS / SQS – Notifications and triggers  
• AWS Lambda / Step Functions – Workflow orchestration  
• IAM – Job-level permissions  
• Amazon S3 – Common input/output storage  

---

## Monitoring and Logging

• CloudWatch metrics and alarms  
• Logs in CloudWatch Logs or S3  
• Track job history, retries, failures  
• Custom metrics for queue depth, duration, cost  

---

## Security

• IAM Roles for job execution + resource access  
• KMS to encrypt environment variables or sensitive data  
• VPC configuration for private networks  
• Supports EFS / FSx for shared storage  

---

## Pricing

• No extra charge for AWS Batch  
• Pay for EC2 / Fargate compute + storage  
• Significant savings with Spot Instances  
• CloudWatch Logs + data transfer billed separately  

---

## Use Cases

• Data processing pipelines and analytics  
• Machine learning model training or inference  
• Media rendering and transcoding  
• HPC simulations and scientific workloads  
• Financial modeling and risk analysis  
• ETL pipelines, nightly batch processing  

---

## Best Practices

• Use Managed Compute Environments for scaling  
• Use Spot Instances for cost-efficient workloads  
• Use Array Jobs to parallelize large workloads  
• Use least-privilege IAM roles  
• Implement retries + timeout strategies  
• Store large datasets in S3 and pass paths as environment variables  
• Use Step Functions or EventBridge to orchestrate workloads  

---

## Exam Tips

• AWS Batch automatically provisions/scales compute — no cluster setup  
• You only pay for compute + storage  
• Uses ECS to run containerized workloads  
• Supports EC2 On-Demand, Spot, Fargate  
• Job definitions store container + vCPU/memory + IAM + retries  
• Job queues determine priority  
• Managed compute environments handled by AWS  
• Array jobs run thousands of parallel tasks  
• Commonly integrated with Step Functions + CloudWatch  
• Ideal for long-running or parallel workloads  

---

## Quick Summary

AWS Batch is a serverless batch orchestration service that automates compute provisioning, job scheduling, scaling, and monitoring. It integrates deeply with ECS, CloudWatch, IAM, and S3, making it ideal for large-scale, cost-efficient, containerized or HPC workloads without managing infrastructure.

