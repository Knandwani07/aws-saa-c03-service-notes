# Amazon DocumentDB

---

## What It Is

Amazon DocumentDB (with MongoDB compatibility) is a fully managed document database service designed to store, query, and index JSON-like documents. It is optimized for scalability, availability, and performance, and is used for semi-structured data applications that require flexible schemas, such as content management systems, catalogs, and user profiles.

---

## Key Features

• Fully managed document database service  
• Compatible with MongoDB APIs (version 3.6, 4.0, 5.0)  
• Designed for high performance, scalability, and availability  
• Stores semi-structured JSON-like documents  
• Automatically scales storage up to 64 TB  
• Built-in security, backup, and monitoring features  
• Offers automatic failover, backups, and patching  
• Integrates with AWS services like CloudWatch, IAM, and Secrets Manager  

---

## Architecture and Performance

• Separates compute and storage layers  
• Each cluster has one primary instance (read/write) and up to 15 replicas (read-only)  
• Six copies of data replicated across three Availability Zones  
• Compute instances are based on Amazon EC2  
• Automatically scales storage in 10 GB increments as needed  
• Supports millions of reads per second with low latency  
• Uses a purpose-built storage engine optimized for document workloads  

---

## Data Model

• Uses a flexible, schema-less JSON-like format  
• Collections contain documents, similar to tables in a relational database  
• Supports embedded documents and arrays for nested data  
• Ideal for applications with changing or dynamic data structures  

---

## MongoDB Compatibility

• Supports MongoDB drivers and tools  
• Compatible with popular MongoDB APIs, including find, insert, update, and delete  
• Some features such as capped collections and change streams may not be fully supported  
• Use AWS DMS to migrate data from existing MongoDB databases  

---

## Scaling and Availability

• Horizontal read scaling with up to 15 read replicas  
• Automatic failover to replicas during primary failure  
• Storage auto-scales without downtime  
• Multi-AZ deployments ensure high availability  
• Supports replica lag monitoring and alerts  

---

## Backups and Restore

• Continuous backups to Amazon S3  
• Point-in-time recovery (PITR) up to 35 days  
• Manual snapshots can be taken and retained as needed  
• Snapshots can be shared across AWS accounts or copied to other regions  

---

## Security

• Encryption at rest using AWS KMS  
• Encryption in transit using TLS  
• VPC deployment for network-level isolation  
• IAM integration for resource-level access control  
• AWS Secrets Manager integration for secure credentials management  
• Audit logging supported using CloudWatch Logs  

---

## Monitoring and Management

• Amazon CloudWatch for performance metrics and alarms  
• Enhanced Monitoring for detailed OS-level metrics  
• Event notifications via Amazon SNS  
• Amazon CloudTrail integration for API activity tracking  
• Fully managed backups, patching, and failover by AWS  

---

## Integration with AWS Services

• AWS DMS for data migration  
• CloudWatch for monitoring and logging  
• Secrets Manager for managing database credentials  
• IAM for access control  
• VPC for secure networking  
• AWS Glue for data transformation and analytics  

---

## Use Cases

• Content management systems  
• Product catalogs and inventory  
• User profiles and personalization  
• Mobile and web applications with flexible schemas  
• Semi-structured data ingestion and processing  

---

## Exam Tips

• Amazon DocumentDB is MongoDB-compatible but not a native MongoDB engine  
• Ideal for applications needing flexible, schema-less document storage  
• Not a drop-in replacement for every MongoDB feature  
• Multi-AZ support with six-way data replication provides high availability  
• Automatically scales storage without downtime  
• Supports up to 15 read replicas for horizontal scaling  
• Fully managed by AWS including patching, backups, and failover  
• Use IAM and VPC for security and access control  
• Encryption at rest and in transit is enabled by default  
• Integration with CloudWatch and CloudTrail for monitoring and auditing  

---

## Quick Summary

Amazon DocumentDB is a scalable, fully managed document database service designed for modern applications that need flexible data models. With MongoDB compatibility, high availability, automated scaling, and integrated AWS security and monitoring, it is ideal for content-rich, semi-structured workloads that require low-latency and resilience.

