# Amazon SQS

Amazon Simple Queue Service (SQS) is a fully managed message queuing service that decouples and scales distributed systems, microservices, and serverless applications.  
It stores, transmits, and retrieves messages without requiring components to know each other’s state or location.

---

## What It Is

• Fully managed message queuing service  
• Decouples and scales distributed systems and applications  
• Stores, transmits, and retrieves messages asynchronously  

---

## Key Features

• Reliable, scalable message queuing  
• Supports Standard queues (high throughput, at-least-once delivery)  
• Supports FIFO queues (exactly-once processing, ordered delivery)  
• Fully managed, no servers to provision  
• Integrates with Lambda, SNS, ECS, Step Functions  

---

## 1. Types of Queues

### a. Standard Queue
• Default queue type  
• Nearly unlimited TPS  
• At-least-once delivery (duplicates possible)  
• Best-effort ordering  
• Use case: High-throughput apps where duplicates are acceptable  

### b. FIFO Queue (First-In-First-Out)
• Guarantees exactly-once processing  
• Preserves strict ordering  
• Up to 300 TPS (higher with batching)  
• Use case: Banking, financial transactions, inventory updates  

---

## 2. Message Lifecycle

• Producer sends a message to the queue  
• SQS stores messages redundantly across multiple AZs  
• Consumer polls queue and processes message  
• Message is deleted after processing  

---

## 3. Message Visibility Timeout

• Time during which retrieved messages remain hidden from other consumers  
• Prevents duplicate processing  
• If not deleted before timeout, message becomes visible again  

---

## 4. Dead-Letter Queues (DLQ)

• Store unprocessed or failed messages  
• Help debug problematic messages  
• Prevent endless retry loops  

---

## 5. Delay Queues

• Delay message delivery for 0–15 minutes  
• Useful for scheduled or delayed processing  

---

## 6. Long Polling

• Waits up to 20 seconds for messages  
• Reduces empty responses and lowers cost  
• More efficient than short polling  

---

## 7. Message Retention Period

• Messages stored between 1 minute and 14 days  
• Default: 4 days  

---

## 8. Message Size

• Max size: 256 KB  
• For larger payloads: use S3 with SQS Extended Client Library  

---

## 9. Encryption

• Server-Side Encryption (SSE) with AWS KMS  
• Encrypts messages at rest  

---

## 10. Access Control

• IAM policies define who can send, receive, delete, or manage queues  
• Supports resource-based policies for cross-account access  

---

## 11. Integrations

• AWS Lambda: process messages directly  
• SNS: fan-out architecture (SNS → multiple SQS queues)  
• Step Functions: orchestrate workflows  
• EventBridge: route events to SQS  

---

## 12. Cost Model

• Pay for:
  - Number of requests  
  - Payload data transfer  
• FIFO queues cost more due to ordering guarantees  

---

## 13. FIFO Queue Features

• Message groups for ordered parallel processing  
• Exactly-once delivery with deduplication:
  - Content-based  
  - Deduplication ID  
• Up to 20,000 in-flight messages per message group  

---

## 14. DLQ and Redrive Policy

• Isolate and inspect failed messages  
• Redrive policy defines:
  - Max receive count  
  - DLQ destination  

---

## 15. Limits

• Limits on queue count, throughput, in-flight messages  
• FIFO queue throughput can be increased via batching  

---

## Use Cases

• Microservice decoupling  
• Buffering workloads  
• Handling long-running tasks  
• Order-dependent workflows (FIFO)  
• Failure isolation using DLQs  

---

## Exam Tips

• Standard: high throughput, at-least-once, duplicates possible  
• FIFO: exactly-once, strict ordering  
• Visibility timeout prevents duplicate processing  
• DLQs isolate failed messages  
• Long polling reduces cost and improves efficiency  
• KMS encryption protects data at rest  
• Lambda can automatically process messages  

---

## Quick Summary

Amazon SQS is a fully managed queuing service enabling decoupled, scalable, and reliable communication between distributed application components.  
It supports Standard and FIFO queues, DLQs, encryption, long polling, and integrates seamlessly with AWS services to build robust cloud architectures.

