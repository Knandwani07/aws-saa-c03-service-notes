# Amazon Keyspaces (for Apache Cassandra)

---

## What It Is

• Fully managed, serverless, and scalable Apache Cassandra–compatible database service  
• Designed for high availability, durability, and low-latency performance  
• Serverless, automatically scales up/down based on traffic  
• No need to provision, patch, or manage Cassandra clusters  
• Compatible with Cassandra Query Language (CQL) and drivers  

---

## Key Benefits

• Eliminates operational overhead of managing Cassandra clusters  
• Serverless scaling, pay only for what you use  
• Automatic replication across multiple AZs for fault tolerance  
• Fully managed backup, patching, and maintenance  
• Strong consistency and flexible read/write options  
• Seamless integration with AWS ecosystem  

---

## Architecture and Deployment

• Fully managed, no EC2 or cluster provisioning needed  
• Data automatically replicated across 3 Availability Zones  
• Supports single-region deployments with multi-AZ redundancy  
• CQL-compatible endpoint, no driver code changes required  
• Integrates with AWS Identity and Access Management (IAM)  
• Serverless: scales partitions and throughput automatically  

---

## High Availability and Durability

• Multi-AZ replication for fault tolerance  
• Durable writes, all data written to 3 replicas across AZs  
• No downtime during scaling or patching  
• Highly available reads and writes even during node failures  
• Point-in-time recovery (PITR) up to 35 days  

---

## Performance and Scaling

• On-demand capacity mode: scales automatically with workload  
• Provisioned capacity mode: manually define read/write throughput  
• Latency in single-digit milliseconds  
• Automatic load balancing and partition management  
• No manual resharding required like traditional Cassandra  

---

## Data Security

• Encryption at rest with AWS KMS  
• Encryption in transit using TLS  
• IAM for fine-grained access control  
• VPC endpoints via AWS PrivateLink for private connectivity  
• Audit logging using AWS CloudTrail  
• No direct SSH or node-level access  

---

## Backup and Restore

• Continuous backups with Point-in-Time Recovery (PITR)  
• Manual on-demand backups available  
• Data stored redundantly across AZs  
• Backups can be restored to new tables  
• No impact on performance during backup operations  

---

## Monitoring and Management

• Integrated with Amazon CloudWatch for metrics  
• AWS CloudTrail for auditing API activity  
• No need to monitor nodes or repair clusters  
• Manage via AWS Console, CLI, or SDKs  
• CQL-compatible tools like cqlsh can connect  

---

## Integration with AWS Services

• Integrates with Lambda, Kinesis, Glue, Data Pipeline, and S3  
• Use with Amazon MSK for streaming writes  
• Connect via Amazon VPC endpoints  
• Integrates with AWS CloudFormation, Terraform, and CDK for IaC  
• Ideal for hybrid or multi-region architectures with data replication  

---

## Use Cases

• IOT data ingestion and time-series data  
• Session and user profile storage  
• High-velocity log data and clickstreams  
• Real-time recommendation systems  
• Catalog and product metadata storage  
• Event tracking and telemetry systems  

---

## Pricing

• Pay per request for reads/writes (on-demand mode)  
• Provisioned mode: pay for configured capacity  
• PITR storage billed separately  
• Data transfer within the same AWS Region is free  
• Costs for backup storage and restores apply  

---

## Best Practices

• Use on-demand mode for unpredictable workloads  
• Use provisioned mode for steady traffic to control costs  
• Design tables with a well-planned partition key for even load distribution  
• Enable PITR for production data protection  
• Restrict access via IAM and VPC PrivateLink  
• Monitor performance with CloudWatch metrics (throttling, latency)  
• Avoid wide partitions distribute writes evenly  

---

## Exam Tips

• Serverless Cassandra service, no cluster management required  
• Supports CQL and Cassandra drivers  
• Automatically replicates data across 3 AZs  
• Encryption at-rest and in-transit supported by default  
• Two capacity modes: On-Demand & Provisioned  
• PITR available for up to 35 days  
• No VPC deployment access via PrivateLink if needed  
• Great for scalable, low-latency, NoSQL workloads  

---

## Quick Summary

Amazon Keyspaces is a fully managed, serverless, and highly available Cassandra-compatible database designed for massive scalability, low-latency workloads, and seamless AWS integration, ideal for use cases like IoT, session management, and real-time analytics without the hassle of cluster administration.

