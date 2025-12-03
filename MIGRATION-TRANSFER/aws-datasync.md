# AWS DataSync

---

## What It Is
AWS DataSync is a fully managed data transfer service for **fast, automated, and secure** movement of large datasets between on-premises storage and AWS services. It supports one-time migrations and ongoing scheduled transfers, eliminating the need for custom scripts or manual operations.

---

## Key Features

• Up to **10x faster** than open-source transfer tools  
• Automates validation, scheduling, monitoring, encryption  
• Preserves metadata, POSIX permissions, and ACLs  
• Ensures integrity with built-in checksum verification  
• No infrastructure to manage beyond the on-premises agent  

---

## Supported Transfer Locations

**On-Premises:**  
• NFS  
• SMB  

**AWS Services:**  
• Amazon S3  
• Amazon EFS  
• Amazon FSx for Windows File Server  
• Amazon FSx for Lustre  
• AWS Snowcone (via DataSync agent)  
• S3-compatible storage  

---

## How It Works

1. Deploy a **DataSync Agent** on-premises (VMware, Hyper-V, EC2).  
2. Connect the agent to on-prem NFS/SMB shares.  
3. Configure **source** and **destination** locations.  
4. Create **tasks** to transfer data (one-time or scheduled).  
5. Data moves securely over Direct Connect, VPN, or Internet.  

Supports:  
• Scheduled transfers  
• Incremental sync (only changed data)  

---

## Performance

• Purpose-built transfer protocol for maximum throughput  
• Parallel, multi-threaded operations  
• Handles millions of files and hundreds of TB  
• Bandwidth throttling to avoid network saturation  

---

## Security

• TLS encryption in transit  
• S3 SSE + SSE-KMS support for encryption at rest  
• IAM-based access control  
• VPC endpoints for private connectivity  
• CloudTrail logs API activity for auditing  

---

## Monitoring & Management

• Console + CLI for configuration and control  
• CloudWatch metrics for throughput, errors, durations  
• SNS alerts via CloudWatch alarms  
• CloudTrail for audit logging  

---

## Pricing

• Charged **per GB transferred**  
• Additional AWS storage costs apply (e.g., S3, EFS, FSx)  

---

## Typical Use Cases

• **Data Migration:** On-prem → AWS  
• **Ongoing Replication:** Backup + DR strategies  
• **Hybrid Workflows:** Sync data between sites  
• **AWS-to-AWS Transfers:** Example: S3 ↔ EFS, FSx ↔ S3  

---

## Integration with AWS Services

• **Amazon S3** – Object storage ingestion/archival  
• **Amazon EFS** – POSIX file system migration  
• **Amazon FSx** – Windows/Lustre workloads  
• **AWS Snowcone** – Edge device transfers  
• **CloudWatch** – Monitoring  
• **CloudTrail** – Auditing  

---

## Data Validation & Integrity

• Automatic checksum verification  
• Ensures 1:1 data accuracy between source and destination  
• Detailed logs for auditing and compliance  

---

## Performance Tuning

• Adjustable bandwidth limits  
• Schedule transfers during off-peak hours  
• Incremental copying → only changed files  

---

## Comparison with Other Services

| Service              | Use Case                               | Key Difference                                      |
|----------------------|------------------------------------------|------------------------------------------------------|
| AWS DataSync         | Fast, automated bulk transfer            | Optimized for NFS/SMB + high-speed protocol         |
| AWS Snowball         | Offline petabyte-scale transfer          | Physical device, no network required                |
| AWS Transfer Family   | SFTP/FTP-based file access               | Protocol-driven user uploads/downloads              |
| AWS Storage Gateway   | Hybrid cloud storage integration         | Provides mounted file/volume/tape interfaces        |

---

## Exam Tips

• DataSync = automated, high-speed data transfer  
• Supports **NFS, SMB, S3, EFS, FSx, Snowcone**  
• Requires **DataSync Agent** for on-prem sources  
• Uses **TLS** for in-transit encryption  
• IAM used for access control  
• Built-in integrity checks (checksums)  
• Supports scheduled + incremental transfers  
• Monitored via CloudWatch, audited via CloudTrail  
• Preferred over manual scripts/tools for speed + reliability  

---

## Quick Summary
AWS DataSync is an automated, scalable, and secure data transfer service for moving large datasets between on-prem and AWS. With built-in validation, encryption, scheduling, and high-speed transfer capabilities, it is ideal for migrations, replication, hybrid architectures, and large-scale AWS-to-AWS data workflows.

