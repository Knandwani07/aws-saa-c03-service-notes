# Amazon FSx

---

## What It Is
Amazon FSx is a fully managed AWS service that makes it simple to launch, run, and scale high-performance, feature-rich file systems in the cloud.  
It provides **native Windows and Linux file systems** without managing file servers or storage hardware.

---

## Key Features
• Fully managed by AWS (patching, backups, monitoring)  
• Multiple file system types for different workloads  
• High performance and scalable storage  
• Integrates with AWS networking and security  
• Encryption at rest and in transit  

---

## Supported File Systems

---

### 1. **Amazon FSx for Windows File Server**
• Built on Microsoft Windows Server  
• SMB protocol support  
• Supports Windows NTFS features:  
  • ACLs  
  • User quotas  
  • Shadow copies  
• Active Directory integration  
• DFS namespaces and replication  

**Use Cases:**  
• Windows-based applications  
• Home directories  
• Content management systems  

---

### 2. **Amazon FSx for Lustre**
• High-performance, POSIX-compliant file system  
• Deep S3 integration:  
  • Link S3 buckets for processing  
  • Write results back to S3  
• Sub-millisecond latencies  
• Throughput up to hundreds of GB/s  

**Use Cases:**  
• Machine learning  
• High-performance computing (HPC)  
• Media processing  

---

### 3. **Amazon FSx for NetApp ONTAP**
• Managed NetApp ONTAP file systems  
• Supports NFS, SMB, and iSCSI  
• Advanced NetApp features:  
  • Multi-protocol access  
  • Snapshots  
  • Data deduplication  
  • Compression  
  • Cloning and replication  
• FlexCache for caching across regions  
• Tier cold data to S3  

**Use Cases:**  
• Enterprise workloads  
• Disaster recovery  
• Hybrid cloud storage  

---

### 4. **Amazon FSx for OpenZFS**
• Managed OpenZFS file systems  
• POSIX-compliant, Linux-native  
• Features:  
  • Snapshots  
  • Clones  
  • Compression  
  • Encryption at rest and in transit  
• Supports NFS v3 and v4.1  
• High throughput and low latency  

**Use Cases:**  
• Linux-based apps  
• Container storage  
• Dev/test environments  

---

## Integration and Access
• Deployed inside a VPC  
• Supports Direct Connect and VPN  
• IAM integration  
• AWS Backup support  
• Supports replication across and within regions (per FS type)  

---

## Security
• KMS encryption at rest  
• SMB/NFS/TLS encryption in transit  
• VPC security groups and NACLs  
• IAM policies for access control  
• Supports AD and AWS Identity Store  

---

## Performance

### FSx for Windows File Server
• Up to tens of GB/s throughput  
• SSD and HDD options  

### FSx for Lustre
• Hundreds of GB/s throughput  
• Sub-millisecond latency  

### FSx for NetApp ONTAP
• Advanced caching  
• Deduplication & compression  

### FSx for OpenZFS
• High IOPS  
• Consistent low latency  

---

## Backup and Recovery
• Automated daily backups  
• User-initiated backups anytime  
• Snapshots for point-in-time restore  
• Replication options:  
  • ONTAP – SnapMirror  
  • Lustre – S3 integration  

---

## Monitoring and Management
• CloudWatch for performance metrics  
• CloudTrail for API logging  
• AWS Backup for centralized backup  
• Manage via Console, CLI, SDK  

---

## Pricing
Charged based on:  
• Storage capacity provisioned  
• Throughput capacity  
• Backup storage  
• Data transfer (replication)  
• SSD vs HDD pricing  

---

## Typical Use Cases
• Lift-and-shift Windows workloads  
• HPC (Lustre)  
• Hybrid enterprise storage (ONTAP)  
• Linux-native workloads (OpenZFS)  
• ML training, media rendering, genomics  

---

## Comparison Table

| FSx Type | Protocols | Best For | Key Features |
|---------|-----------|----------|--------------|
| **FSx for Windows File Server** | SMB | Windows apps, user shares | NTFS, AD, DFS, Shadow Copies |
| **FSx for Lustre** | NFS, POSIX | HPC, ML, analytics | S3 integration, sub-ms latency, high throughput |
| **FSx for NetApp ONTAP** | NFS, SMB, iSCSI | Enterprise, hybrid | Snapshots, dedupe, FlexCache, tiering |
| **FSx for OpenZFS** | NFS v3/v4.1 | Linux, container workloads | Snapshots, clones, compression, encryption |

---

## Exam Tips
• Fully managed—no server maintenance  
• FSx for Windows → SMB + AD + NTFS  
• FSx for Lustre → HPC + S3 data processing  
• FSx for ONTAP → enterprise features + multi-protocol  
• FSx for OpenZFS → Linux + ZFS features  
• Encryption at rest (KMS) + in transit  
• Integrated with VPC, IAM, CloudWatch, CloudTrail, AWS Backup  

---

## Quick Summary
Amazon FSx provides fully managed, scalable, high-performance file systems optimized for Windows, HPC, Linux, and enterprise applications. Each FSx variant is purpose-built so you can choose based on protocols, performance requirements, and storage features.

