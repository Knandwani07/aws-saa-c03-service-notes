# Amazon EFS

---

## What It Is
Amazon Elastic File System (EFS) is a fully managed, scalable, elastic NFS file system for AWS and on-premises environments. It provides shared, concurrent access to thousands of EC2 instances with automatic scaling and high durability.

---

## Key Characteristics
Managed NFS file system (NFSv4.1, NFSv4.0).  
Elastic — automatically expands and shrinks based on file storage.  
Scalable to petabytes with high throughput and IOPS.  
Accessible concurrently from multiple AZs.  
Supports POSIX permissions for file-level access control.

---

## Storage Classes

### Standard
For frequently accessed files.  
Higher cost.  
Low latency and high throughput.

### Infrequent Access (IA)
Lower cost for less frequently accessed files.  
Charged per GB stored + per access request.  
Good for content that must remain available but is rarely accessed.

### Lifecycle Management
Automatically transitions files to IA based on age.  
Policies such as “no access for 30 days.”

---

## Performance Modes

### General Purpose
Default mode.  
Low latency for transactional workloads.  
Ideal for web servers, CMS, home directories.

### Max I/O
Higher aggregate throughput.  
Higher latency.  
Best for massive parallel workloads: analytics, media processing, big data.

---

## Throughput Modes

### Bursting Throughput
Default.  
Throughput scales with file system size.  
Suitable for most workloads.

### Provisioned Throughput
Specify throughput regardless of storage size.  
For workloads demanding consistent high throughput.

---

## Availability and Durability
Data stored redundantly across multiple AZs.  
Designed for **11 nines** (99.999999999%) durability.  
Regional service — accessible from all AZs in the region.

---

## Security
KMS encryption at rest.  
TLS for in-transit encryption.  
IAM policies + POSIX permissions.  
Supports VPC security groups and NACLs.  

### EFS Access Points
Managed entry points for applications.  
Enforce user/group IDs and root access control.

---

## Mounting Options
Mount over NFS on EC2 instances.  
Mount targets in each AZ for HA.  
Supported on:  
• Linux EC2  
• On-prem via Direct Connect/VPN  
• ECS & Lambda (via Access Points)

---

## Backup and Restore
AWS Backup supports automated backups.  
Define backup plans and retention rules.  
Point-in-time restore capability.

---

## Use Cases
Content management.  
Web hosting and shared file storage.  
Home directories.  
Big data analytics.  
Media processing workflows.  
Lift-and-shift applications needing shared storage.

---

## Pricing
Charges based on:  
Storage used (Standard or IA).  
IA access requests.  
Provisioned throughput (if configured).  
Data transfer inside VPC is free; cross-region charges apply.

---

## Integration with AWS Services
EC2 — primary compute integration.  
ECS — shared persistent storage for containers.  
Lambda — native EFS integration via Access Points.  
AWS Backup — centralized automated backups.

---

## Best Practices
Enable Lifecycle Management to reduce costs.  
Use General Purpose for low-latency apps.  
Choose Max I/O for throughput-heavy, parallel workloads.  
Encrypt at rest and in transit.  
Use Access Points for secure and simplified access.  
Monitor with CloudWatch (IOPS, throughput, storage).  
Configure mount targets across all AZs for regional resilience.

---

## Exam Tips
POSIX-compliant managed NFS.  
Supports concurrent access by thousands of instances.  
Elastic scaling with no provisioning.  
Storage classes: Standard + IA.  
Performance modes: General Purpose + Max I/O.  
Encryption: KMS at rest, TLS in transit.  
Access Points for fine-grained access control.  
Can be mounted on-prem via DX or VPN.  
Integrated with AWS Backup.

---

## Quick Summary
Amazon EFS is a regional, fully managed, elastic NFS file system that scales automatically and supports massive concurrent access. With multiple storage/performance classes, robust security, and seamless AWS integration, it is ideal for shared, scalable file-based workloads across EC2, containers, serverless, and hybrid environments.

