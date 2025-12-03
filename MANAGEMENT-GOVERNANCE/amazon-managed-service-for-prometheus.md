# Amazon Managed Service for Prometheus (AMP)

---

## What It Is

Amazon Managed Service for Prometheus (AMP) is a fully managed, highly available, and scalable monitoring service compatible with open-source Prometheus. It lets you collect, store, and query metrics at scale without managing or operating Prometheus infrastructure.

---

## Key Features

• Fully managed, serverless, and auto-scaling  
• Prometheus-compatible with full PromQL support  
• High availability across multiple AZs  
• Integrated with AWS security services (IAM, PrivateLink)  
• Encryption in transit and at rest using AWS KMS  
• Supports EKS, ECS, EC2, and other AWS metric sources  
• Pay-as-you-go with no upfront cost  

---

## Prometheus Compatibility

• Works with open-source Prometheus clients, exporters, and tools  
• Supports remote write to ingest metrics from existing Prometheus servers  
• PromQL querying for metric analysis  
• Compatible with standard Prometheus instrumentation libraries  

---

## Data Ingestion and Storage

• Remote write API for pushing metrics  
• Automatically scales ingestion throughput  
• Durable, long-term metric storage  
• Replicates data across multiple AZs  
• Retention policies for cost and compliance management  

---

## Querying and Analysis

• Full PromQL query support  
• Native integration with Amazon Managed Grafana for dashboards  
• Build alerts and visualizations using Prometheus metrics  
• Low-latency querying at any scale  

---

## Security and Access Control

• IAM policies for workspace-level access control  
• AWS PrivateLink for private, secure connectivity  
• KMS encryption for data in transit and at rest  
• CloudTrail logging for auditing API calls  
• Resource tagging for cost tracking  

---

## Integration with AWS Services

• Amazon EKS – native Kubernetes metric collection  
• AWS Distro for OpenTelemetry – metrics ingestion from many sources  
• Amazon Managed Grafana – dashboarding and visualization  
• AWS CloudWatch – complementary logs/metrics support  
• IAM – identity and access management for AMP resources  

---

## Pricing

• Based on ingestion volume, stored GB-months, and query requests  
• No upfront fees or commitments  
• Pay only for actual usage, ideal for variable workloads  

---

## Use Cases

• Monitoring Kubernetes clusters on Amazon EKS  
• Collecting metrics from Prometheus exporters  
• Building PromQL-based alerts and Grafana dashboards  
• Centralized observability for hybrid AWS + on-prem environments  
• Supporting DevOps/SRE teams with autoscaling metric storage  

---

## Best Practices

• Use IAM for fine-grained workspace access control  
• Use PrivateLink for private, secure ingestion and querying  
• Tag workspaces for cost governance  
• Integrate with Managed Grafana for visualization and alerting  
• Configure retention policies based on compliance + cost goals  

---

## Exam Tips

• AMP is fully managed and Prometheus-compatible  
• Uses PromQL for querying metrics  
• Supports remote write from existing Prometheus setups  
• Integrates with IAM and PrivateLink for secure access  
• Works closely with Managed Grafana for dashboards  
• Replicates data across multiple AZs for high availability  
• Pay-as-you-go model, no provisioning required  

---

## Quick Summary

Amazon Managed Service for Prometheus provides scalable, secure, Prometheus-compatible monitoring without the complexity of running Prometheus infrastructure. It integrates natively with AWS compute, networking, and observability services, offering reliable metric ingestion, long-term storage, and efficient querying at cloud scale.

