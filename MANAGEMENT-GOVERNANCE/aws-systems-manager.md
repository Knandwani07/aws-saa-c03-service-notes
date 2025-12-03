# AWS Systems Manager (SSM)

---

## What It Is
AWS Systems Manager (SSM) is a centralized operational hub that lets you manage, automate, monitor, patch, and remotely access your AWS and on-premises infrastructure — without needing SSH, bastion hosts, or manual maintenance scripts.

---

## Key Capabilities

### **1. SSM Agent**
• Installed on EC2/on-prem servers  
• Enables Systems Manager to communicate with and manage the instance  

### **2. Session Manager**
• Browser/CLI-based shell access with **no SSH keys, no open ports, no bastion**  
• IAM-based access control  
• Fully logged in CloudTrail/CloudWatch Logs  

### **3. Run Command**
• Run shell/PowerShell commands across multiple instances simultaneously  
• No login required  
• Great for bulk updates, config changes, or ad-hoc fixes  

### **4. Automation**
• Automates repetitive tasks (patching, backups, AMI creation, remediation)  
• Uses Automation Documents (runbooks) — AWS-provided or custom  

### **5. Patch Manager**
• Automates OS patching for EC2 and on-prem servers  
• Patch baselines + maintenance windows for controlled updates  

### **6. Parameter Store**
• Secure storage for configuration variables and secrets  
• Supports plaintext and KMS-encrypted values  
• Widely used by Lambda, EC2, ECS, and CI/CD pipelines  

### **7. Inventory**
• Collects software + configuration metadata across instances  
• Helps with audits, compliance, and visibility  

### **8. State Manager**
• Enforces desired state configs (e.g., antivirus installed, NTP settings)  
• Applies configs periodically or continuously  

### **9. OpsCenter**
• Centralized view of operational issues (OpsItems)  
• Integrated with CloudWatch + Config for troubleshooting insights  

### **10. Change Manager**
• Built-in change approval workflows  
• Ensures safe, governed modifications to infrastructure  

---

## Use Cases
• Patch and maintain EC2 fleets at scale  
• Secure, auditable remote access without SSH  
• Store secrets/config outside code via Parameter Store  
• Automate compliance tasks and remediation  
• Bulk operations across instances using Run Command  
• Create/rotate AMIs automatically  

---

## Security & IAM
• IAM controls access to SSM features, documents, and Parameter Store values  
• CloudTrail logs all SSM activity  
• Parameter Store supports KMS encryption for secrets  
• Session Manager eliminates SSH keys and exposed ports  

---

## Pricing
• Many features are **free**: Run Command, Session Manager, Patch Manager, Parameter Store (Standard)  
• Costs apply for:  
  – Parameter Store **Advanced** params  
  – Automation step charges (beyond free tier)  
  – OpsCenter integrations  
  – API usage in high volume  

---

## Exam Tips
• Session Manager = secure, auditable, no SSH/bastion  
• Run Command = multi-instance scripting without login  
• Parameter Store = config + secrets (use KMS for encryption)  
• Patch Manager = automated patch compliance  
• Automation = runbooks for repetitive tasks  
• **SSM Agent must be installed and running** on managed instances  

---

## Quick Summary
AWS Systems Manager unifies automation, security, and operational control for AWS and on-prem servers. It enables secure access, fleet-wide updates, patching, configuration enforcement, and secrets management — all without manual SSH or custom tooling.

