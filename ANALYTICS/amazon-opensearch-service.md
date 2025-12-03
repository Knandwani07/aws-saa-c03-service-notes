# Amazon OpenSearch

Amazon OpenSearch Service is a fully managed service that makes it easy to deploy, operate, and scale OpenSearch and legacy Elasticsearch clusters in the AWS Cloud.
It is widely used for search, log analytics, real-time monitoring, and operational dashboards.

---

## What It Is

• Fully managed service for OpenSearch and Elasticsearch  
• Supports versions of OpenSearch and legacy Elasticsearch (up to 7.10)  
• In-place version upgrades  
• Includes OpenSearch Dashboards and legacy Kibana  
• Integrates with CloudWatch, Kinesis, S3, and other AWS services  
• Provides domain-level security and fine-grained access control  
• Supports encryption at rest and node-to-node encryption  
• VPC support for secure, isolated network access  
• Auto-Tune for performance optimization  
• Ultrawarm and cold storage tiers for cost-efficient storage  

---

## Core Concepts

• **Domain:** OpenSearch/Elasticsearch cluster  
• **Index:** Collection of documents  
• **Document:** Basic JSON unit of data  
• **Shard:** Horizontal data partition  
• **Replica:** Copy of a shard for fault tolerance  

---

## Deployment and Scaling

• Scale clusters by adjusting instance count and types  
• Supports data nodes, dedicated master nodes, Ultrawarm nodes, cold storage  
• Automated snapshots to S3 for backups  
• Manual and scheduled snapshots supported  
• Multi-AZ deployments for high availability  

---

## Ultrawarm and Cold Storage

• **Ultrawarm:** Cost-effective tier for read-only, infrequently accessed data  
• **Cold Storage:** Lowest-cost long-term storage tier  
• Seamless search across hot, Ultrawarm, and cold tiers  

---

## Security

• IAM policies for domain-level access control  
• Fine-grained access control (OpenSearch security plugin)  
• Cognito integration for dashboard authentication  
• Encryption at rest with AWS KMS  
• Node-to-node TLS encryption  
• HTTPS for in-transit encryption  
• VPC support for private connectivity  

---

## Monitoring and Logging

• Integrated with Amazon CloudWatch for metrics and alarms  
• Detailed logs through CloudWatch Logs  
• Slow logs for search and indexing performance tuning  
• Audit logs for compliance  
• CloudTrail for API activity logging  

---

## Data Ingestion

Supports ingestion using:  
• Amazon Kinesis Data Firehose  
• Logstash  
• Fluentd  
• Beats  
• Custom ingestion pipelines  

Also supports OpenSearch ingest nodes for processing pipelines.

---

## Querying and Analytics

• Full-text search  
• Aggregations for analytics  
• SQL support  
• PPL (Piped Processing Language)  
• OpenSearch Dashboards for visualization  

---

## Integrations

• CloudWatch – monitoring and alerts  
• Kinesis Data Firehose – streaming ingestion  
• AWS Lambda – serverless ingestion pipelines  
• Amazon S3 – snapshots and cold storage  
• AWS Cognito – authentication for dashboards  

---

## Use Cases

• Application search  
• Log and event analytics  
• Infrastructure monitoring  
• SIEM workloads  
• Real-time application performance monitoring  
• Business and operational dashboards  

---

## Pricing

• Charges based on instance hours, storage, and data transfer  
• Ultrawarm and cold tiers reduce cost for older data  
• Data transfer within the same region is free for ingestion  
• Snapshot storage in S3 billed separately  

---

## Best Practices

• Choose appropriate instances and storage tiers  
• Use Ultrawarm/Cold tiers for historical data  
• Enable automated snapshots  
• Apply fine-grained access control and encryption  
• Monitor performance with CloudWatch and slow logs  
• Scale clusters based on ingestion and query demands  

---

## Exam Tips

• Fully managed service for OpenSearch and Elasticsearch  
• Use cases: log analytics, real-time search, monitoring  
• Integrates with Firehose, CloudWatch, Cognito  
• Ultrawarm/Cold tiers = cost-effective long-term retention  
• Security: encryption at rest, node-to-node encryption, IAM  
• Fine-grained access control using OpenSearch security plugin  
• Automated snapshots stored in S3  
• VPC support for secure access  

---

## Quick Summary

Amazon OpenSearch Service is AWS’s managed search and analytics platform supporting OpenSearch and legacy Elasticsearch.
It offers real-time search, log analytics, operational monitoring, and dashboards with deep AWS integration, strong security, and scalable architecture.

