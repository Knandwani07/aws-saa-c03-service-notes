# 📘 AWS SAA-C03 – Consolidated Service Cheatsheet
This cheatsheet provides a concise, category-based summary of major AWS services 
relevant to the AWS SAA-C03 exam.  
Each entry focuses on the primary function of the service (“What It Does”), allowing 
rapid review while preparing for the certification.

# ANALYTICS

Service | What It Does
--------|--------------
Amazon Athena | Serverless interactive query service; run SQL directly on S3 data. Pay per query; ideal for ad-hoc analysis.
AWS Data Exchange | Subscribe to and use third-party datasets directly in AWS workflows.
AWS Data Pipeline | Managed ETL and workflow orchestration across AWS and on-prem environments.
Amazon EMR | Managed Hadoop/Spark clusters for large-scale data processing; cost-efficient and customizable.
AWS Glue | Serverless ETL with data cataloging, crawlers, and Spark jobs for data preparation.
Amazon Kinesis | Real-time streaming ingestion/processing of logs, IoT data, clickstreams.
AWS Lake Formation | Build, govern, and secure S3-based data lakes with centralized permissions.
Amazon MSK | Fully managed Apache Kafka clusters; AWS manages scaling and patching.
Amazon OpenSearch Service | Managed search & analytics engine; log analysis, dashboards; ELK compatible.
Amazon QuickSight | Serverless BI dashboards with in-memory SPICE engine.
Amazon Redshift | Fully managed data warehouse with MPP architecture and columnar storage.

# APPLICATION INTEGRATION

Service | What It Does
--------|--------------
Amazon AppFlow | No-code data movement between SaaS apps (Salesforce, Slack) and AWS.
AWS AppSync | Managed GraphQL API service with real-time sync and offline support.
Amazon EventBridge | Serverless event bus integrating AWS services, SaaS apps, and custom events.
Amazon MQ | Managed ActiveMQ/RabbitMQ for traditional applications needing message brokers.
Amazon SNS | Pub/Sub messaging with fan-out to SQS, Lambda, email, mobile push.
Amazon SQS | Fully managed message queues; Standard & FIFO for ordered/exactly-once delivery.
AWS Step Functions | Serverless workflow orchestration with visual state machines.

# AWS COST MANAGEMENT

Service | What It Does
--------|--------------
AWS Budgets | Create budgets and receive alerts for cost and usage thresholds.
AWS CUR (Cost and Usage Report) | Most detailed AWS billing dataset; exported to S3 for deep analysis.
AWS Cost Explorer | Analyze cost trends, identify usage patterns, and view recommendations.
Savings Plans | Commit to usage ($/hr) for 1–3 years to receive significant compute discounts.

# COMPUTE

Service | What It Does
--------|--------------
AWS Batch | Runs batch workloads at any scale; provisions compute automatically.
Amazon EC2 | Resizable virtual servers with full OS/network control.
EC2 Auto Scaling | Automatically adjusts EC2 capacity based on demand.
AWS Elastic Beanstalk | Platform-as-a-Service; deploy apps without managing infrastructure.
AWS Outposts | Run AWS hardware/services in on-prem data centers for low-latency or residency needs.
AWS Serverless Application Repository | Prebuilt serverless apps published by AWS and the community.
VMware Cloud on AWS | Run VMware (vSphere/NSX/vSAN) on AWS bare metal.
AWS Wavelength | Ultra-low-latency compute at 5G edge locations for AR/VR, IoT, autonomous workloads.

# CONTAINERS

Service | What It Does
--------|--------------
Amazon ECS Anywhere | Run ECS tasks on premises or edge with centralized control.
Amazon EKS Anywhere | On-prem Kubernetes clusters using EKS management tooling.
Amazon EKS Distro | Open-source Kubernetes distribution used by EKS.
Amazon ECR | Managed container registry with scanning and secure image storage.
Amazon ECS | AWS-managed container orchestration, tightly integrated with AWS services.
Amazon EKS | Managed Kubernetes service with automated control-plane operations.

# DATABASES

Service | What It Does
--------|--------------
Amazon Aurora | High-performance, MySQL/PostgreSQL-compatible relational DB with distributed storage.
Aurora Serverless | On-demand autoscaling Aurora with pay-per-use pricing.
Amazon DocumentDB | Managed MongoDB-compatible document database.
Amazon DynamoDB | Fully managed NoSQL key-value/document DB; single-digit ms latency.
Amazon ElastiCache | Managed Redis/Memcached for in-memory caching; sub-ms performance.
Amazon Keyspaces | Managed Cassandra-compatible NoSQL DB; serverless and scalable.
Amazon Neptune | Fully managed graph database (Property Graph + RDF).
Amazon QLDB | Immutable ledger database with cryptographically verifiable logs.
Amazon RDS | Managed relational databases (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB).
Amazon Redshift | Managed data warehouse with columnar storage and high-speed MPP queries.

# DEVELOPER TOOLS

Service | What It Does
--------|--------------
AWS X-Ray | End-to-end tracing for distributed applications; identifies latency, bottlenecks, and failures.

# FRONT-END & MOBILE

Service | What It Does
--------|--------------
AWS Amplify | Full-stack web/mobile development; handles auth, APIs, storage, hosting.
Amazon API Gateway | Managed REST/HTTP/WebSocket API service with throttling, auth, caching.
AWS Device Farm | Test web/mobile apps on real devices in AWS.
Amazon Pinpoint | Targeted engagement via SMS, email, push, with analytics and segmentation.

# MACHINE LEARNING

Service | What It Does
--------|--------------
Amazon Comprehend | NLP service for sentiment, entities, key phrases, language detection.
Amazon Forecast | Managed time-series forecasting using ML.
Amazon Fraud Detector | Detects fraudulent activity using ML-based models.
Amazon Kendra | Intelligent enterprise search with natural-language querying.
Amazon Lex | Conversational interface service; same tech behind Alexa.
Amazon Polly | Text-to-speech with natural-sounding voices.
Amazon Rekognition | Image/video analysis: labels, faces, moderation, OCR.
Amazon SageMaker | End-to-end ML development platform.
Amazon Textract | Extracts text/tables/forms from documents using ML OCR.
Amazon Transcribe | Converts audio streams into text.
Amazon Translate | Neural machine translation.

# MANAGEMENT & GOVERNANCE

Service | What It Does
--------|--------------
AWS Auto Scaling | Unified scaling across EC2, ECS, DynamoDB, Aurora.
AWS CloudFormation | Infrastructure-as-code using templates.
AWS CloudTrail | Logs API calls and account activity.
Amazon CloudWatch | Metrics, logs, alarms, dashboards.
AWS CLI | Command-line management interface for AWS services.
AWS Compute Optimizer | Recommends optimal instance types for cost & performance.
AWS Config | Tracks configuration changes and compliance; drift detection.
AWS Control Tower | Automated multi-account setup with guardrails and blueprints.
AWS Health Dashboard | Service health and personalized impact notifications.
AWS License Manager | Track and manage software licenses.
Amazon Managed Grafana | Fully managed Grafana dashboards.
Amazon Managed Service for Prometheus | Scalable Prometheus metrics ingestion.
AWS Management Console | Web-based UI for AWS services.
AWS Organizations | Multi-account governance, SCPs, consolidated billing.
AWS Proton | Automated deployment templates for microservices/serverless.
AWS Service Catalog | Managed portfolios of approved IT services.
AWS Systems Manager | Patch Manager, Parameter Store, Session Manager, Automation, OpsCenter.
AWS Trusted Advisor | Real-time optimization checks.
AWS Well-Architected Tool | Reviews workloads against AWS best-practice pillars.

# MEDIA SERVICES

Service | What It Does
--------|--------------
Amazon Elastic Transcoder | Legacy transcoding service for converting media formats.
Amazon Kinesis Video Streams | Capture, store, and process live video; integrates with ML tools.

# MIGRATION & TRANSFER

Service | What It Does
--------|--------------
AWS Application Discovery Service | Collects server inventory, dependencies, performance data for migration planning.
AWS Application Migration Service (MGN) | Lift-and-shift server migration with continuous replication.
AWS Database Migration Service (DMS) | Migrates databases with minimal downtime.
AWS DataSync | High-speed transfer between on-prem storage and AWS.
AWS Migration Hub | Central migration tracking dashboard.
AWS Snow Family | Snowcone/Snowball/Snowmobile for large offline transfers.
AWS Transfer Family | Managed SFTP/FTPS/FTP into S3 or EFS.

# NETWORKING & CONTENT DELIVERY

Service | What It Does
--------|--------------
AWS Client VPN | Fully managed client VPN for remote access.
Amazon CloudFront | Global CDN with caching, DDoS protection, edge compute.
AWS Direct Connect | Private dedicated link between on-prem and AWS.
Elastic Load Balancing | Distributes traffic across resources (ALB/NLB/CLB).
AWS Global Accelerator | Improves global performance via AWS backbone.
AWS PrivateLink | Private connectivity to services without using public internet.
Amazon Route 53 | Managed DNS with routing policies and health checks.
AWS Site-to-Site VPN | IPSec VPN between on-prem and AWS.
AWS Transit Gateway | Central hub for VPC and on-prem connectivity.
Amazon VPC | Private cloud network: subnets, route tables, SGs, NACLs, IGW, NAT.

# SECURITY, IDENTITY & COMPLIANCE

Service | What It Does
--------|--------------
AWS Artifact | On-demand access to compliance reports (SOC, PCI, ISO).
AWS Audit Manager | Collects evidence for compliance audits.
AWS Certificate Manager | Issues and manages SSL/TLS certificates.
AWS CloudHSM | Dedicated hardware security modules.
Amazon Cognito | User authentication, identity federation.
Amazon Detective | Investigates security findings using relationship graphs.
AWS Directory Service | Managed Active Directory integrations.
AWS Firewall Manager | Centralized management for WAF/Shield/Network Firewall.
Amazon GuardDuty | ML-based continuous threat detection.
AWS IAM Identity Center | Centralized SSO across AWS accounts and apps.
AWS IAM | Core access management with policies, roles, permissions.
Amazon Inspector | Automated vulnerability scanning.
AWS KMS | Key creation, storage, rotation, and encryption.
Amazon Macie | ML-based PII detection in S3.
AWS Network Firewall | Managed network-level firewall.
AWS RAM | Share resources across AWS accounts.
AWS Secrets Manager | Secure secret storage with automatic rotation.
AWS Security Hub | Aggregate and prioritize findings.
AWS Shield | DDoS protection service.
AWS WAF | Protects against common web exploits.

# SERVERLESS

Service | What It Does
--------|--------------
AWS AppSync | Managed GraphQL API service.
AWS Fargate | Serverless compute engine for containers.
AWS Lambda | Event-driven compute with automatic scaling.

# STORAGE

Service | What It Does
--------|--------------
AWS Backup | Centralized automated backups for AWS resources.
Amazon EBS | Block storage for EC2 with snapshots.
Amazon EFS | Fully managed NFS file system; elastic scaling.
Amazon FSx | High-performance file systems (Lustre, ONTAP, OpenZFS, Windows).
Amazon S3 | Scalable object storage with high durability.
Amazon S3 Glacier | Low-cost archival storage.
AWS Storage Gateway | Hybrid on-prem to AWS storage integration.

