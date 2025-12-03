# AWS X-Ray

---

## What It Is

AWS X-Ray is a distributed tracing service that helps developers analyse and debug production, distributed applications. It provides insights into application behaviour and performance by collecting data about requests as they travel through an application.

---

## Key Features

• End-to-end request tracing across microservices and components  
• Visual service map to see how components interact  
• Trace data includes latency, errors, and exceptions  
• Helps identify bottlenecks and performance issues  
• Supports sampling to control tracing costs  
• Works with AWS services like EC2, ECS, Lambda, API Gateway, and more  

---

## Core Concepts

• Segments: Data collected for individual services handling a request  
• Subsegments: Fine-grained data within a segment, such as downstream calls or annotations  
• Traces: Complete end-to-end path of a single request through the system  
• Sampling: Controls which requests are traced to balance cost and insight  
• Annotations: Indexed key-value pairs for searching and filtering traces  
• Metadata: Non-indexed data attached to segments for deeper analysis  

---

## How It Works

• X-Ray SDKs instrument applications to record trace data  
• Trace data is sent to the X-Ray service  
• Service map visualizes connections and latencies between components  
• Developers analyse traces to identify errors, slow components, and service dependencies  
• Sampling rules define which requests are traced to manage cost  

---

## Integrations

• AWS Lambda: Automatic integration with tracing enabled  
• API Gateway: Can pass trace headers to downstream services  
• Elastic Load Balancer: Passes trace headers to targets  
• ECS and EC2: SDK-based integration for applications  
• AWS App Runner: Supports X-Ray integration  
• AWS Step Functions: Can propagate trace context between steps  

---

## Sampling

• Reduces overhead by only tracing a subset of requests  
• Default rate of 1 request per second with 5% of additional requests  
• Configurable sampling rules per service or endpoint  
• Ensures consistent visibility without excessive cost  

---

## Security and Permissions

• IAM policies control access to X-Ray APIs and data  
• Data is encrypted in transit using TLS  
• Data is encrypted at rest in the X-Ray service  

---

## Storage and Retention

• Trace data retained by AWS X-Ray for 30 days  
• No need to manage storage infrastructure  
• Pay only for traces recorded and analysed  

---

## Analysis and Troubleshooting

• Service Map: Visual representation of request flow between services  
• Trace Timeline: Breaks down request duration by segment and subsegment  
• Error and Fault Analysis: Highlights errors, exceptions, and timeouts  
• Filter Expressions: Search traces by annotation, service, or error type  
• Insights: Automated root cause analysis of anomalies  

---

## Pricing

• Free tier: 100,000 traces recorded and 1,000,000 traces retrieved or scanned per month for the first three months  
• Pricing based on traces recorded and retrieved beyond free tier  
• No cost for integrating X-Ray SDK or agent  

---

## Use Cases

• Debugging production issues in microservices architectures  
• Analysing and improving application performance  
• Identifying latency bottlenecks across services  
• Tracing user requests end-to-end across distributed systems  
• Compliance and audit of service interactions  

---

## Best Practices

• Enable sampling to control costs without losing visibility  
• Add meaningful annotations for better filtering and searching  
• Monitor service maps regularly to detect unexpected dependencies  
• Use X-Ray Insights for proactive detection of anomalies  
• Integrate with CI/CD pipelines for continuous observability  

---

## Exam Tips

• X-Ray is used for distributed tracing and debugging  
• Visualizes service maps and trace timelines  
• Supports sampling to manage cost and performance impact  
• Integrated with many AWS services, including Lambda and API Gateway  
• Helps identify errors, bottlenecks, and dependencies in microservices  
• IAM policies control access to X-Ray data and APIs  

---

## Quick Summary

AWS X-Ray is a managed service for distributed tracing, helping developers analyse, visualize, and debug applications in production. It enables end-to-end request tracing, identifies performance bottlenecks, and improves observability for microservices and serverless architectures.

