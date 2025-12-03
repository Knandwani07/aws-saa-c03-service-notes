# Amazon Managed Grafana

---

## What It Is

Amazon Managed Grafana is a fully managed service that provides scalable, secure, and highly available Grafana workspaces without needing to operate Grafana infrastructure. It enables teams to visualize, analyse, and share operational data across AWS services and third-party data sources using rich dashboards and alerting.

---

## Key Features

• Fully managed, highly available Grafana workspaces  
• Native integration with AWS data sources (CloudWatch, X-Ray, Timestream, IoT SiteWise)  
• Supports 40+ data sources including Prometheus, Elasticsearch, InfluxDB, MySQL  
• Built-in security with AWS SSO and IAM Identity Center  
• Supports Grafana Enterprise plugins  
• Automatic version upgrades and patching  
• Dashboard creation, sharing, and embedding support  
• Advanced alerting with SNS, Slack, and more  

---

## Workspaces

• Logical, isolated Grafana environments within your AWS account  
• Multi-user access with AWS SSO  
• Workspaces are secure and independent  
• Create multiple workspaces for teams, projects, or environments  

---

## Data Sources

• Native AWS integrations:  
o Amazon CloudWatch  
o AWS X-Ray  
o AWS IoT SiteWise  
o Amazon Timestream  
o AWS Managed Prometheus  

• Third-party integrations:  
o Prometheus  
o Elasticsearch  
o InfluxDB  
o MySQL/PostgreSQL  
o OpenSearch Service  

---

## Security and Access Control

• Authentication/authorization via AWS SSO  
• Fine-grained IAM policy control  
• Encryption at rest with AWS KMS  
• VPC connectivity for private sources  
• CloudTrail audit logging for governance  

---

## Alerting

• Define metric thresholds and alerting conditions  
• Integrations with SNS, Slack, email, and other channels  
• Managed alerting with deduplication and silencing  
• Centralized rule and notification policy management  

---

## Grafana Enterprise Features

• Optional access to enterprise plugins (additional cost)  
• Examples: ServiceNow, Splunk, Datadog, Dynatrace  
• Enhanced reporting and integration capabilities  

---

## Integration with AWS Services

• CloudWatch – Metrics dashboards for AWS infrastructure  
• X-Ray – Application trace visualization  
• IoT SiteWise – Industrial data analytics  
• Timestream – Time-series data dashboards  
• Managed Prometheus – Prometheus metrics visualization  

---

## Deployment and Management

• Fully managed provisioning, scaling, patching, and availability  
• Deploy via Console, CLI, or CloudFormation  
• Automatic upgrades to latest Grafana versions  
• Supports IaC for workspace lifecycle management  

---

## Pricing

• Billed per active user per workspace per month  
• Free tier available for trials  
• Extra charges for enterprise plugins  
• Data transfer charges when querying external sources  

---

## Use Cases

• Monitoring AWS infrastructure with CloudWatch  
• Microservices observability using Prometheus and X-Ray  
• Industrial IoT visualization with SiteWise  
• DevOps/SRE operational dashboards  
• Unified metrics, logs, and traces correlation  

---

## Best Practices

• Use AWS SSO to manage user authentication  
• Restrict workspace access using IAM policies  
• Enable audit logging for compliance  
• Segment workspaces by team/project  
• Integrate SNS for alerting into AWS workflows  

---

## Exam Tips

• Fully managed Grafana service, no server maintenance  
• Integrates with AWS native + third-party data sources  
• Secure access via AWS SSO and IAM  
• Ideal for dashboards monitoring AWS services and application traces  
• AWS handles versioning, updates, and scaling  
• Alerts can be sent via SNS, Slack, email, etc.  

---

## Quick Summary

Amazon Managed Grafana delivers scalable, secure, fully managed Grafana workspaces integrated deeply with AWS and third-party data sources. It enables dashboard creation, real-time observability, enterprise plugin support, and advanced alerting without the operational overhead of self-hosting Grafana.

