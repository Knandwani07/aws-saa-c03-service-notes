# AWS Lambda 

---

## What It Is
• Serverless, event-driven compute service that runs code without provisioning servers  
• Automatically scales with incoming events  
• Pay only for **requests + compute time (ms-based)**  
• Supports multiple runtimes: Python, Node.js, Java, Go, C#, Ruby, PowerShell  
• Max execution time per invocation: **15 minutes**

---

## Key Features
• Fully managed, no infrastructure to maintain  
• Event-based execution from AWS services or custom apps  
• Per-millisecond billing  
• Multiple triggers + event orchestration  
• Supports Lambda Layers & container images  

---

## Triggers & Event Sources
• S3 (uploads/deletes)  
• DynamoDB Streams  
• Kinesis Data Streams  
• SNS, SQS  
• EventBridge  
• API Gateway (REST/WebSocket)  
• ALB for HTTP/HTTPS  
• Direct invocation via SDK/CLI  
• Event Source Mapping for SQS, Kinesis, DynamoDB  

---

## Execution Environment
• Isolated runtime environment per function  
• Memory: 128 MB → 10 GB  
• CPU scales with memory  
• /tmp storage up to **10 GB**  
• Environment variables supported  
• Lambda Layers for shared dependencies  

---

## Concurrency & Scaling
• Auto-scaling based on event volume  
• Default concurrency limit per account/region  
• **Reserved Concurrency** ensures guaranteed capacity  
• **Provisioned Concurrency** keeps functions warm (no cold starts)  

---

## Function Configuration
• Timeout: up to **15 minutes**  
• Memory, runtime, handler, environment variables  
• IAM Role attached to Lambda controls permissions  
• VPC support for private subnets  

---

## Deployment & Versioning
• Publish immutable **versions**  
• Use **aliases** for traffic shifting  
• Supports blue/green deployment with CodeDeploy  
• Deployment packages:
  - ZIP archives  
  - Container images (up to **10 GB** via ECR)**  

---

## Container Image Support
• Package Lambda as OCI-compatible container images  
• Store images in Amazon ECR  
• Use when dependencies are large or need custom OS libraries  

---

## Security
• IAM execution role defines resource permissions  
• Encrypt environment variables with KMS  
• VPC integration for private networking  
• Supports Secrets Manager & Parameter Store  

---

## Monitoring & Logging
• CloudWatch Logs for function logs  
• CloudWatch Metrics for invocations, errors, throttles, duration  
• X-Ray for tracing and performance diagnostics  
• CloudTrail logs for API activity  

---

## Pricing
• First **1M requests/month free**  
• Pay for:
  - Requests  
  - Compute time (GB-seconds)  
• Extra for Provisioned Concurrency  
• Data transfer costs apply  

---

## Use Cases
• Real-time file processing (S3)  
• Stream processing (Kinesis, DynamoDB Streams)  
• Serverless REST APIs with API Gateway  
• Automation tasks (cron with EventBridge)  
• IoT/mobile backends  
• Lightweight compute jobs  

---

## Integration with AWS Services
• API Gateway → Serverless APIs  
• S3 → Trigger on object events  
• DynamoDB Streams → Change data capture  
• Kinesis → Stream ingestion  
• SQS/SNS → Async processing  
• EventBridge → Event-driven architectures  
• Step Functions → Workflow orchestration  

---

## Best Practices
• Use environment variables for config  
• Keep functions small and single-purpose  
• Optimize package size for faster cold starts  
• Use Provisioned Concurrency for low-latency apps  
• Apply least-privilege IAM policies  
• Use Lambda Layers for common libraries  
• Monitor metrics and set CloudWatch alarms  

---

## Exam Tips
• Lambda = serverless compute with automatic scaling  
• Billed per request + execution time  
• Max runtime = 15 minutes  
• Triggered by dozens of AWS services  
• Uses IAM roles for permissions  
• Supports container images  
• Use Provisioned Concurrency to minimize cold starts  
• CloudWatch + X-Ray for monitoring and tracing  
• Works closely with API Gateway, S3, DynamoDB, Kinesis, EventBridge  

---

## Quick Summary
AWS Lambda is a serverless, event-driven compute service that automatically scales and only charges for actual compute usage. Integrated with most AWS services, supports multiple runtimes, offers strong security and monitoring features, and is ideal for building efficient, scalable, event-based and API-driven applications.
