# Amazon EFS

---

## What It Is
Amazon Elastic File System (EFS) is a fully managed, scalable, elastic NFS file system for use with AWS services and on-premises resources.  
Provides shared, concurrent access to thousands of EC2 instances.

---

## Key Characteristics
• Managed Network File System (NFSv4.1, NFSv4.0)  
• Elastic: Automatically grows and shrinks as files are added or removed  
• Scalable: Supports petabytes of data, high levels of throughput and IOPS  
• Accessible concurrently by multiple instances across AZs  
• Supports POSIX permissions for access control  

---

## Storage Classes

### 1. Standard
o For frequently accessed files  
o Higher cost  
o Designed for low latency, high throughput  

### 2. Infrequent Access (IA)
o Lower cost for infrequently accessed files  
o Charged per GB stored and per access request  
o Ideal for files not read often but must be available  

### 3. Lifecycle Management
o Automatically moves files to IA based on age  
o Configurable transition policy (e.g., 30 days of no access)  

---

## Performance Modes

### 1. General Purpose
o Default mode  
o Low latency for latency-sensitive use cases  
o Suitable for web servers, CMS, home directories  

### 2. Max I/O
o Supports higher levels of aggregate throughput  
o Higher latencies  
o Best for big data, media processing, analytics workloads  

---

## Throughput Modes

### 1. Bursting Throughput
o Default  
o Throughput scales with file system size  
o Suitable for most workloads  

### 2. Provisioned Throughput
o Specify throughput independent of storage size  
o Useful for workloads needing higher, consistent throughput  

---

## Availability and Durability
• Data is stored redundantly across multiple AZs in a region  
• Designed for 99.999999999% (11 9s) durability  
• Regional service: accessible from all AZs in a region  

---

## Security
• Supports AWS KMS for encryption at rest  
• TLS encryption for data in transit  
• IAM policies and POSIX permissions for access control  
• Supports VPC security groups and network ACLs  
• **EFS Access Points:**  
  o Managed application access  
  o Enforce user and group identities, root access control  

---

## Mounting Options
• Mount directly on EC2 instances using NFS protocol  
• Mount targets in each AZ for high availability  
• Supported on:  
  o Linux EC2 instances  
  o On-premises servers via AWS Direct Connect or VPN  
  o AWS services like ECS and Lambda (via EFS Access Points)  

---

## Backup and Restore
• AWS Backup supports EFS file systems  
• Centralized, automated backup service  
• Define backup plans and retention policies  
• Point-in-time recovery of file systems  

---

## Use Cases
• Content management  
• Web serving and hosting  
• Home directories  
• Big data and analytics  
• Media processing workflows  
• Application lift and shift  

---

## Pricing
Charged based on:  
o Storage used (Standard or IA)  
o Requests to IA storage class  
o Provisioned throughput (if used)  
o Data transfer within VPC is free; cross-region transfer incurs charges  

---

## Integration with Other AWS Services
• EC2 – primary mounting target  
• ECS – persistent shared storage for containers  
• Lambda – native EFS integration with Access Points  
• AWS Backup – centralized backup and restore  

---

## Best Practices
• Use Lifecycle Management to reduce costs  
• Choose General Purpose performance mode for low-latency workloads  
• Use Max I/O for parallel, throughput-heavy workloads  
• Encrypt data at rest and in transit  
• Use Access Points to simplify and secure access  
• Monitor throughput, IOPS, and storage via CloudWatch  
• Deploy mount targets in each AZ for regional redundancy  

---

## Exam Tips
• EFS is POSIX-compliant, fully managed NFS  
• Supports concurrent access from thousands of instances  
• Automatically scales with usage  
• Two storage classes: Standard & IA  
• Two performance modes: General Purpose & Max I/O  
• Encryption at rest (KMS) and in transit (TLS)  
• Access Points = fine-grained access control  
• Supports hybrid access via Direct Connect or VPN  
• Integrated with AWS Backup  

---

## Quick Summary
Amazon EFS is a regional, elastic, fully managed NFS system supporting massive concurrency, multiple performance/storage classes, POSIX permissions, encryption, and seamless integration with AWS compute and container services.  
Perfect for scalable, shared, highly available file-based workloads.

