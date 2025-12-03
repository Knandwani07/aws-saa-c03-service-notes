# Amazon EBS

---

# What It Is
  Amazon Elastic Block Store (EBS) is durable block storage for EC2 instances. Provides persistent volumes that remain even after instance stops or terminates. Volumes can only attach        within the same Availability Zone.

---

# Key Characteristics
• Block-level storage for EC2
• Persistent, AZ-scoped storage
• 99.999% availability
• Snapshot support (incremental, stored in S3)
• Encrypted with AWS KMS (at rest + in transit)
• Volumes can be resized without downtime (Elastic Volumes)

---

# EBS Volume Types

1. General Purpose SSD (gp3)
• Baseline 3,000 IOPS  
• Can provision up to 16,000 IOPS  
• Up to 1,000 MB/s throughput  
• Ideal for boot volumes, dev/test workloads  

2. Provisioned IOPS SSD (io1 / io2)
• High-performance for critical workloads  
• io1 supports up to 64,000 IOPS  
• io2 has higher durability (99.999% SLA)  
• Supports Multi-Attach across multiple EC2 instances  

3. Throughput Optimized HDD (st1)
• Low-cost, high throughput  
• Up to 500 MB/s  
• For big data, logs, streaming  
• Cannot be used as boot volume  

4. Cold HDD (sc1)
• Lowest cost  
• Up to 250 MB/s  
• For infrequently accessed workloads  
• Cannot be used as boot volume

---

# Volume Features
• Replicated within an AZ for durability  
• Elastic Volumes allows modifying size, IOPS, type without downtime  
• Snapshots are incremental and restorable across regions  
• FSR (Fast Snapshot Restore) reduces initialization latency  
• Encryption covers volumes, snapshots, and transit  

---

# Performance
• Performance depends on volume type + size  
• gp3 allows independent tuning of IOPS + throughput  
• io1/io2 provide predictable high performance  
• gp3 supports bursting  

---

# Multi-Attach (io1/io2)
• Attach one volume to multiple Nitro-based EC2 instances  
• Supports clustered / shared-disk workloads  

---

# Snapshots
• Stored in S3 (not visible as objects)  
• Incremental backups  
• Can be copied cross-region  
• Used to create new volumes or restore existing ones  

---

# EBS Lifecycle Manager
• Automates snapshot creation, retention, deletion  
• Helps maintain compliance and DR strategies  

# Data Lifecycle
• Create volume in an AZ  
• Attach to EC2 in same AZ  
• Detach / reattach to other instances  
• Delete when done  
• Snapshots allow cross-region restoration  

---

# Security
• Encrypted with AWS KMS  
• IAM controls access to volumes + snapshots  
• Encrypted snapshots can be shared cross-account with KMS permissions  
• Transparent encryption for data in transit  

---

# Pricing
• Pay per GB/month of provisioned capacity  
• Pay for provisioned IOPS on io1/io2  
• Snapshot storage billed per GB-month  
• FSR incurs hourly cost  
• Cross-AZ/Region transfer billed  

---

# Best Practices
• Use gp3 for general workloads  
• Use io1/io2 for critical, latency-sensitive workloads  
• Enable encryption by default  
• Automate backups with Lifecycle Manager  
• Monitor performance via CloudWatch  
• Use Multi-Attach for shared disk systems  
• Use Fast Snapshot Restore for production recovery  

---

# Exam Tips
• EBS persists independently of EC2  
• Snapshots are incremental + stored in S3  
• gp3 = adjustable IOPS/throughput  
• io1/io2 = high IOPS + Multi-Attach  
• st1/sc1 = HDD, cannot be boot volumes  
• FSR improves initialization speed  
• Must be created in same AZ as EC2  

---
# Quick Summary
Amazon EBS is durable block storage for EC2 with multiple performance tiers, encryption, snapshots, and advanced features like Multi-Attach and Fast Snapshot Restore.
