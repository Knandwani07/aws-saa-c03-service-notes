# Amazon SNS

Amazon Simple Notification Service (SNS) is a fully managed pub/sub messaging service that decouples application components through asynchronous message delivery and enables fan-out messaging to multiple subscribers.

---

## What It Is

• Fully managed pub/sub messaging service  
• Decouples application components  
• Enables message fan-out to multiple subscribers  

---

## Core Concepts

### 1. Topics
• Logical access point for publishing messages  
• Publishers send messages to a topic  
• Subscribers receive messages from a topic  

### 2. Subscriptions
• Determine where messages are delivered  
• Supported protocols:
  - Amazon SQS  
  - AWS Lambda  
  - HTTP/HTTPS  
  - Email / Email-JSON  
  - SMS  
  - Mobile push (Application)  
  - AWS Kinesis Data Firehose  

### 3. Publishers and Subscribers
• Publisher (Producer): sends messages to the SNS topic  
• Subscriber (Consumer): receives messages using supported protocols  

---

## Message Delivery

• Push-based delivery to multiple endpoints  
• Message filtering by attributes  
• Automatic retries on delivery failure  
• Dead-letter queues (DLQs) supported  

---

## Use Cases

• Application decoupling via pub/sub  
• Fan-out messaging to multiple consumers  
• Event-driven architecture  
• Mobile push notifications  
• Real-time alerts and monitoring  

---

## SNS vs SQS

| Feature | SNS | SQS |
|--------|-----|-----|
| Model | Pub/Sub (Push) | Queue (Pull) |
| Delivery | Push to multiple subscribers | Pull by one consumer |
| Use Case | Fan-out to services | Decoupling with buffering |
| Target Options | Lambda, SQS, SMS, Email, HTTP/S | Lambda or polling |

---

## Message Filtering

• Subscribers receive only messages matching attribute rules  
• Reduces logic required in subscribers  
• Attribute-based filtering defined during subscription creation  

---

## Message Format

• JSON by default  
• Raw message delivery supported for SQS or Lambda  

---

## Delivery Retries and DLQ

• Automatic retries on delivery failure  
• Configurable retry policy:
  - Backoff strategy  
  - Retry attempts  
• DLQs supported (SQS as DLQ)  

---

## Access Control

• IAM policies and SNS topic access policies  
• Controls who can publish or subscribe  
• Can restrict access to specific accounts, services, or conditions  

---

## Encryption

• Server-Side Encryption (SSE) using AWS KMS  
• Protects messages at rest within SNS topics  

---

## Monitoring and Logging

• CloudWatch metrics:
  - Published messages  
  - Delivered messages  
  - Failed deliveries  
  - Delivery latency  
• CloudTrail logs API calls for auditing  

---

## Mobile Notifications

Supports mobile push notifications via:

• Amazon Device Messaging (ADM)  
• Apple Push Notification Service (APNS)  
• Firebase Cloud Messaging (FCM)  
• Baidu Cloud Push  

---

## Cross-Region and Cross-Account

• Topics can be accessed cross-account via topic policies  
• No native cross-region replication (requires Lambda or custom solution)  

---

## Limits

• Highly scalable service  
• Default limits include:
  - Number of topics  
  - Max message size (256 KB)  
• Limits can be increased via AWS Support  

---

## Pricing

• Charged per:
  - Publish requests  
  - Notification deliveries (protocol-dependent)  
• SMS pricing varies by destination country  

---

## Exam Tips

• SNS = push model, SQS = pull model  
• SNS + SQS = fan-out architecture  
• Use message filtering for targeted deliveries  
• Common subscribers: Lambda, SQS, HTTP/S  
• DLQ recommended for failed deliveries  
• Encrypt messages at rest using KMS SSE  
• IAM policies + topic access policies control access  
• Use SNS for mobile push notifications  

---

## Quick Summary

Amazon SNS is a fully managed pub/sub service that enables message delivery to multiple subscribers, supporting application decoupling, real-time notifications, and scalable fan-out messaging across AWS services and mobile platforms.

