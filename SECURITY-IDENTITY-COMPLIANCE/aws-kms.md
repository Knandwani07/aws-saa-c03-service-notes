# AWS Key Management Service (AWS KMS)

---

## What It Is
AWS Key Management Service (KMS) is a **fully managed encryption and key management service** used to create, control, rotate, and audit encryption keys across AWS. It integrates seamlessly with most AWS services to secure data at rest and in transit.

---

## Key Features
• **Customer Master Keys (CMKs)**  
  – Core resources used for encryption operations  
  – Types: AWS-managed keys, customer-managed keys, and imported keys  
  – Controlled via IAM policies and key policies  

• **AWS-managed keys**  
  – Fully automated by AWS  
  – Minimal configuration; used for default encryption  

• **Customer-managed CMKs**  
  – Full lifecycle control (rotation, permissions, deletion)  
  – CloudTrail logs all usage  
  – Best for compliance and sensitive workloads  

• **Envelope Encryption**  
  – KMS generates a data key  
  – Data key encrypts data; CMK encrypts the data key  
  – Efficient and scalable for large datasets  

• **Import Your Own Keys (IYOK)**  
  – Bring externally generated keys into KMS  
  – Helps meet strict regulatory requirements  

• **Multi-Region Keys**  
  – Replicate CMKs across AWS Regions  
  – Useful for global applications requiring low-latency decrypts  

• **CloudTrail Integration**  
  – Logs every encryption/decryption and key operation  
  – Essential for auditing and compliance workflows  

---

## How It Works
• Applications call the KMS API to **encrypt or decrypt data keys**  
• KMS uses **FIPS 140-2 validated HSMs** for secure key operations  
• CMK plaintext **never leaves KMS**  
• Data encryption happens using **data keys**, not CMKs directly  
• CMKs encrypt the data keys (envelope encryption pattern)  

---

## Use Cases
• Encrypting **S3 objects** using SSE-KMS  
• Encrypting **EBS volumes** and snapshots  
• Encrypting **RDS databases** and Aurora clusters  
• Securing **Lambda environment variables**  
• Application-layer encryption with GenerateDataKey API  
• Compliance-driven key management for regulated workloads  

---

## Pricing
• Monthly charge per customer-managed CMK  
• Additional cost per KMS API call (Encrypt, Decrypt, GenerateDataKey, etc.)  
• AWS-managed keys included at no additional cost for many services  

---

## Security & Compliance
• Backed by **FIPS 140-2 validated HSMs**  
• Customers define key policies and IAM controls  
• All usage logged via CloudTrail for full visibility  
• Keys remain **Region-scoped** unless using multi-Region CMKs  
• Supports key rotation (automatic for AWS-managed keys; optional for CMKs)  

---

## Exam Tips
• KMS = central service for encryption key management across AWS  
• CMKs can be AWS-managed or customer-managed  
• SSE-KMS = S3 encrypted with KMS keys  
• Envelope encryption = CMK encrypts data key; data key encrypts data  
• Use CloudTrail for logging key usage and auditing  
• Import your own keys when strict compliance requires full control  
• Need dedicated hardware + full ownership? → Use **CloudHSM**, not KMS  
• Multi-Region CMKs enable cross-region encryption/decryption  

---

## Quick Summary
AWS KMS provides secure, scalable, and fully managed encryption key management across AWS. It integrates deeply with services like S3, EBS, RDS, and Lambda, supports envelope encryption for performance, and offers detailed access control and auditing through IAM and CloudTrail. Ideal for securing sensitive workloads and meeting compliance requirements.

