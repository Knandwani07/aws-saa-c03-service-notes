# Amazon CloudWatch

---

## What It Is

Amazon CloudWatch is a monitoring and observability service for AWS resources and applications. It provides data collection, visualization, alerting, and automated responses to changes in your environment.

---

## Key Features

• Collects and tracks metrics for AWS resources and custom metrics  
• Logs aggregation, storage, search, and analysis  
• Alarms for monitoring thresholds and triggering actions  
• Dashboards for visualization of metrics and logs  
• Events for responding to state changes in AWS resources  
• Anomaly detection for identifying unusual metric patterns  
• Contributor Insights for analysing high-cardinality log data  
• CloudWatch Synthetics for monitoring application endpoints  
• ServiceLens for visualizing application performance and dependencies  

---

## Metrics

• Automatically collects metrics from AWS services like EC2, RDS, Lambda, and ELB  
• Custom metrics can be published by applications  
• Standard and detailed monitoring (e.g., 1-minute vs 5-minute intervals)  
• Supports percentile-based metrics and high-resolution (up to 1-second) metrics  
• Metric math for creating derived metrics from existing ones  

---

## Logs

• Centralized storage and analysis of logs from AWS services and applications  
• CloudWatch Logs Agents and AWS Lambda can send logs  
• Supports log filtering and metric extraction  
• Log groups and log streams for organization  
• Subscription filters for streaming logs to other services (e.g., Lambda, Kinesis)  
• Log Insights for querying and analysing logs with a SQL-like syntax  

---

## Alarms

• Watches metrics and triggers actions when thresholds are breached  
• Supports static thresholds and anomaly detection  
• Actions include SNS notifications, Auto Scaling policies, and EC2 actions (stop, terminate, reboot, recover)  
• Composite alarms to combine multiple alarms with AND/OR logic  

---

## Dashboards

• Customizable views of metrics and logs in a single interface  
• Supports text, metric graphs, and log queries  
• Can include data from multiple regions and accounts  
• JSON-based dashboard definitions for automation  

---

## Events (EventBridge Integration)

• CloudWatch Events is now Amazon EventBridge  
• Delivers system events describing changes in AWS resources  
• Allows setting up rules to match events and trigger targets like Lambda, SNS, or Step Functions  
• Supports scheduled (cron) events for automated tasks  

---

## CloudWatch Synthetics

• Allows creation of canaries to monitor application endpoints and APIs  
• Simulates user interactions to check availability and latency  
• Captures screenshots, logs, and metrics for detailed analysis  

---

## CloudWatch Contributor Insights

• Analyses time-series log data to identify top contributors  
• Helps troubleshoot high-cardinality issues such as top talkers or top error sources  
• Supports real-time and historical analysis  

---

## CloudWatch ServiceLens

• Integrates metrics, logs, and traces for end-to-end observability  
• Visualizes service maps and dependencies  
• Integrates with AWS X-Ray for distributed tracing  
• Helps identify bottlenecks and performance issues across microservices  

---

## Retention and Storage

• Metrics retained for 15 months (granularity decreases with age)  
• Logs retention configurable from days to indefinite  
• Log archives can be exported to S3  

---

## Security

• IAM policies to control access to CloudWatch resources  
• Data encrypted at rest and in transit  
• Supports KMS for log group encryption  
• AWS CloudTrail integration for auditing API calls  

---

## Integration with AWS Services

• Works with EC2, Lambda, RDS, DynamoDB, ELB, ECS, EKS, and many other AWS services  
• Supports custom applications publishing metrics via the PutMetricData API  
• Integrates with AWS Auto Scaling for dynamic resource management  
• Supports cross-account dashboards and metrics  

---

## Pricing

• Charged based on metrics, API requests, alarms, dashboards, logs ingested and stored, and canary runs  
• Free tier includes basic monitoring metrics and 5GB of log ingestion per month  

---

## Best Practices

• Use detailed monitoring for production-critical resources  
• Set up alarms for key metrics and use SNS for notifications  
• Use log filters to extract custom metrics from logs  
• Leverage Contributor Insights for analysing high-volume log data  
• Combine metrics, logs, and traces in dashboards for full observability  
• Use anomaly detection for dynamic workloads  
• Archive old logs to Amazon S3 for cost optimization  

---

## Exam Tips

• CloudWatch Metrics: monitor AWS resources and custom data  
• CloudWatch Logs: store, search, and analyse application and system logs  
• Alarms: trigger actions based on metric thresholds  
• Dashboards: visualize operational data in one place  
• Events/EventBridge: respond to state changes or schedule tasks  
• Synthetics: monitor API and web endpoint availability  
• Contributor Insights: analyse top contributors in log data  
• ServiceLens: correlate metrics, logs, and traces  
• Integrates with Auto Scaling, SNS, Lambda, and many other AWS services  

---

## Quick Summary

Amazon CloudWatch is AWS’s integrated monitoring and observability service. It provides metrics, logs, alarms, dashboards, events, and advanced features like anomaly detection, Contributor Insights, and ServiceLens to help you understand and manage the performance, health, and availability of your AWS environment and applications.

