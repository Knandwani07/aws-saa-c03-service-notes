# Amazon S3

---

## What It Is
Amazon Simple Storage Service (Amazon S3) is an object storage service offering industry-leading scalability, durability, security, and performance.  
Store and retrieve any amount of data from anywhere on the web.

---

## Core Concepts
• **Buckets:**  
  o Top-level container for objects  
  o Globally unique name  
  o Defined in a single AWS Region  

• **Objects:**  
  o Data stored in buckets  
  o Consist of key (name), value (data), metadata, version ID  

• **Keys:**  
  o Unique identifier for an object  

• **Regions:**  
  o Buckets created in a specific AWS Region  

---

## Storage Classes
• **Standard:**  
  o Frequent access  
  o 99.999999999% durability (11 9s)  
  o 99.99% availability  

• **Intelligent-Tiering:**  
  o Automatically moves data between tiers  
  o Best for unpredictable access patterns  

• **Standard-IA:**  
  o Lower cost for infrequent access  
  o Retrieval fee applies  

• **One Zone-IA:**  
  o Single-AZ storage  
  o Cheaper but less resilient  

• **Glacier:**  
  o Archival storage  
  o Retrieval in minutes to hours  

• **Glacier Deep Archive:**  
  o Lowest-cost archival class  
  o Retrieval within 12 hours  

• **Reduced Redundancy Storage (Deprecated):**  
  o Legacy, not recommended  

---

## Durability and Availability
• **Durability:**  
  o 99.999999999% (11 9s) across all classes  

• **Availability:**  
  o Standard → 99.99%  
  o Standard-IA → 99.9%  
  o One Zone-IA → 99.5%  

---

## S3 Object Versioning
• Preserves and restores every object version  
• Can be enabled or suspended  
• Protects against unintended delete/overwrite  

---

## S3 Encryption Options

### Encryption In-Transit
o HTTPS/TLS  

### Encryption At Rest
o SSE-S3 (AWS-managed keys)  
o SSE-KMS (KMS keys + audit logs)  
o SSE-C (customer-provided keys)  
o Client-side encryption  

---

## Access Control
• **Bucket Policies:**  
  o JSON-based access rules  
  o Bucket-level permissions  

• **IAM Policies:**  
  o User/Role-based permissions  

• **ACLs:**  
  o Legacy fine-grained access  

• **Block Public Access:**  
  o Prevents public access  
  o Strongly recommended by AWS  

---

## S3 Access Points
• Simplifies access management for shared datasets  
• Each access point has its own policy  
• Supports VPC-only access  

---

## S3 Storage Lens
• Organization-wide visibility into usage  
• Identifies cost optimizations and security risks  

---

## S3 Event Notifications
• Trigger actions on object events  
• Supports:  
  o SNS  
  o SQS  
  o Lambda  

---

## S3 Lifecycle Policies
• Automate tier transitions  
• Define expiration rules for deleting objects  

---

## S3 Replication
• **Cross-Region Replication (CRR):**  
  o Replicate to another AWS Region  
  o Supports DR & compliance  

• **Same-Region Replication (SRR):**  
  o Replicate within same Region  
  o Useful for log aggregation  

• Supports replication of new & existing objects via batch operations  

---

## S3 Transfer Acceleration
• Uses CloudFront edge locations for faster uploads/downloads  
• Ideal for global distributed users  

---

## S3 Multipart Upload
• Splits large objects for parallel upload  
• Recommended for > 100 MB  
• Required for > 5 GB  

---

## S3 Select
• Retrieve only a subset of object data  
• Uses SQL-like syntax  
• Reduces data transfer cost  

---

## S3 Object Lock
• Enforces **WORM** (Write Once Read Many)  
• Supports retention periods and legal holds  
• Used for compliance and regulated workloads  

---

## S3 Access Analyzer
• Identifies publicly accessible buckets  
• Detects cross-account access risks  

---

## S3 Inventory
• CSV reports listing objects and metadata  
• Useful for compliance and auditing  

---

## S3 Batch Operations
• Perform bulk operations on millions/billions of objects  
• Supports copying, tagging, ACL updates, and Lambda execution  

---

## Security
• IAM Policies, Bucket Policies, ACLs  
• Encryption at rest & in transit  
• Block Public Access  
• VPC Endpoints for private S3 access  
• CloudTrail for auditing S3 API calls  

---

## Pricing
Charges based on:  
o Storage per GB/month  
o Requests & retrieval costs  
o Data transfer out  
o Replication charges  
o Features like S3 Select, Inventory, etc.  

---

## Integration With AWS Services
• AWS Lambda (event-driven processing)  
• CloudFront (CDN delivery)  
• Athena (query S3 data)  
• Glue (ETL)  
• Amazon Macie (sensitive data discovery)  
• AWS DataSync (large migrations)  
• Snowball/Snowmobile (offline transfer)  

---

## Exam Tips
• S3 = **object** storage (not block or file)  
• Ultra-high durability (11 9s)  
• Region-scoped buckets  
• Versioning protects against deletes/overwrites  
• Encryption options → SSE-S3, SSE-KMS, SSE-C, client-side  
• Lifecycle → automate transitions/deletions  
• Replication → CRR, SRR  
• Block Public Access → critical security control  
• Access via IAM, bucket policies, access points, ACLs  
• Transfer Acceleration speeds up global uploads  
• Object Lock → WORM compliance  
• Event notifications integrate with SNS, SQS, Lambda  

---

## Quick Summary
Amazon S3 is AWS’s highly durable, scalable, secure **object storage** service. It supports lifecycle automation, replication, strong encryption, event notifications, storage analytics, and deep integrations across the AWS ecosystem—making it essential for modern cloud storage at any scale.

