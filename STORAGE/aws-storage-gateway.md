# AWS Storage Gateway

---

## What It Is
AWS Storage Gateway is a hybrid cloud storage service that connects on-premises environments to AWS storage infrastructure.  
It enables seamless integration between on-prem applications and cloud storage for backup, archiving, disaster recovery, and tiered storage use cases.

---

## Gateway Types

---

### 1. File Gateway (NFS / SMB)
• Provides file-based access to objects in Amazon S3  
• Interfaces with on-prem apps via NFS or SMB  
• Files are stored as S3 objects  
• Frequently accessed data is cached locally for low-latency access  
• Supports **Amazon S3 Object Lock** for WORM compliance  

**Use Cases:**  
o File server replacement  
o Backup storage  
o Data lake ingestion  

---

### 2. Volume Gateway (iSCSI)
• Presents cloud-backed block storage to on-prem servers via iSCSI  
• Two modes:

**Stored Volumes:**  
o Primary data stored locally  
o Asynchronous backups to AWS via EBS Snapshots  
o Low-latency access with local storage  

**Cached Volumes:**  
o Primary data stored in AWS  
o Frequently accessed data cached locally  
o Reduces on-prem storage needs  

**Use Cases:**  
o Local applications with cloud backup  
o Disaster recovery  

---

### 3. Tape Gateway (VTL)
• Appears as a virtual tape library (VTL) to backup applications  
• Compatible with enterprise backup tools  
• Virtual tapes stored in S3  
• Archived tapes stored in S3 Glacier or Glacier Deep Archive  
• Eliminates physical tape infrastructure  

**Use Cases:**  
o Backup/archive replacement  
o Long-term compliance storage  

---

## Deployment Options
• Deploy on VMware ESXi, Microsoft Hyper-V, or Amazon EC2  
• Requires local disk for cache + upload buffer  
• Secure connection to AWS via HTTPS  
• Managed using Storage Gateway Console or AWS CLI  

---

## Security
• TLS encryption for all in-transit data  
• KMS encryption for all data at rest  
• Supports IAM for API-level access control  
• File Gateway integrates with Active Directory for SMB permissions  

---

## Monitoring & Management
• Integrated with:  
  o Amazon CloudWatch (monitoring)  
  o AWS CloudTrail (API auditing)  
  o AWS Backup (Volume & Tape Gateway backup policies)  

• Automatic software + configuration updates  

---

## Storage Integration

| Gateway Type | Access Protocol | AWS Backend Storage | Caching | Use Case |
|--------------|----------------|----------------------|---------|----------|
| File Gateway | NFS / SMB | Amazon S3 | Local disk | File shares, ingest to S3 |
| Volume Gateway | iSCSI | EBS Snapshots (Stored/Cached) | Local (optional) | Block storage with cloud backup |
| Tape Gateway | iSCSI (VTL) | S3 + Glacier | Local disk | Virtual tape backup/archive |

---

## Data Durability and Availability
• Inherits S3's 11-nines durability  
• Glacier provides long-term archival durability  
• Automatic replication and failover through AWS backend infrastructure  

---

## Exam Tips
• **File Gateway** → File interface that stores data as S3 objects  
• **Volume Gateway** → Block storage over iSCSI  
• **Tape Gateway** → Virtual tape library backed by S3/Glacier  
• **Cached Volumes** → Data in AWS, cached locally  
• **Stored Volumes** → Data stored locally, backed up to AWS  
• Commonly used for hybrid cloud, DR, and backup scenarios  
• Security: TLS in transit + KMS at rest + IAM  
• AWS Backup manages Volume & Tape Gateway backups  

---

## Quick Summary
AWS Storage Gateway provides File, Volume, and Tape gateways to bridge on-prem environments with AWS cloud storage.  
It enables hybrid storage workflows, cloud-backed backups, archival, and compliance storage, offering local caching, encryption, and seamless integration with AWS services.

