# AWS Snowball Edge

---

## What It Is
AWS Snowball Edge is a **rugged, portable data transfer and edge computing device** used for TB-scale data movement and running compute workloads in remote, disconnected, or harsh environments.

---

## Key Features

### • Storage and Capacity
Two device types:

**Snowball Edge Storage Optimized**  
• 80 TB usable storage  
• Best for large-scale data transfer and local storage  

**Snowball Edge Compute Optimized**  
• 42 TB usable storage  
• More vCPUs + optional GPU (NVIDIA V100) for ML/AI and compute-heavy edge workloads  

---

## Edge Computing Capabilities

• Runs **EC2 instances locally**  
• Supports **AWS Lambda** functions for local event-driven processing  
• Can **filter, preprocess, or transform** data before sending to AWS  
• Ideal for intermittent-connectivity environments  

---

## Use Cases

• TB-scale data migration to AWS  
• Edge compute in remote/field/military operations  
• IoT and sensor data processing  
• Disaster recovery  
• Running workloads where internet is unreliable or unavailable  

---

## Data Transfer

• Secure, offline transfer workflow:  
  – Load data on-prem  
  – Ship device back to AWS  
  – AWS uploads data into your **S3 bucket**  

• Supports **import and export**  
• Local clustering enables direct transfer and redundant storage  

---

## Clustering

• Combine multiple Snowball Edge devices for:  
  – Increased storage capacity  
  – High-availability  
  – Local HDFS-compatible storage  

---

## Security

• End-to-end **AES-256 encryption**  
• Managed via **AWS KMS**  
• Tamper-resistant enclosure and seals  
• Trusted Platform Module (TPM)  
• Complete chain-of-custody tracking  
• Automatic data wipe after transfer to AWS  

---

## Ordering and Management

• Ordered through AWS Management Console  
• Managed via Snow Family Console / Snowball client CLI  
• Track device status, shipping, job progress  
• Device arrives preconfigured for your job  

---

## Networking

• Supports **10 Gb, 25 Gb, 40 Gb** network links  
• High-speed on-prem transfer interfaces  
• Works in fully disconnected edge sites  

---

## Snowball Edge Variants

| Type               | Storage Capacity | Use Case                               | Compute Capabilities                  |
|--------------------|------------------|------------------------------------------|----------------------------------------|
| Storage Optimized  | 80 TB usable     | Bulk transfer, local storage            | EC2 + Lambda                           |
| Compute Optimized  | 42 TB usable     | ML/AI, compute-heavy edge workloads     | Extra vCPUs, optional GPU (V100)       |

---

## Comparison with Snowmobile

| Feature        | Snowball Edge               | Snowmobile                         |
|----------------|------------------------------|-------------------------------------|
| Capacity       | 42–80 TB per device          | Up to 100 PB per truck              |
| Use Case       | TB-scale + edge computing    | Exabyte-scale migration             |
| Delivery       | Shipped as rugged appliance  | 45-foot secure truck                |
| Compute        | EC2 + Lambda                 | None                                |

---

## Exam Tips

• Snowball Edge = TB-scale **data transfer + edge compute**  
• Storage Optimized → bulk transfer  
• Compute Optimized → local ML/AI or EC2 workloads  
• End-to-end KMS encryption  
• Device automatically wiped after ingestion  
• Clustering supported for capacity & HA  
• Common exam clue: **disconnected remote site needing compute + transfer**  

---

## Quick Summary
AWS Snowball Edge is a rugged, portable device for **secure TB-scale data transfer and edge computing**. With local EC2, Lambda, encryption, clustering, and offline transport to S3, it is ideal for remote, bandwidth-limited, and compute-at-the-edge scenarios.

