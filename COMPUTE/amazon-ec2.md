# Amazon EC2

Amazon Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity in the AWS cloud.  
It allows you to launch virtual servers on demand, scale easily, and pay only for what you use.

---

## What It Is

• Resizable compute capacity with multiple instance types  
• Supports Linux and Windows operating systems  
• Choice of instance types optimized for compute, memory, storage, or GPU workloads  
• Flexible pricing models  
• Supports auto scaling, load balancing, and high availability architectures  
• Integrated with many AWS services (EBS, S3, IAM, VPC, CloudWatch)  

---

## EC2 Instance Types

• General Purpose — Balanced resources (t3, m5)  
• Compute Optimized — High-performance processors (c5)  
• Memory Optimized — Large memory workloads (r5, x1)  
• Storage Optimized — High sequential I/O, NVMe (i3)  
• Accelerated Computing — GPU/FPGA processing (p3, g4)  

---

## EC2 Pricing Models

1. On-Demand Instances  
– Pay by the second or hour  
– No commitment  
– Ideal for short-term, unpredictable workloads  

2. Reserved Instances (RI)  
– 1-year or 3-year commitment  
– Significant discounts  
– Standard & Convertible options  
– Best for steady-state workloads  

3. Savings Plans  
– Flexible pricing model  
– Commit to hourly spend  
– Applies to EC2, Fargate, Lambda  

4. Spot Instances  
– Up to 90% discount  
– Can be terminated with 2-minute warning  
– Ideal for batch/stateless workloads  

5. Dedicated Hosts  
– Physical servers dedicated to your use  
– Helps meet compliance/licensing  

6. Dedicated Instances  
– Hardware dedicated to you, not tied to a specific server  

7. Capacity Reservations  
– Reserve capacity in a specific Availability Zone  

---

## Storage Options

• EBS (Elastic Block Store)  
– Persistent block storage  
– Types: gp3, io1/io2, st1/sc1  
– Snapshots stored in S3  
– KMS encryption supported  

• Instance Store  
– Ephemeral local disks  
– Data lost when instance stops/terminates  
– Extremely high IOPS  

• EFS  
– Scalable network file system for Linux  

• FSx  
– Managed Windows FS or Lustre  

---

## Networking Features

• Launched inside VPC  
• Public and private IP assignments  
• Elastic IP = static public IPv4  
• Security Groups — stateful instance firewall  
• Network ACLs — stateless subnet-level rules  
• ENI — elastic network interface  
• Placement Groups:  
– Cluster → low latency, high throughput  
– Spread → place instances on distinct hardware  
– Partition → isolation for large distributed systems  

---

## Launch Options

• AMIs  
– Preconfigured OS + software templates  

• User Data  
– Boot-time scripts for automation  

• Launch Templates  
– Reusable launch configurations  

• Launch Configurations  
– Legacy option for Auto Scaling  

---

## Auto Scaling

• Automatically adjusts EC2 capacity  
• Auto Scaling Groups (ASG):  
– Set min, max, desired capacity  
– Scaling via CloudWatch alarms  
– Health checks + automatic replacement  

---

## Load Balancing

• Application Load Balancer (ALB)  
– Layer 7 routing  

• Network Load Balancer (NLB)  
– Layer 4, ultra-low latency  

• Gateway Load Balancer  
– For traffic inspection appliances  

• Classic Load Balancer  
– Legacy option  

---

## Monitoring and Management

• CloudWatch metrics, logs, alarms  
• CloudWatch Agent for OS-level metrics  
• Systems Manager (SSM):  
– Run Command  
– Patch Manager  
– Session Manager (SSH-free access)  

• CloudTrail for auditing API calls  

---

## Security

• IAM Roles for EC2  
– Temporary credentials for applications  

• Security Groups  
– Stateful inbound/outbound controls  

• Key Pairs  
– SSH for Linux, RDP for Windows  

• Encryption  
– EBS volume encryption (KMS)  
– Encrypted EBS snapshots  

---

## Purchasing Options & Cost Savings

• Use Savings Plans for flexibility  
• Use Reserved Instances for predictable workloads  
• Run Spot Instances for interruptible workloads  
• Combine Auto Scaling with On-Demand + Spot via EC2 Fleet or Spot Fleet  

---

## Placement Strategies

• Cluster Placement Group  
– High performance within a single AZ  

• Spread Placement Group  
– Distribute across different hardware  

• Partition Placement Group  
– Partition-aware deployments for isolation  

---

## High Availability & Fault Tolerance

• Deploy workloads across multiple AZs  
• Use Auto Scaling Groups with ELB  
• Assign Elastic IPs for stable addressing  
• Take regular EBS snapshots  

---

## Best Practices

• Use IAM Roles instead of static keys  
• Encrypt EBS volumes by default  
• Design stateless workloads where possible  
• Enable CloudWatch monitoring  
• Send logs to CloudWatch Logs  
• Use Auto Scaling for resilience  
• Keep instances patched via SSM  

---

## Exam Tips

• On-Demand → unpredictable workloads  
• Reserved Instances/Savings Plans → steady workloads  
• Spot Instances → cheap, interruptible workloads  
• EBS = persistent; Instance Store = ephemeral  
• Security Groups = stateful; NACLs = stateless  
• Use IAM roles, not hardcoded credentials  
• User Data runs at boot for automation  
• Placement Groups optimize performance/latency  
• Auto Scaling + ELB = high availability  

---

## Quick Summary

Amazon EC2 provides scalable virtual servers with flexible instance types, pricing models, storage, networking, and security. With Auto Scaling, Load Balancing, and deep AWS integration, EC2 powers secure, resilient, and highly available cloud architectures across all workloads.

