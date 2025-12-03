# AWS EventBridge

AWS EventBridge is a serverless event bus service for building event-driven applications.  
It ingests, filters, routes, and delivers events from AWS services, your own apps, and SaaS partners.

---

## Key Features

• Serverless event bus service for event-driven applications  
• Handles events from:
  - AWS services  
  - Custom applications  
  - SaaS partners  

---

## Core Concepts

### 1. Event Bus
• Logical pipeline that receives events  
• Types:
  - Default Event Bus: receives AWS service events  
  - Custom Event Bus: for your applications  
  - Partner Event Bus: for SaaS integrations  

### 2. Events
• JSON-formatted records describing changes in AWS resources or application state  
• Examples:
  - S3 object created  
  - EC2 instance state change  
  - Custom application events  

### 3. Rules
• Match events using event patterns  
• Determine which targets receive matched events  
• Can transform events before delivery  

### 4. Targets
• Services that receive and process events  
• Examples:
  - Lambda  
  - SNS  
  - SQS  
  - Step Functions  
  - Kinesis Data Streams  
  - EC2 (via Systems Manager Run Command)  
  - API Destinations (HTTP endpoints)  

### 5. Event Patterns
• JSON structures that filter events based on their contents  
• Rules use patterns to determine routing  

### 6. Event Archive and Replay
• Archive: store events for later analysis or compliance  
• Replay: resend archived events  
• Useful for testing, debugging, and recovery  

### 7. Schema Registry
• Discovers and stores event schemas  
• Helps developers understand and parse events consistently  
• Supports code bindings for multiple languages  

### 8. API Destinations
• Send events to external HTTP endpoints  
• Supports API keys and OAuth  
• Ideal for SaaS or custom API integrations  

### 9. Cross-Account Event Delivery
• Send events securely between AWS accounts  
• Useful for centralized logging or shared services  
• Supported by resource policies  

### 10. Partner Integrations
• SaaS providers can publish events directly to a Partner Event Bus  
• Examples: Zendesk, Datadog, PagerDuty  

---

## Key Features

• Fully managed, no servers to maintain  
• Near real-time event delivery  
• Highly scalable and reliable  
• Integrates with 200+ AWS services  
• Supports event filtering, transformation, routing  

---

## Use Cases

• Application decoupling with event-driven architecture  
• Real-time notifications and automation  
• Integrating AWS services with SaaS systems  
• Event archiving for auditing and compliance  
• Triggering workflows based on resource changes  

---

## Pricing

• Charged per event published and per event matched  
• Additional charges for event archiving and replay  
• Free tier includes millions of events per month  

---

## EventBridge vs SNS

### SNS
• Simple pub/sub  
• Broad, unfiltered push delivery  

### EventBridge
• Advanced event filtering and routing  
• SaaS integration and schema registry  
• Event archive and replay  
• Designed for event-driven architectures  

---

## Exam Tips

• Default Event Bus = AWS service events  
• Custom Event Bus = your application events  
• Partner Event Bus = SaaS provider events  
• Rules match and route events  
• Multiple targets allowed per rule  
• Archive + Replay = testing, compliance, recovery  
• Schema Registry = consistent event structure  
• API Destinations = HTTP integration outside AWS  
• Choose EventBridge over SNS for advanced routing or SaaS integration  

---

## Quick Summary

Amazon EventBridge is a serverless event bus that connects AWS services, custom applications, and SaaS products using events.  
It provides advanced event filtering, routing, archiving, and replay, making it ideal for scalable event-driven architectures.

