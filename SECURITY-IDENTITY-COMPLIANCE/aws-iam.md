# AWS Identity and Access Management (IAM)

---

## What It Is
AWS Identity and Access Management (IAM) is a global AWS service that controls authentication (who) and authorization (what they can do) for AWS resources. It provides secure access management using users, groups, roles, and policies.

---

## Key IAM Concepts

### 1. IAM Users
• Represent individual people or applications  
• Have credentials (passwords, access keys)  
• Permissions assigned directly or through groups  

### 2. IAM Groups
• Collection of IAM users  
• Attach policies to groups for simplified permission management  

### 3. IAM Roles
• Provide temporary security credentials  
• Used for:  
  – EC2 instances accessing AWS services  
  – Cross-account access  
  – Federated identities (SAML/OIDC)  
  – AWS services assuming roles  
• No long-term credentials  

### 4. IAM Policies
• JSON documents defining permissions  
• Types:  
  – **AWS-managed policies**  
  – **Customer-managed policies**  
  – **Inline policies**  

### 5. IAM Policy Elements
• **Effect** – Allow or Deny  
• **Action** – API operations permitted  
• **Resource** – Target resources  
• **Condition** – Optional fine-grained controls  

### 6. Permissions Boundaries
• Set the *maximum* permissions a role or user can have  
• Useful for delegated administration  

### 7. Identity-Based vs Resource-Based Policies
• **Identity-based** – Attached to users, groups, roles  
• **Resource-based** – Attached to AWS resources (e.g., S3 bucket policy)  
• Resource-based policies allow cross-account access  

### 8. IAM Access Analyzer
• Detects resources shared outside your account  
• Helps ensure least privilege  

### 9. IAM Password Policy
• Enforces password complexity and rotation for IAM users  

### 10. Multi-Factor Authentication (MFA)
• Adds extra security using:  
  – Virtual MFA apps  
  – Hardware/U2F keys  
  – SMS MFA (less secure)  
• Strongly recommended for root and privileged users  

---

## IAM Best Practices
• Enable MFA  
• Apply least privilege  
• Rotate access keys regularly  
• Avoid using root account  
• Use IAM roles for EC2/Lambda instead of hardcoding keys  
• Use AWS Organizations + SCPs in multi-account setups  

---

## IAM Roles for Applications & Services

### EC2 Instance Profiles
• Provide temporary credentials via Instance Metadata Service (IMDS)

### Lambda Execution Role
• Grants Lambda permission to access other AWS resources  

### Cross-Account Roles
• Provide access to resources across accounts  

---

## Temporary Security Credentials
• Provided via AWS STS  
• Used for:  
  – Cross-account roles  
  – Federated users  
  – Service-based role assumption  

---

## Federation and SSO
• Supports external IdPs:  
  – SAML (Active Directory, Okta)  
  – OIDC (Google, Auth0)  
  – AWS IAM Identity Center (AWS SSO)  
• Enables single sign-on to AWS  

---

## AWS Managed vs Customer Managed Policies
• **AWS Managed** – Pre-built, automatically updated  
• **Customer Managed** – Custom and fully controllable  

---

## Service-Linked Roles
• Required for specific AWS services (ECS, Auto Scaling, etc.)  
• Managed entirely by AWS  

---

## IAM Credential Report
• CSV overview of IAM user credentials  
• Shows access key age, MFA status, password use  

---

## IAM Access Advisor
• Shows “last accessed” info for permissions  
• Helps remove unused permissions  

---

## Pricing
• IAM is free  
• Pay only for underlying AWS services used  

---

## Exam Tips
• IAM is **global**, not regional  
• Roles = temporary credentials (no passwords/keys)  
• Policies define the permissions model  
• MFA for root is mandatory best practice  
• Access Analyzer highlights unintended external access  
• Use roles for EC2/Lambda instead of long-term keys  
• Federation used for SSO with external identity providers  

---

## Quick Summary
AWS IAM is the central access control service in AWS, allowing secure management of who can access which resources using users, groups, roles, and policies. With MFA, least privilege, roles, federation, and auditing tools like Access Analyzer, IAM enables strong, scalable identity governance across the AWS environment.

