# AWS Step Functions

AWS Step Functions is a fully managed service for building serverless workflows that coordinate multiple AWS services into business-critical applications.  
It allows you to design workflows as state machines with visual modelling, error handling, and service integrations.

---

## What It Is

• Fully managed workflow orchestration service  
• Visual design of serverless workflows  
• Coordinates multiple AWS services  

---

## Key Features

• Visual workflow editor for defining state machines  
• Supports Standard and Express Workflows  
• Built-in error handling, retries, and catchers  
• State input, output, and result manipulation with JSON Path  
• Service Integrations for over 200 AWS services  
• Wait states for delays or timeouts  
• Choice states for branching logic  
• Parallel execution of tasks  
• Execution history and detailed logging  

---

## Workflow Types

### Standard Workflows
• Long-running, durable, auditable  
• Supports executions up to 1 year  
• Exactly-once workflow execution  

### Express Workflows
• High-volume, short-duration workflows  
• Lower cost for high-frequency invocations  
• Executions up to 5 minutes  

---

## States and State Types

• Task State – Runs a single unit of work (Lambda, AWS service integration)  
• Choice State – Branching logic  
• Parallel State – Runs multiple branches simultaneously  
• Map State – Processes array items in parallel/sequentially  
• Wait State – Introduces delay or waits until a timestamp  
• Pass State – Passes input to output, adds static data  
• Succeed State – Marks successful completion  
• Fail State – Marks failure of execution  

---

## Service Integrations

• AWS Lambda  
• AWS Batch  
• AWS Glue  
• Amazon ECS and AWS Fargate  
• Amazon SageMaker  
• SNS and SQS  
• DynamoDB and S3  
• AWS API Gateway  
• Amazon EventBridge  
• AWS SDK integrations for direct service API calls  

---

## Error Handling and Retries

• Retry Policies:
– Configure retry intervals  
– Configure maximum attempts  

• Catchers:
– Capture errors and redirect workflow paths  

• Enables fault-tolerant, resilient workflow execution  

---

## State Input and Output

• InputPath – Select input portion  
• Parameters – Set parameters sent to a task  
• ResultSelector – Transform task results  
• ResultPath – Control where results are placed  
• OutputPath – Select output from the state  

---

## Execution Management

• View execution history in AWS Console  
• CloudWatch Logs for detailed traces  
• API support for updating and starting executions  
• Supports synchronous and asynchronous execution modes  

---

## Express Workflow Details

• Built for high-volume, event-driven workloads  
• Ideal for streaming analytics and data pipelines  
• Supports thousands of executions per second  
• Lower cost per execution  
• Max duration: 5 minutes  

---

## Standard Workflow Details

• Durable with execution history retained for 90 days  
• Supports human approval processes  
• Suitable for long-running jobs  
• Higher cost per state transition  

---

## Monitoring and Logging

• Amazon CloudWatch metrics and logs  
• View state machine execution results  
• Supports alarms and automated failure responses  

---

## Security

• IAM policies for Step Functions access control  
• Fine-grained permissions per state machine  
• VPC Endpoints for private access  
• Encryption of data in transit and at rest using AWS KMS  

---

## Pricing

• Standard Workflows: charged per state transition  
• Express Workflows: charged per execution and duration  
• Additional charges for AWS service calls and data transfer  

---

## Use Cases

• Microservice orchestration  
• Serverless application workflows  
• Data processing pipelines  
• Machine learning model training/deployment  
• ETL workflows with AWS Glue  
• Human approval workflows with Wait + Choice states  
• Error handling and retry orchestration  

---

## Best Practices

• Choose workflow type based on volume and duration  
• Use Choice and Parallel states to simplify complex logic  
• Implement retries and catchers for resilience  
• Use Wait states for delays and approvals  
• Secure workflows with IAM roles  
• Monitor using CloudWatch for errors and performance  

---

## Exam Tips

• Standard = long-running, durable  
• Express = high-volume, short-lived  
• Supports direct integrations with many AWS services  
• Visual state machine design  
• Built-in retries and error handling  
• IAM roles control access  
• JSON Path used for manipulating state input and output  

---

## Quick Summary

AWS Step Functions is a serverless orchestration service that coordinates AWS services and custom logic into resilient workflows.  
It supports Standard and Express Workflows, visual modelling, state machine design, error handling, and service integrations for a wide variety of use cases.

