# Amazon Athena

Amazon Athena is a serverless interactive query service that makes it easy to analyse data stored in Amazon S3 using standard SQL.
It requires no infrastructure management, and you pay only for the queries you run.

---

## What It Is

Amazon Athena is an interactive query service that allows you to analyse data in Amazon S3 using SQL.  
It is fully serverless, meaning there are no servers to configure, scale, or maintain.

---

## Key Features

• Serverless, no need to provision or manage infrastructure  
• SQL-based queries using standard ANSI SQL  
• Supports querying data in S3 directly  
• Pay-per-query pricing model (charged per TB of data scanned)  
• Integrated with AWS Glue Data Catalog for schema management  
• Supports complex joins, window functions, and arrays  
• Query results can be stored in Amazon S3  

---

## How It Works

• Point Athena at data stored in Amazon S3  
• Define table schema using AWS Glue Data Catalog or Athena DDL  
• Run SQL queries directly on data in S3  
• Query results are saved to S3  
• Supports data partitioning for improved performance and cost savings  

---

## Supported Data Formats

• CSV, TSV, JSON  
• ORC, Parquet, Avro  
• Text files with custom delimiters  
• Apache Web Logs  

---

## Performance Optimization

• **Partitioning** – Splits data into smaller sets for faster queries  
• **Columnar formats** – ORC and Parquet reduce data scanned  
• **Compression** – Reduces data transfer and storage costs  
• **Bucketing** – Organizes data for efficient joins  

---

## AWS Glue Integration

• Stores metadata in the AWS Glue Data Catalog  
• Glue Crawlers can infer schema automatically  
• Shared Data Catalog with Amazon Redshift Spectrum and Amazon EMR  
• Supports schema versioning  

---

## Security

• Encryption at rest using SSE-S3 or SSE-KMS  
• Encryption in transit using HTTPS  
• IAM policies control access to queries and underlying data  
• Integration with AWS Lake Formation for fine-grained access control  
• Query result encryption in S3  

---

## Monitoring and Logging

• CloudWatch integration for query metrics  
• CloudTrail logging for API audit events  
• Query history visible in Athena console  
• Ability to track slow or failed queries  

---

## Use Cases

• Ad hoc querying of log files in S3  
• Analysing AWS service logs (CloudTrail, ELB, VPC Flow Logs)  
• Data lake analytics without requiring ETL  
• Interactive data exploration and reporting  
• BI dashboards using Amazon QuickSight  
• Cost-efficient warehousing for infrequent queries  

---

## Pricing

• Charged per TB of data scanned  
• Columnar, compressed, and partitioned data lowers cost  
• No cost for infrastructure or idle time  
• AWS Glue Data Catalog pricing applies separately  

---

## Integration with Other AWS Services

• **Amazon S3** – Data source + query result storage  
• **AWS Glue** – Schema and metadata management  
• **Amazon QuickSight** – Dashboards and visualizations  
• **AWS Lake Formation** – Governance and access control  
• **CloudTrail & CloudWatch** – Logging and monitoring  

---

## Best Practices

• Partition data to minimize scan size  
• Use columnar formats (Parquet or ORC)  
• Compress data to reduce storage and cost  
• Maintain schemas in AWS Glue  
• Apply IAM and encryption controls for security  

---

## Exam Tips

• Serverless SQL queries on S3  
• Pay-per-TB scanned → optimize with partitions/columnar formats  
• Integrated with AWS Glue Data Catalog  
• Supports multiple formats including Parquet and ORC  
• Works with QuickSight for visualization  
• Best suited for ad hoc queries on large S3 datasets  
• Use IAM + Lake Formation for access control  
• Encrypt data at rest and in transit  

---

## Quick Summary

Amazon Athena is a fully serverless service that queries S3 data using standard SQL without requiring infrastructure.
It is cost-efficient, integrates with AWS Glue, supports multiple formats, and is ideal for ad hoc analytics and data lake use cases.
