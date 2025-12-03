# AWS Snowmobile

---

## What It Is
AWS Snowmobile is an **exabyte-scale** data transfer service that uses a **45-foot ruggedized truck** to physically move extremely large datasets—**up to 100 PB per Snowmobile**—from your data center into AWS.  
It is designed for scenarios where transferring data over the network is **impossible, too slow, or too expensive**.

---

## Key Features

### • Capacity
• Each Snowmobile stores **up to 100 PB**  
• Multiple Snowmobiles can be used for **exabyte-scale** migrations  

### • Use Case
Ideal when network-based transfers are not feasible, such as:  
• Data center evacuation  
• Massive archival migration  
• Large disaster recovery transfers  
• Regulatory / time-sensitive transfers  

### • Physical Security
Snowmobile is a **tractor-trailer container** equipped with:  
• GPS tracking  
• 24/7 video surveillance  
• Tamper-resistant enclosures  
• Alarm systems  
• Security escort during transit  

### • Data Security
• All data encrypted using **AES-256**  
• Encryption keys managed with **AWS KMS**  
• Keys are **never stored** inside the Snowmobile  
• Digital signatures validate data integrity  

---

## Data Transfer Workflow

1. AWS delivers the Snowmobile to your facility  
2. AWS connects it to your high-speed local network  
3. Data is copied at speeds up to **1 Tbps** (in ideal conditions)  
4. Snowmobile is physically transported to an AWS region  
5. AWS uploads the data to your **S3 buckets**  

---

## Comparison With Other Snow Services

| Service           | Capacity          | Use Case                             | Delivery Time         |
|-------------------|-------------------|---------------------------------------|------------------------|
| **Snowball Edge** | Up to 80 TB       | TB-scale transfer, edge computing     | Days–Weeks            |
| **Snowmobile**    | Up to 100 PB      | Exabyte-scale, data-center migration  | Weeks (size-dependent) |

---

## Security Considerations

• AES-256 encryption in transit and at rest  
• Keys managed via **KMS** (held only by customer)  
• Full chain-of-custody tracking  
• Security escort + hardened container  
• Strict physical and operational controls  

---

## Limitations

• Available only in select AWS regions  
• Logistically complex—requires onsite planning  
• Intended for **one-time**, massive migrations  
• Requires coordination with AWS account team  

---

## Exam Tips

• Snowmobile = **100 PB truck** for extreme data transfer  
• Used when network transfer is infeasible (bandwidth/time limits)  
• Data secured with **KMS-managed 256-bit keys**  
• Comes with escort and robust physical security  
• Don’t confuse with Snowball Edge (TB-scale)  

---

## Quick Summary
AWS Snowmobile is a physically delivered, ultra-secure data transfer solution capable of moving **up to 100 PB per unit** from your data center to AWS. It uses military-grade security, KMS-based encryption, high-speed data ingestion, and a full chain-of-custody process—making it ideal for massive, one-time data center migrations where speed and security are paramount.

