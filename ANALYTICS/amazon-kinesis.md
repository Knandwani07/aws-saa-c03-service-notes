# Amazon Kinesis

Amazon Kinesis is a fully managed platform for real-time ingestion, processing, analysis, and delivery of streaming data.
It supports real-time applications for analytics, monitoring, IoT, and video processing at large scale.

---

## What It Is

• Fully managed service for real-time processing of streaming data at massive scale.  
• Enables you to collect, process, and analyse data streams in near real-time.  
• Supports use cases like log analytics, event data processing, IoT telemetry, and video streams.  

---

## Kinesis Data Streams (KDS)

• Real-time streaming service for continuous capture of gigabytes of data per second.  
• Producers send records to the stream.  
• Data is stored in shards.  

  - Each shard: 1 MB/s write, 2 MB/s read.  

• Records retained for 24 hours by default, up to 7 days (extended retention).  

• Consumers:  
  - AWS Lambda  
  - Kinesis Client Library (KCL)  
  - Enhanced fan-out supported (dedicated throughput per consumer)  

• Partition Key:  
  - Determines which shard the data goes to.  

• Encryption:  
  - Supports server-side encryption with AWS KMS.  

• Use Cases:  
  - Real-time dashboards  
  - Log and event collection  
  - Clickstream analysis  

---

## Kinesis Data Firehose

• Fully managed, no-shard-management service to reliably load streaming data to:  
  - S3  
  - Redshift  
  - OpenSearch (formerly Elasticsearch)  
  - Splunk  
  - Custom HTTP endpoints  

• Supports data transformation via AWS Lambda.  
• Automatic scaling.  
• Near real-time delivery (approx. 60 seconds latency).  
• Built-in compression and encryption.  
• No persistent data storage in Firehose.  

• Use Cases:  
  - Loading logs to S3 for analytics  
  - Near-real-time reporting  
  - Streaming ETL pipelines  

---

## Kinesis Data Analytics

• Fully managed service to analyse streaming data using SQL.  
• Ingests data from Kinesis Data Streams or Firehose.  
• Runs SQL queries continuously on streaming data.  
• Supports aggregation, filtering, anomaly detection.  

• Outputs to:  
  - Kinesis Data Streams  
  - Kinesis Data Firehose  
  - AWS Lambda  

• Use Cases:  
  - Real-time metrics and alerts  
  - Time-series analytics  
  - Continuous data transformation  

---

## Kinesis Video Streams

• Capture, process, and store video streams for analytics and ML.  
• Supports live and on-demand video ingestion.  
• Automatically encrypts and indexes video data.  

• Integrates with:  
  - AWS Rekognition Video  
  - Custom ML workflows  

• Provides time-indexed video storage in S3.  

• Use Cases:  
  - Security camera feeds  
  - Video-enabled IoT devices  
  - Machine learning on video data  

---

## Data Retention and Replay

• Kinesis Data Streams:  
  - Retains data for 24 hours by default, configurable up to 7 days.  
  - Supports replay (reprocessing older data).  

• Firehose:  
  - Does not store data; delivers directly to destinations.  

---

## Security

• SSE with AWS KMS for encryption at rest.  
• IAM policies for controlling access to streams, Firehose, and analytics apps.  
• VPC endpoints supported for private connectivity.  

---

## Scaling

• Kinesis Data Streams:  
  - Scale by adding/removing shards.  
  - Resharding supports split and merge operations.  
  - On-Demand mode for elastic scaling.  

• Firehose:  
  - Fully managed and auto-scales.  

• Data Analytics:  
  - Managed scaling, charged based on Kinesis Processing Units (KPU).  

---

## Pricing

• Based on:  
  - Number of shards (KDS)  
  - PUT payload units  
  - Data volume delivered (Firehose)  
  - Processing units (Analytics)  
  - Video ingestion and storage duration (Video Streams)  

---

## Kinesis Service Comparison

Service | Purpose | Data Storage | Scaling | Use Cases  
--------|---------|--------------|---------|----------  
Kinesis Data Streams | Real-time ingestion & custom processing | Stored in shards (24h–7d retention) | Manual shard scaling or On-Demand | Dashboards, logs, clickstreams  
Kinesis Data Firehose | Managed delivery to destinations | No storage (direct delivery) | Auto-scales | Load data to S3, Redshift, OpenSearch  
Kinesis Data Analytics | SQL-based analysis | Processes input only | Managed KPUs | Real-time metrics, transformations  
Kinesis Video Streams | Video ingestion & storage | Time-indexed S3 storage | Managed ingestion | Security cams, IoT video, ML  

---

## Integration

• Lambda – event source for stream processing  
• S3 – Firehose destination  
• Redshift – Direct loading via Firehose  
• OpenSearch – Indexing streaming data  
• AWS Rekognition – Video analysis  

---

## Exam Tips

• Kinesis Data Streams → real-time, ordered, sharded stream processing.  
• Firehose → simplest option; fully managed delivery to S3/Redshift/OpenSearch.  
• Data Analytics → continuous SQL queries on streaming data.  
• Video Streams → ingest and analyse video feeds.  
• Shards determine throughput in KDS.  
• Firehose supports transformation via Lambda.  
• SSE-KMS for encryption.  
• IAM policies manage access.  
• Enhanced fan-out gives dedicated throughput per consumer.  

---

## Quick Summary

Amazon Kinesis is a suite of real-time streaming services for ingestion, processing, analysis, and delivery of data.
It includes Kinesis Data Streams (sharded ingestion), Firehose (managed delivery), Data Analytics (SQL processing), and Video Streams (video ingestion and ML integration), enabling scalable real-time data applications.

