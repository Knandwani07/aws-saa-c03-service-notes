# Amazon API Gateway

---

## What It Is

Amazon API Gateway is a fully managed service that makes it easy to create, publish, maintain, monitor, and secure APIs at any scale. It supports RESTful APIs, WebSocket APIs, and HTTP APIs, enabling developers to build serverless backends and expose AWS services or custom business logic to clients.

---

## Key Features

• Supports REST, WebSocket, and HTTP APIs  
• Fully managed, scalable, and highly available  
• Request/response transformation with mapping templates  
• Integrated authorization and authentication  
• Throttling, caching, and quota management  
• Monitoring and logging with CloudWatch  
• Supports custom domain names and SSL certificates  
• Private APIs accessible via VPC Endpoints  

---

## API Types

• REST APIs: Feature-rich, customizable, supports request validation and mapping  
• HTTP APIs: Simpler, lower-cost alternative for most REST use cases  
• WebSocket APIs: Real-time two-way communication between client and server  

---

## Integration Types

• AWS Lambda: Serverless backend for APIs  
• AWS Service Integrations: Direct calls to AWS services using IAM roles  
• HTTP/HTTPS Endpoints: Proxy to external services  
• Mock Integration: Return mocked responses for testing  
• VPC Links: Access private resources in a VPC via Network Load Balancer  

---

## Authorization and Authentication

• IAM Authorization: Control API access using AWS IAM policies and roles  
• Cognito User Pools: User authentication and JWT token validation  
• Lambda Authorizers (Custom Authorizers): Run custom logic to authorize requests  
• Resource Policies: Control access based on IP addresses, VPCs, and AWS accounts  

---

## API Keys and Usage Plans

• API Keys: Identify and track API consumers  
• Usage Plans: Define throttling and quota limits for API keys  
• Enforce request limits per consumer to manage costs and resources  

---

## Throttling and Quotas

• Global and per-method request limits  
• Prevents overuse and abuse  
• Helps control costs and protect backends  

---

## Caching

• Enable response caching at the stage level  
• Reduce backend load and improve latency  
• Specify cache TTL and encryption options  

---

## Deployment and Stages

• Deploy APIs to stages (e.g., dev, test, prod)  
• Stage variables for configuration management  
• Supports canary deployments for gradual rollout  

---

## Custom Domain Names

• Map APIs to custom domains  
• Supports ACM-managed SSL/TLS certificates  
• Base path mapping for routing multiple APIs under one domain  

---

## Monitoring and Logging

• CloudWatch Metrics: Track requests, latency, errors, cache hits  
• CloudWatch Logs: Full request/response logging for debugging  
• AWS X-Ray integration for tracing API calls  

---

## Private APIs

• Accessible only within specified VPCs using Interface VPC Endpoints  
• Secures internal microservices without exposure to the public internet  

---

## Security Features

• TLS encryption for data in transit  
• IAM-based resource policies  
• API keys for managing access to consumers  
• AWS WAF integration for protection against common web exploits  
• Cognito integration for user authentication and JWT validation  
• Resource policies to restrict access to specific IP ranges or AWS accounts  

---

## Pricing

• Based on number of API calls and data transfer out  
• Separate pricing for REST APIs, HTTP APIs, and WebSocket APIs  
• Caching and custom domain name usage incur additional charges  

---

## Integration with Other AWS Services

• AWS Lambda: Create serverless backends  
• AWS Cognito: User authentication and authorization  
• AWS Step Functions: Orchestrate workflows  
• AWS DynamoDB: Direct service integrations  
• AWS S3: Serve static content or store API results  
• AWS Kinesis: Streaming data ingestion  
• AWS SNS/SQS: Messaging and queuing  

---

## Use Cases

• Build RESTful and WebSocket APIs for mobile and web applications  
• Create serverless backends with AWS Lambda  
• Securely expose AWS services to external applications  
• Enable real-time communication with WebSocket APIs  
• Build microservice architectures with managed APIs  
• Support third-party developer access with API keys and usage plans  

---

## Best Practices

• Use IAM, Cognito, or Lambda Authorizers for securing APIs  
• Enable request throttling and usage plans to prevent abuse  
• Use caching to improve performance and reduce backend load  
• Monitor usage with CloudWatch and enable logging for troubleshooting  
• Apply resource policies to restrict access to trusted networks or accounts  
• Use canary deployments to test new versions safely  
• Design APIs for idempotency and error handling  

---

## Exam Tips

• REST APIs offer advanced customization and integration features  
• HTTP APIs are simpler and cheaper, ideal for most REST use cases  
• WebSocket APIs support two-way real-time communication  
• Supports multiple integration types including Lambda, AWS services, HTTP endpoints  
• Authorization options include IAM, Cognito User Pools, and Lambda Authorizers  
• API Keys and Usage Plans enforce rate limiting and quotas  
• VPC Links allow private integrations with VPC resources  
• Supports custom domain names with ACM-managed certificates  
• Can be integrated with AWS WAF for security  
• Detailed monitoring with CloudWatch and X-Ray  

---

## Quick Summary

Amazon API Gateway is a fully managed service for building, deploying, and securing APIs at scale. It supports REST, HTTP, and WebSocket APIs with flexible integrations, authentication options, throttling, caching, monitoring, and advanced security features for both public and private APIs.

