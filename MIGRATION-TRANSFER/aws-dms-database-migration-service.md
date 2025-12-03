# AWS Database Migration Service (DMS)

---

## What It Is
AWS Database Migration Service (AWS DMS) is a managed service for migrating databases to AWS securely and with **minimal downtime**. It supports **homogeneous** (Oracle→Oracle) and **heterogeneous** (Oracle→Aurora) migrations, continuous replication using **CDC**, and works with on-premises, EC2-based, or cloud databases.

---

## Key Features

• One-time migration + ongoing continuous replication  
• Supports homogeneous & heterogeneous migrations  
• Schema + data migration (with AWS Schema Conversion Tool)  
• Minimal downtime using Change Data Capture (CDC)  
• Multi-AZ deployment for high availability  
• Supports on-premises, EC2-hosted, and AWS-managed databases  
• Basic data transformation during migration  
• CloudWatch-based monitoring  

---

## Supported Sources and Targets

**Sources:**  
• On-premises databases  
• AWS-managed databases  
• EC2-hosted databases  

**Targets:**  
• Amazon RDS (all engines)  
• Amazon Aurora  
• Amazon Redshift  
• Amazon S3  
• DynamoDB  
• Kinesis Data Streams  
• OpenSearch Service  
• Any JDBC-supported database  

---

## Homogeneous vs. Heterogeneous Migrations

**Homogeneous**: Same engine (e.g., Oracle → Oracle)  
**Heterogeneous**: Different engines (e.g., Oracle → Aurora PostgreSQL)  

• Heterogeneous migrations require **AWS Schema Conversion Tool (SCT)**  
• SCT converts schema, procedures, functions, views, and reports incompatible objects  

---

## Replication Tasks

• **Full Load** – Migrates existing data  
• **CDC (Change Data Capture)** – Captures ongoing inserts/updates/deletes  
• **Full Load + CDC** – Full migration with near-zero downtime cutover  

---

## Change Data Capture (CDC)

• Near real-time, continuous replication  
• Tracks insert / update / delete operations  
• Keeps target in sync during migration and until cutover  

---

## High Availability

• Multi-AZ deployment for failover coverage  
• Replication tasks automatically resume after failover  
• Ensures minimal disruption during network or instance failures  

---

## Data Transformation

• Modify columns, data types, names  
• Filter/partition data during migration  
• Basic rule-based mapping supported  

---

## Performance and Scalability

• Scales replication instances for large migrations  
• Parallel table loading for faster throughput  
• Efficient for terabyte-scale migrations  

---

## Monitoring and Management

• CloudWatch metrics for throughput, lag, failures  
• Console UI for tasks and instance monitoring  
• Detailed task logs for debugging  
• SNS notifications for task status  

---

## Security

• Encryption in transit + at rest using KMS  
• VPC networking + security groups for isolation  
• IAM for controlling DMS operations access  
• All traffic encrypted via TLS  

---

## AWS Schema Conversion Tool (SCT)

• Required for **heterogeneous migrations**  
• Converts schema, stored procedures, triggers, functions  
• Generates assessment reports for manual fixes  
• Supports Aurora, PostgreSQL, MySQL, and others  

---

## Pricing

• Charged per replication instance-hour  
• Additional charges for migration logs + cached changes  
• No charge for data transfer between DMS and AWS databases in same region  

---

## Use Cases

• Production database migrations with minimal downtime  
• Continuous replication for DR or high availability  
• Consolidating multiple databases  
• Migrating analytics workloads to Redshift  
• Archiving transactional data to S3  

---

## Best Practices

• Use SCT early for heterogeneous migrations  
• Test migration tasks before production cutover  
• Monitor lag + task health in CloudWatch  
• Use Multi-AZ for mission-critical workloads  
• Validate post-migration data integrity  
• Plan secure networking (VPC, SGs, IAM)  

---

## Exam Tips

• Supports both homogeneous and heterogeneous migrations  
• **CDC** = minimal-downtime ongoing replication  
• **SCT** required for schema conversion in cross-engine migrations  
• Multi-AZ ensures HA and automatic failover  
• Works with on-premises, EC2, and AWS-managed databases  
• CloudWatch + SNS for monitoring and alerts  
• KMS for encryption at rest/in transit  

---

## Quick Summary
AWS Database Migration Service (DMS) automates secure, low-downtime database migrations to AWS using full-load and continuous CDC replication. It supports cross-engine migrations with SCT, integrates with CloudWatch and SNS, and provides high availability via Multi-AZ — making it the go-to tool for modern, scalable, low-risk database migrations.

