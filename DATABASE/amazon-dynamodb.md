# Amazon DynamoDB

---

## Overview

• Fully managed, serverless NoSQL database (key-value and document model)  
• Single-digit millisecond latency at any scale  
• Designed for high availability, durability, and scalability  
• Automatically replicates data across multiple AZs  
• Integrated with other AWS services (Lambda, AppSync, Glue, etc.)  

---

## Core Concepts

• Table: Collection of items (like a relational DB table)  
• Item: Individual record (like a row)  
• Attribute: Field within an item (like a column)  
• Primary Key:  
- Partition Key: Determines data partition  
- Partition + Sort Key: Enables sorting and querying within the partition  

---

## Indexes

• Global Secondary Index (GSI):  
- Query on different attributes  
- Supports different partition/sort keys  

• Local Secondary Index (LSI):  
- Same partition key, different sort key  
- Must be defined at table creation  

---

## Capacity Modes

• On-Demand:  
- No capacity planning  
- Scales automatically based on traffic  

• Provisioned:  
- Manually define RCUs/WCUs  
- Can enable Auto Scaling  

---

## Performance Optimization

• DynamoDB Accelerator (DAX):  
- In-memory cache  
- Reduces read latency to microseconds  

• Adaptive Capacity:  
- Automatically adjusts throughput for imbalanced workloads  

---

## Data Consistency

• Eventually Consistent Reads (default, more scalable)  
• Strongly Consistent Reads (read after write consistency)  
• Transactions:  
- ACID-compliant operations across multiple items/tables  

---

## Streams

• Capture item-level changes (insert, update, delete)  
• Can trigger AWS Lambda for real-time processing  
• Provides exactly-once event delivery  

---

## Backup and Restore

• On-Demand Backup: Full backups, manual  
• Point-in-Time Recovery (PITR):  
- Continuous backup up to 35 days  
- Restore to any second within the window  

---

## Security

• Encryption at Rest: AWS KMS integration  
• IAM Policies: Fine-grained access control  
• VPC Endpoints: Private connectivity without Internet exposure  

---

## Global Tables

• Multi-Region, multi-active replication  
• Low-latency global access  
• Automatic conflict resolution  
• Supports disaster recovery across regions  

---

## Integration

• Lambda: Trigger from Streams  
• AppSync: GraphQL API layer for DynamoDB  
• Glue/Data Pipeline: ETL and data movement  
• CloudWatch: Monitoring and alerting  
• Backup: Centralized backup through AWS Backup  
• Kinesis Firehose: Data streaming to analytics tools  

---

## Pricing

• Charges based on:  
- Read/Write capacity (or On-Demand usage)  
- Storage (per GB/month)  
- Streams, backups, PITR, DAX, Global Tables billed separately  

---

## Use Cases

• Real-time bidding platforms  
• Gaming leaderboards  
• Shopping carts  
• IoT telemetry data  
• Mobile app backends  
• User preference/profile storage  

---

## Best Practices

• Use On-Demand mode for unpredictable traffic  
• Partition keys should distribute traffic evenly  
• Enable Auto Scaling for provisioned workloads  
• Use DAX for frequently accessed read-heavy data  
• Secure with IAM, KMS, and VPC Endpoints  
• Use Streams + Lambda for event-driven architecture  

---

## Exam Tips

• Choose On-Demand to avoid provisioning headaches  
• LSI = must be defined at creation, GSI = can be added anytime  
• Streams trigger Lambda, great for real-time applications  
• Global Tables enable low-latency writes and reads across regions  
• Transactions enable coordinated writes with ACID compliance  
• PITR enables second-level restore up to 35 days  
• Know difference between Eventually and Strongly Consistent Reads  

---

## Quick Summary

Amazon DynamoDB is a fully managed, serverless NoSQL database delivering high performance, scalability, and resilience. It offers on-demand and provisioned capacity, automatic multi-AZ replication, DAX for caching, PITR for recovery, and global tables for low-latency, multi-region access. Ideal for real-time, serverless, and globally distributed applications.

