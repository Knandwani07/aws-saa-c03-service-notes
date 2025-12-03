# AWS CloudTrail

---

## What It Is

AWS CloudTrail is a service that enables governance, compliance, and operational and risk auditing of your AWS account. It records account activity and API calls across AWS services, delivering log files to Amazon S3, CloudWatch Logs, or CloudWatch Events.

---

## Key Features

• Records AWS Management Console actions, AWS SDKs, command-line tools, and other AWS services API calls  
• Tracks who did what, when, and from where in your AWS account  
• Delivers event history to S3 buckets for auditing and analysis  
• Integrates with CloudWatch Logs for real-time monitoring and alarms  
• Integrates with Amazon EventBridge (formerly CloudWatch Events) to automate responses to events  

---

## Events and Trails

• An event represents a single AWS API call, including request parameters and response elements  
• Trails are configurations that specify how events are logged and delivered  
• Single Region or Multi-Region Trails  
• Supports logging for all AWS Regions in an account  
• Management Events (control plane) record operations on AWS resources  
• Data Events (data plane) record resource operations like S3 object-level actions and Lambda function invocations  

---

## Types of Events

• Management Events: By default, includes Read and Write operations for resource configuration  
• Data Events: Must be explicitly enabled, e.g., S3 GetObject, PutObject, Lambda Invoke  
• Insights Events: Identify unusual operational activity (e.g., high rate of API errors)  

---

## Trails Configuration

• Can have multiple trails per account  
• Apply to single Region or all Regions  
• Event logs delivered to S3 bucket specified in trail configuration  
• Optional integration with CloudWatch Logs for near real-time monitoring  
• Supports encryption of logs with AWS KMS  

---

## CloudTrail Event History

• Provides 90 days of management event history for free  
• Can view, search, and download events in the AWS console  
• Useful for viewing recent account activity without setting up a trail  

---

## CloudTrail Insights

• Analyses write management events to detect unusual activity  
• Detects spikes in API call volume or error rates  
• Provides Insight Events with details about the anomaly  
• Helps identify security issues or operational problems  

---

## Integration with Other AWS Services

• Amazon S3 for storing logs  
• AWS CloudWatch Logs for real-time analysis and alarms  
• Amazon EventBridge for automating workflows and security responses  
• AWS Lambda to automatically respond to specific events  
• AWS Organizations for organization-level trails covering all member accounts  

---

## Organization Trails

• AWS Organizations can create a trail that applies to all accounts in the organization  
• Centralized logging for governance and compliance  
• Prevents member accounts from disabling logging  

---

## Security and Access Control

• Logs can be encrypted with AWS KMS for secure storage  
• IAM policies control access to CloudTrail logs and settings  
• Supports bucket policies and S3 ACLs for secure delivery of logs  

---

## Pricing

• Viewing CloudTrail Event History (last 90 days of management events) is free  
• First copy of management events recorded in a trail is free  
• Charges apply for additional copies, data events, and Insights events  
• Storage costs for S3 and optionally CloudWatch Logs ingestion and storage  

---

## Best Practices

• Always enable CloudTrail in all Regions to ensure full coverage  
• Use organization trails in AWS Organizations for centralized auditing  
• Enable log file validation to ensure log integrity  
• Enable encryption using AWS KMS for secure log storage  
• Store logs in a dedicated S3 bucket with strict access controls  
• Integrate with CloudWatch Logs and EventBridge for real-time alerting and automated responses  
• Use Insights for detecting anomalous API activity  

---

## Exam Tips

• CloudTrail records all API calls made in your account, including from the console, SDKs, CLI, and other AWS services  
• Delivers logs to S3, integrates with CloudWatch Logs for monitoring and alarms  
• Management Events include control plane operations (e.g., creating resources)  
• Data Events must be explicitly enabled (e.g., S3 object-level actions, Lambda invocations)  
• Supports organization-wide trails in AWS Organizations  
• Insights detect unusual API activity patterns  
• Security best practices include encryption with KMS and log file validation  

---

## Quick Summary

AWS CloudTrail is the essential AWS service for auditing and compliance, recording API activity across your account and delivering logs to S3 for analysis. It supports real-time monitoring via CloudWatch, integrates with EventBridge for automation, and offers advanced features like Insights for detecting anomalies.

