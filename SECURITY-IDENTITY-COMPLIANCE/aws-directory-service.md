# AWS Directory Service

---

## What It Is
AWS Directory Service is a fully managed service that lets you run Microsoft Active Directory (AD) in AWS, or connect AWS resources to your existing on-premises AD. It enables centralized user authentication, authorization, and seamless integration with Microsoft AD-aware applications.

---

## Why Use AWS Directory Service
• Centralized user authentication and access control  
• Enable SSO for AWS applications and workloads  
• Support Microsoft AD–aware workloads (SQL Server, SharePoint, WorkSpaces, etc.)  
• Simplify user/group management with directory integration  

---

## Directory Types

---

### 1. **AWS Managed Microsoft AD**
• Actual Microsoft Active Directory running natively on AWS  
• AWS manages patching, monitoring, backups, and multi-AZ deployment  
• Supports **trust relationships** with on-prem AD  
• Full AD features: Kerberos, NTLM, Group Policy, LDAP, domain join  

**Editions:**  
• Standard Edition – up to ~5,000 objects  
• Enterprise Edition – up to ~500,000 objects  

**Best For:** Enterprise workloads, hybrid AD environments, full AD compatibility  

---

### 2. **AD Connector**
• A directory proxy that connects AWS to your existing on-premises AD  
• No directory data stored in AWS  
• Provides pass-through authentication to on-premises AD  

**Use Cases:**  
• Reuse existing AD identities  
• Provide SSO to AWS Console and AWS applications  
• No need to manage AD in AWS  

**Limitations:** Requires stable network connectivity to on-premises AD  

---

### 3. **Simple AD**
• Low-cost, standalone directory powered by **Samba 4**  
• Provides basic AD-like capabilities  
• Does **not** support trust relationships  

**Sizes:**  
• Small – up to 500 users  
• Large – up to 5,000 users  

**Best For:** Small organizations needing inexpensive AD-compatible features  

---

## Integration with AWS Services
• **Amazon WorkSpaces** – user authentication  
• **Amazon WorkMail** – native with Managed Microsoft AD  
• **Amazon WorkDocs** – use AD groups and credentials  
• **EC2 Windows Instances** – domain join support  
• **AWS IAM Identity Center (SSO)** – Directory as identity source  
• Applications using LDAP/Kerberos/Group Policy  

---

## Security
### AWS Managed Microsoft AD
• Multi-AZ high availability  
• Daily automatic snapshots  
• KMS encryption for data at rest  
• Strong password and account policies  

### AD Connector
• No credential storage in AWS  
• Relies on on-premises AD security  

### Simple AD
• AWS-managed directory  
• Basic security features  

---

## Pricing
• **Managed Microsoft AD** – charged per domain controller hour  
• **AD Connector** – charged per connector hour (Small/Large)  
• **Simple AD** – charged per directory hour based on size  

---

## Use Cases
• Migrating Windows workloads to AWS while retaining AD integration  
• Centralizing user authentication across AWS services  
• Enabling domain join for EC2 Windows instances  
• Providing SSO for AWS resources using existing AD users  
• Supporting WorkSpaces, WorkDocs, and WorkMail deployments  

---

## Exam Tips
• Managed Microsoft AD = full Microsoft AD in AWS + trust relationships  
• AD Connector = proxy to on-prem AD, no data stored in AWS  
• Simple AD = low-cost AD-compatible option, no trust relationships  
• Managed Microsoft AD supports Kerberos, NTLM, GPOs, MFA via AD FS  
• AD Connector requires reliable connectivity to on-prem AD  
• Integrates with WorkSpaces, WorkMail, WorkDocs, EC2 Windows, and IAM Identity Center  
• Multi-AZ deployment ensures high availability  

---

## Comparison Table

| Feature | AWS Managed Microsoft AD | AD Connector | Simple AD |
|--------|---------------------------|--------------|-----------|
| Type | Fully managed Microsoft AD | Proxy to on-prem AD | Standalone AD-compatible directory |
| AWS-Hosted Directory | Yes | No | Yes |
| Trust Relationships | Yes | Uses on-prem AD | No |
| Group Policy Support | Yes | Through on-prem AD | Limited |
| Use Cases | Enterprise AD workloads, hybrid AD | Reuse on-prem AD without migration | Small-scale, simple AD needs |
| Editions/Sizes | Standard / Enterprise | Small / Large | Small / Large |
| Typical Customers | Enterprises | Organizations with existing AD | Small teams |

---

## Quick Summary
AWS Directory Service provides multiple directory options for AWS environments.  
• **AWS Managed Microsoft AD** offers full-featured Microsoft Active Directory in AWS.  
• **AD Connector** lets AWS authenticate users against on-prem AD without migration.  
• **Simple AD** provides a low-cost AD-compatible directory for small workloads.  
Together they simplify identity management, enable SSO, and support Microsoft AD–aware applications in AWS.

