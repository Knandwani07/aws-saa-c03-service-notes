# Amazon RDS

---

## What It Is

Amazon RDS is a managed relational database service that makes it easier to set up, operate, and scale databases in the cloud. It automates tasks such as provisioning, patching, backup, recovery, and scaling.

---

## Supported Database Engines

• Amazon Aurora (MySQL and PostgreSQL compatible)  
• PostgreSQL  
• MySQL  
• MariaDB  
• Oracle  
• Microsoft SQL Server  

---

## Key Features

• Managed database service that handles maintenance tasks  
• Automated backups with point-in-time recovery  
• Automated software patching  
• Automatic failure detection and recovery  
• Multi-AZ deployments for high availability  
• Read replicas for scaling read traffic  
• Encryption at rest using AWS KMS  
• Encryption in transit using SSL/TLS  
• Easy scaling of compute and storage  

---

## Deployment Options

• Single-AZ: Single database instance in one Availability Zone  

• Multi-AZ: Synchronous standby replica in another AZ for high availability  
- Automated failover to standby on failure  

• Read Replicas: Asynchronous replication for read-heavy workloads  
- Supports up to 5 read replicas for MySQL, MariaDB, PostgreSQL  
- Aurora supports up to 15 read replicas with low-latency replication  

---

## Storage Options

• General Purpose (SSD)  
- Cost-effective, balanced performance  
- Suitable for most workloads  

• Provisioned IOPS (SSD)  
- High-performance storage for critical workloads  
- Consistent low latency and high throughput  

• Magnetic (legacy)  
- Previous-generation storage, limited use cases  

---

## Backups and Snapshots

• Automated Backups  
- Enabled by default  
- Retention period configurable from 0 to 35 days  
- Supports point-in-time recovery  

• Manual Snapshots  
- User-initiated  
- Retained until explicitly deleted  
- Can be shared with other AWS accounts or copied to other regions  

---

## Maintenance and Patching

• AWS manages patching of the database engine  
• Can specify maintenance window  
• Minor version upgrades can be applied automatically or manually  

---

## Monitoring and Metrics

• Amazon CloudWatch metrics for CPU, memory, storage, IOPS, connections  
• Enhanced Monitoring for OS-level metrics  
• Performance Insights for query performance analysis and optimization  

---

## Security

• Encryption at rest using AWS KMS  
• Encryption in transit using SSL/TLS  
• IAM integration for management access  
• VPC support for network isolation  
• Security groups to control inbound/outbound traffic  
• Supports AWS Secrets Manager for credential management  
• Option to enforce IAM Database Authentication (MySQL and PostgreSQL)  

---

## Pricing

• Pay for instance hours (on-demand or reserved instances)  
• Storage and I/O requests billed separately  
• Backups stored in S3 are free up to the allocated storage size  
• Data transfer costs may apply  

---

## Aurora Highlights

• AWS-built, MySQL and PostgreSQL-compatible engine  
• Up to 5x faster than standard MySQL, 3x faster than PostgreSQL  
• Storage automatically grows up to 128 TB  
• Six-way replication across three AZs  
• Automated failover, continuous backups to S3  
• Aurora Serverless: Auto-scales capacity based on load  
• Global Databases for low-latency global reads and disaster recovery  

---

## Use Cases

• Web and mobile applications  
• Enterprise applications  
• E-commerce platforms  
• Business analytics  
• SaaS applications requiring relational data storage  

---

## Exam Tips

• Use multi-AZ for high availability and automatic failover  
• Read Replicas are for scaling reads and disaster recovery  
• Aurora offers better performance and high availability with low replication lag  
• IAM Database Authentication adds IAM-based access control  
• Backups support point-in-time recovery  
• Encryption at rest uses KMS, in transit uses SSL/TLS  
• Performance Insights helps identify slow queries  
• Storage Auto Scaling automatically increases storage as needed  
• Aurora Global Databases support globally distributed applications  
• AWS handles maintenance tasks such as backups and patching  

---

## Quick Summary

Amazon RDS is a managed service that simplifies deploying, operating, and scaling relational databases in AWS. It supports multiple database engines, offers automated backups, multi-AZ deployments for high availability, read replicas for scaling, and encryption for data security. Aurora, AWS’s proprietary database engine, offers additional performance and scaling benefits.

