# Amazon Aurora
---

## What It Is

Amazon Aurora is a fully managed, MySQL- and PostgreSQL-compatible relational database engine built for the cloud. It delivers the performance and availability of high-end commercial databases at a lower cost, while being fully integrated with AWS services.

---

## Key Features

• MySQL- and PostgreSQL-compatible  
• Up to 5x faster than standard MySQL and 3x faster than standard PostgreSQL  
• Storage automatically scales in 10GB increments up to 128TB  
• Fault-tolerant and self-healing storage system with six-way replication across three Availability Zones  
• Continuous backups to Amazon S3  
• Automatic, incremental backups with point-in-time recovery  
• Database cloning for fast, cost-effective copies  
• Supports Global Databases for low-latency global reads and disaster recovery  
• Integrated with AWS monitoring and security services  

---

## Aurora Cluster Architecture

• Consists of a cluster volume that spans multiple AZs  
• One primary instance for read/write operations  
• Up to 15 Aurora Replicas for read scaling with low replication lag  
• Reader endpoint automatically load-balances read traffic  
• Failover to a replica typically takes less than 30 seconds  

---

## Aurora Storage

• Distributed, fault-tolerant, self-healing storage  
• Automatically replicated six ways across three AZs  
• Continuous backup to Amazon S3 without affecting performance  
• Supports storage auto-scaling up to 128TB  

---

## Aurora Replicas

• Provide read scalability  
• Up to 15 Aurora Replicas per cluster  
• Replication lag typically under 100 milliseconds  
• Supports cross-Region replication with Global Databases  
• Failover targets for high availability  

---

## Backups and Snapshots

• Automated backups with configurable retention (up to 35 days)  
• Point-in-time recovery to any second during retention period  
• Manual snapshots retained until deleted  
• Snapshots can be shared with other AWS accounts or copied across regions  

---

## Global Databases

• Designed for globally distributed applications  
• Single primary Region with read-only secondary Regions  
• Cross-region replication with typical lag under 1 second  
• Supports fast recovery in case of regional outages  
• Enables low-latency global reads  

---

## Aurora Serverless v1

• On-demand, auto-scaling configuration  
• Automatically starts, stops, and scales based on workload  
• Ideal for variable or unpredictable workloads  
• Charges based on actual usage (Aurora Capacity Units)  
• Supports MySQL-compatible edition  

---

## Aurora Serverless v2

• Fine-grained, instant scaling with minimal latency  
• Supports even higher workloads and connections  
• Works with both MySQL- and PostgreSQL-compatible editions  
• More production-ready and scalable than v1  

---

## Performance and Scaling

• Up to 64 vCPUs and hundreds of GBs of RAM per instance  
• Storage and compute scale independently  
• Supports read scaling with Aurora Replicas  
• Write scaling can be improved with partitioning at the application layer  
• Integrated with Amazon RDS Proxy for connection pooling  

---

## Security

• Encryption at rest using AWS KMS  
• Encryption in transit using SSL/TLS  
• VPC isolation and subnet-level security  
• IAM integration for management  
• Database authentication with IAM for MySQL and PostgreSQL  
• Audit logging for tracking database activity  
• Integration with AWS Secrets Manager for managing credentials  

---

## Monitoring and Management

• Amazon CloudWatch for metrics and alarms  
• Enhanced Monitoring for OS-level metrics  
• Performance Insights for analysing query performance  
• Automated backups, patching, and maintenance  
• Database cloning for rapid creation of test and development environments  

---

## Integration with Other AWS Services

• AWS Lambda for triggers and integrations  
• AWS DMS for migrations to Aurora  
• AWS Secrets Manager for credential management  
• AWS Backup for centralized backup management  
• RDS Proxy for improving application scalability and resiliency  

---

## Pricing

• Charged per instance hour based on instance type  
• Aurora Serverless charged based on Aurora Capacity Units (ACUs)  
• Storage billed per GB per month  
• I/O requests billed per million requests  
• Backup storage beyond the allocated database size incurs additional charges  
• Cross-region replication charges for Global Databases  

---

## Use Cases

• Enterprise-grade applications requiring high availability and durability  
• SaaS applications needing high performance at scale  
• Global applications with low-latency read requirements  
• Variable workloads with unpredictable usage patterns (Aurora Serverless)  
• Online transaction processing (OLTP) systems  

---

## Exam Tips

• Aurora is MySQL- and PostgreSQL-compatible but AWS-built for cloud performance  
• Supports automatic storage scaling up to 128TB  
• Six-way replication across three AZs ensures durability  
• Multi-AZ by design with fast failover  
• Aurora Replicas provide read scalability with minimal lag  
• Global Databases enable low-latency global reads and DR  
• Aurora Serverless is ideal for infrequent, unpredictable workloads  
• Supports encryption at rest (KMS) and in transit (SSL/TLS)  
• Point-in-time recovery and continuous backups to S3  
• Database cloning for development and testing without affecting production workloads  

---

## Quick Summary

Amazon Aurora is AWS’s high-performance, highly available relational database engine compatible with MySQL and PostgreSQL. It offers advanced features like storage auto-scaling, fault-tolerant replication, read replicas, global databases, and serverless deployments, making it an ideal choice for modern, cloud-native applications requiring scalability, durability, and high availability.

