# AWS Application Migration Service (MGN)

---

## What It Is
AWS Application Migration Service (MGN) is a fully managed **lift-and-shift migration service** that moves physical, virtual, and cloud-based servers to AWS with **continuous block-level replication** and minimal downtime. It automates rehosting, reduces manual work, and simplifies large-scale migrations.

---

## Key Features

• Continuous block-level replication of source servers  
• Minimal-downtime cutover with test + final migration  
• Automated EC2 launch template creation  
• Converts source machines to run natively on AWS  
• Supports physical, VMware, Hyper-V, and cloud servers  
• Rollback capability to original environment  
• Simplifies and accelerates large migrations  

---

## How It Works

1. **Install Agent** – Deploy replication agent on each source server  
2. **Continuous Replication** – Data replicates into an AWS staging area subnet  
3. **Test Launch** – Validate workloads using automatically generated EC2 instances  
4. **Cutover Launch** – Perform final migration when ready  
5. **Post-Migration** – Optimize migrated servers using Systems Manager, Cost Explorer, etc.  

---

## Core Components

• **Replication Agent** – Installed on source machines to send block-level changes  
• **Staging Area** – Temporary AWS environment storing replicated data  
• **Launch Templates** – Auto-generated EC2 templates for test/cutover  
• **Test & Cutover Instances** – EC2 instances created for validation and final migration  

---

## Supported Use Cases

• Lift-and-shift migrations from on-premises to AWS  
• Migrating workloads from other cloud providers  
• Rehosting legacy applications with minimal modifications  
• Large datacenter migrations and DR modernization  

---

## Best Practices

• Always run **Test Launch** before cutover  
• Ensure proper **IAM permissions** for MGN  
• Monitor replication lag via **CloudWatch**  
• Tag replicated and cutover resources for cost tracking  
• Clean up staging resources after migration to reduce cost  

---

## Integration with AWS Services

• **IAM** – Access control  
• **CloudWatch** – Replication monitoring  
• **AWS Systems Manager** – Post-migration automation & patching  
• **AWS Migration Hub** – Central migration tracking  
• **AWS Cost Explorer** – Cost optimization post-migration  

---

## Pricing

• Pay-as-you-go based on number of actively replicating source servers  
• Test/cutover EC2 + EBS costs billed separately  
• No upfront fees  

---

## Exam Tips

• MGN is the **recommended lift-and-shift** migration tool  
• Replaces older **Server Migration Service (SMS)**  
• Uses **continuous replication**, not snapshots  
• Staging area subnet is required  
• Supports physical, virtual, and cloud-based servers  
• Automatically generates EC2 launch templates  
• Always test before cutover  

---

## Quick Summary
AWS Application Migration Service (MGN) enables seamless, low-downtime lift-and-shift migrations to AWS using continuous block-level replication. It automates EC2 configuration, supports testing before cutover, integrates with IAM/CloudWatch/Migration Hub, and is ideal for large-scale, quick, and low-risk migrations across physical, virtual, or cloud environments.

