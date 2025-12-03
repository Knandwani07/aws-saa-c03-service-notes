# AWS Transfer Family

---

## What It Is
AWS Transfer Family is a **fully managed file transfer service** that lets you move files into and out of **Amazon S3** or **Amazon EFS** using traditional protocols like **SFTP, FTPS, and FTP**.  
It replaces legacy FTP servers with a secure, scalable, highly available AWS-managed solution.

---

## Supported Protocols

• **SFTP** (Secure File Transfer Protocol)  
• **FTPS** (FTP over SSL/TLS)  
• **FTP** (unencrypted, for legacy-only use cases)  

---

## Key Features

• Fully managed—no servers to provision or maintain  
• Native integration with:  
  – Amazon S3  
  – Amazon EFS  
• Auto-scales to thousands of concurrent connections  
• Supports custom domain names with ACM  
• Highly available across multiple AZs  
• Multiple authentication options:  
  – Service-managed users  
  – AWS Directory Service (Active Directory)  
  – Custom identity provider using API Gateway + Lambda  

---

## Storage Integration

### **Amazon S3**
• Files land directly into S3 buckets  
• Supports S3 access points for granular permissions  

### **Amazon EFS**
• Use EFS as the backend for file transfer workloads  
• Supports POSIX-compatible shared access  

---

## Security

**Data in transit**  
• SFTP/FTPS encrypted  
• FTP unencrypted (legacy use only)  

**Data at rest**  
• Uses S3/EFS encryption  
• Supports KMS-managed keys  

**Access & Network Security**  
• IAM policies for user permissions  
• CloudTrail logging  
• VPC Security Groups & VPC endpoints for private connectivity  

---

## User Management

**Service-managed identities**  
• Credentials and folder mappings stored in AWS  

**Directory Service (AD)**  
• Integrates with Active Directory for unified authentication  

**Custom Identity Provider**  
• API Gateway + Lambda for external identity systems  

---

## Availability & Scalability

• Highly available (multi-AZ architecture)  
• Automatically scales with workload  
• No infrastructure management required  

---

## Monitoring & Logging

• **CloudWatch** — metrics, connection counts, data transfer  
• **CloudTrail** — API auditing and configuration history  

---

## Typical Use Cases

• Replace on-prem FTP/SFTP servers  
• Secure partner/vendor file exchange  
• Load files into S3 data lakes  
• Provide SFTP/FTPS access to EFS-backed applications  

---

## Pricing

• Based on:  
  – Endpoint hours  
  – Data uploaded / downloaded  
  – S3 or EFS storage costs  
• No upfront commitments  

---

## Comparison with AWS Storage Gateway

| Feature            | AWS Transfer Family                      | AWS Storage Gateway                              |
|-------------------|-------------------------------------------|--------------------------------------------------|
| Purpose           | Protocol-based file transfer              | Hybrid storage integration                       |
| Protocols         | SFTP, FTPS, FTP                           | NFS, SMB, iSCSI                                  |
| Storage Backend   | S3, EFS                                   | S3, EBS Snapshots, Glacier                       |
| Use Case          | Partner file exchange, legacy FTP replace | Backup, DR, hybrid cloud workflows               |

---

## Exam Tips

• Transfer Family provides **SFTP/FTPS/FTP** access directly into **S3/EFS**  
• Ideal answer for “replace legacy FTP servers with a managed service”  
• Custom authentication = API Gateway + Lambda  
• Supports private connectivity using VPC endpoints  
• IAM + CloudTrail + encryption for security & auditing  
• Auto-scaling and multi-AZ high availability  

---

## Quick Summary
AWS Transfer Family is a **secure, scalable, fully managed** service that provides **SFTP, FTPS, and FTP** file transfer directly to **Amazon S3 or EFS**, enabling seamless modernization of legacy file transfer workflows without needing to run your own servers.

