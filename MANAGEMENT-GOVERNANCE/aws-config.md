# AWS Config

---

## What It Is

AWS Config is a fully managed service that tracks, records, and evaluates the configuration of AWS resources. It provides continuous monitoring, compliance evaluation, historical configuration data, and automated remediation to maintain governance and security across your AWS environment.

---

## Key Features

• Records configuration changes of supported AWS resources  
• Captures point-in-time snapshots and change histories  
• Evaluates resources against compliance rules  
• Maintains full configuration history for auditing  
• Delivers snapshots and notifications to S3 and SNS  
• Integrates with AWS Organizations for multi-account governance  

---

## Configuration Recorder

• Core component of AWS Config  
• Records changes to supported AWS resources  
• Must be enabled to capture configuration changes  
• Can record all resources or only selected types  

---

## Configuration Items (CIs)

• Represent a resource’s configuration at a given time  
• Include metadata, relationships, and config details  
• Delivered to S3 in JSON format  

---

## Resource Inventory

• Consolidated view of all recorded AWS resources  
• Searchable inventory  
• Tracks resource relationships (e.g., EC2 → VPC)  

---

## Configuration History

• Detailed history of configuration changes  
• Useful for audits and troubleshooting  
• Stored in S3 for long-term retention  

---

## Configuration Snapshots

• Point-in-time view of all resource configurations  
• Delivered to S3  
• Used for compliance and audit reporting  

---

## AWS Config Rules

• Define desired configurations for resources  
• Continuously evaluate resources against these rules  
• AWS Managed Rules – pre-built compliance checks  
• Custom Rules – user-defined (often Lambda-powered)  
• Triggered on configuration changes or periodically  
• Non-compliant resources are flagged  

---

## Remediation

• Automates fixing non-compliant resources  
• Uses Systems Manager Automation runbooks  
• Can run automatically or manually  
• Ensures ongoing compliance  

---

## Aggregators

• Combine data across multiple accounts and regions  
• Provide central visibility into compliance posture  
• Integrate with AWS Organizations  

---

## Integration with AWS Organizations

• Enforces consistent policies across all accounts  
• Organization-wide recording and rule evaluation  
• Central governance for large environments  

---

## Delivery Channels

• Define S3 bucket and SNS topic for Config data  
• Deliver snapshots, configuration history, and notifications  
• Support KMS encryption for secure data storage  

---

## Security and Access Control

• IAM controls access to AWS Config resources  
• KMS encryption for configuration files in S3  
• CloudWatch Logs integration for monitoring  

---

## Pricing

• Charged per configuration item recorded  
• Additional charges for rule evaluations  
• Aggregator usage billed for multi-account/region queries  
• S3 storage charges for configuration data  

---

## Use Cases

• Compliance auditing and security analysis  
• Continuous configuration monitoring  
• Operational troubleshooting and resource tracking  
• Multi-account governance and change management  
• Automated policy enforcement  

---

## Best Practices

• Enable AWS Config in all regions  
• Use Managed + Custom Rules for compliance  
• Aggregate data across accounts with Organizations  
• Automate remediation for high-priority issues  
• Store snapshots/history in secured, versioned S3 buckets  
• Integrate with SNS/CloudWatch for alerting  

---

## Exam Tips

• Tracks and evaluates resource configurations over time  
• Managed + Custom Rules enforce compliance  
• Aggregators provide multi-account visibility  
• Delivers snapshots/history to S3  
• SNS + CloudWatch Logs for notifications/monitoring  
• Automated remediation via SSM Automation  
• Strong integration with AWS Organizations  

---

## Quick Summary

AWS Config provides continuous monitoring, configuration tracking, compliance evaluation, and automated remediation. It delivers a complete historical record of resource changes and enforces governance across single- or multi-account AWS environments.

