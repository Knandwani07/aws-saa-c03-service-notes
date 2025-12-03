# Amazon EMR

Amazon EMR (Elastic MapReduce) is a fully managed big data platform that simplifies running large-scale distributed data processing jobs using open-source frameworks such as Apache Hadoop, Spark, Hive, HBase, Presto, and others.
It allows fast and cost-effective processing of vast amounts of data.

---

## What It Is

Amazon EMR is a managed cluster platform for big data processing using popular open-source tools.
It supports scalable, cost-efficient workloads that integrate with S3 and other AWS services.

---

## Key Features

• Fully managed clusters for Hadoop, Spark, Hive, HBase, Presto, and more  
• Quick and easy provisioning of resizable clusters  
• Integration with Amazon S3 for data storage  
• Decoupled storage and compute using EMRFS  
• Cluster scaling with Auto Scaling and manual resizing  
• EMR Managed Scaling automatically adjusts resources  
• Cost-effective with per-second billing and Spot Instances  
• Supports AWS Glue Data Catalog for schema management  
• Integration with AWS Lake Formation for data permissions  
• Integration with AWS Step Functions for orchestration  
• Notebook support via EMR Notebooks for interactive analysis  

---

## Core Components

• Cluster – A collection of Amazon EC2 instances running EMR  
• Master Node – Manages cluster and tracks job progress  
• Core Nodes – Process data and store intermediate results  
• Task Nodes – Process data only, with no HDFS storage  
• EMRFS – Connects EMR to S3 for scalable, durable storage  

---

## Deployment and Management

• Launch clusters via Console, CLI, SDKs, or CloudFormation  
• Choose EC2 instance types and purchase options (On-Demand, Spot)  
• EMR Managed Scaling automatically adjusts cluster size  
• Cluster Auto Termination helps reduce costs  
• Bootstrap actions install software and customize nodes  
• Supports multi-master mode for high availability in Hadoop YARN  

---

## Data Storage

• EMRFS for S3 integration with consistency improvements  
• HDFS for ephemeral storage on cluster nodes  
• Supports Glue Data Catalog for Hive Metastore compatibility  
• Lake Formation integration for centralized data access control  

---

## Processing Frameworks

• Hadoop MapReduce for batch processing  
• Apache Spark for fast, in-memory analytics  
• Hive for SQL-like queries  
• Presto for low-latency SQL queries  
• HBase for NoSQL workloads  
• Flink for real-time stream processing  
• Zeppelin and Jupyter Notebooks for interactive analytics  

---

## Security

• IAM roles for fine-grained access control  
• AWS KMS for encryption at rest  
• TLS for encryption in transit  
• Kerberos authentication for Hadoop clusters  
• Security groups for network control  
• Lake Formation integration for data permissions  
• EC2 key pairs for SSH access  
• CloudTrail for auditing API calls  

---

## Monitoring and Logging

• Amazon CloudWatch for cluster metrics and alarms  
• CloudWatch Logs for application logs  
• EMR console for real-time monitoring  
• Ganglia and Spark UI for performance insights  
• S3 for storing logs  

---

## Scaling and Flexibility

• Manual resizing or Auto Scaling for cluster elasticity  
• EMR Managed Scaling automatically resizes clusters  
• Spot Instances supported for cost savings  
• Instance Fleets and Instance Groups for provisioning strategies  
• Decoupled compute and storage with S3  

---

## Cost Optimization

• Per-second billing for EC2 instances  
• Support for Spot Instances  
• Cluster Auto Termination to prevent idle costs  
• Reserved Instances for predictable workloads  
• EMR charges based on instance hours plus EC2 costs  

---

## Integrations

• Amazon S3 for data lake storage  
• AWS Glue for schema management  
• AWS Lake Formation for permissions  
• AWS Step Functions for orchestration  
• AWS CloudTrail for auditing  
• Amazon RDS and Redshift as data sources  
• Kinesis Data Streams and Firehose for streaming ingestion  

---

## Use Cases

• Big data processing and ETL workloads  
• Data lake analytics using S3  
• Machine learning workflows with Spark MLlib  
• Log and clickstream analysis  
• Real-time stream processing with Flink  
• Ad hoc analytics with notebooks  
• Batch processing of large datasets  

---

## Pricing

• Charges based on EC2 instance hours  
• Additional EMR per-instance-hour fee  
• Per-second billing for EC2  
• S3 storage and data transfer charges  
• Additional costs for Glue, Lake Formation, and integrated services  

---

## Best Practices

• Use Spot Instances for core and task nodes to reduce cost  
• Enable EMR Managed Scaling for automatic optimization  
• Store data in S3 using EMRFS for decoupled architecture  
• Use AWS Glue Data Catalog for schema management  
• Secure clusters using IAM roles, KMS encryption, and Kerberos  
• Monitor using CloudWatch and CloudTrail  
• Automate workflows with Step Functions and CloudFormation  

---

## Exam Tips

• Fully managed big data platform supporting Hadoop, Spark, Hive, Presto, HBase  
• EMRFS enables direct read/write to S3  
• Managed Scaling automatically resizes clusters  
• Spot Instances reduce costs significantly  
• Supports TLS and KMS encryption  
• IAM roles manage resource access  
• Glue Catalog support for Hive compatibility  
• Decoupled compute and storage  
• Use cases: log processing, ETL, ML, data lake analytics  

---

## Quick Summary

Amazon EMR is AWS’s managed big data platform for running open-source frameworks on scalable EC2 clusters.
It integrates tightly with S3, offers strong security, flexible scaling, and cost optimization,
making it ideal for processing massive datasets for analytics, ETL, and machine learning.

