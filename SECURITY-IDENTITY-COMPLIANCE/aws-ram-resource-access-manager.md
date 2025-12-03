# AWS Resource Access Manager (AWS RAM)

---

## What It Is
AWS Resource Access Manager (RAM) is a managed service that lets you **securely share AWS resources** across AWS accounts, Organizational Units (OUs), or your entire AWS Organization without needing to duplicate infrastructure. It streamlines multi-account architectures and centralizes resource management.

---

## Why Use AWS RAM
• Centralized sharing of AWS resources  
• Eliminates redundant resources across multiple accounts  
• Enforces access controls and security boundaries  
• Simplifies multi-account architectures  
• Reduces operational effort and improves governance  

---

## Key Concepts
• **Resource Share**  
  Container holding the resources being shared and the principals receiving access.

• **Principal**  
  AWS accounts, OUs, or entire Organization that receives access to shared resources.

• **Managed Permissions**  
  Define what actions principals can take. AWS provides default managed permissions per resource type.

---

## Supported Resource Types
Examples of resources supported by AWS RAM include:

• VPC Subnets  
• Transit Gateways  
• Route 53 Resolver Rules  
• AWS License Manager configurations  
• AWS Network Firewall policies  
• AWS Outposts resources  
• Cloud WAN core network policies  
• Resource Groups  
• Service Catalog integrated custom resources  

(AWS continues to expand support for more resource types.)

---

## How It Works
1. **Create a Resource Share**  
   Select resources → choose principals → assign permissions.

2. **Invitation Process**  
   • Within AWS Organizations → automatic sharing  
   • Outside the organization → invitation must be accepted

3. **Access & Usage**  
   Shared resources show up in recipient accounts, usable within allowed permissions.

---

## Sharing Types
• **Within AWS Organization**  
  Automatic acceptance; simplest and most scalable.

• **Specific AWS Accounts**  
  Cross-account sharing; requires invitation acceptance.

• **Organizational Units (OUs)**  
  Fine-grained sharing using Organizations’ hierarchy.

---

## Permissions & Security
• Uses **IAM** for access control  
• AWS-managed permissions for resource types  
• Access can be modified or revoked anytime  
• Sharing limited to specific resources to avoid oversharing  

---

## Monitoring & Auditing
• **AWS CloudTrail**  
  Logs API calls involving RAM for auditing and compliance.

• **AWS Config**  
  Tracks configuration changes and resource-sharing compliance.

---

## Pricing
• AWS RAM is **free**  
• You only pay for the shared resources and resource consumption  
  (Example: launching EC2 in a shared subnet bills the receiving account.)

---

## Common Use Cases
• **Centralized networking**  
  Share subnets, Transit Gateways, DNS rules.  

• **Hybrid DNS resolution**  
  Share Route 53 Resolver Rules across accounts.

• **Cost optimization**  
  Avoid duplicating infrastructure.

• **License management**  
  Centrally enforce License Manager configurations.

• **Network governance**  
  Share Network Firewall and Cloud WAN policies.

---

## Best Practices
• Use AWS Organizations for simplified and automatic sharing  
• Apply least privilege with managed permissions  
• Monitor activity with CloudTrail + AWS Config  
• Regularly review shared resources  
• Tag shared resources for tracking and cost allocation  

---

## Exam Tips
• AWS RAM enables secure **cross-account resource sharing**  
• Resource Shares = the core unit of sharing  
• Sharing in AWS Organizations → **no acceptance needed**  
• Sharing outside org → **invitation required**  
• Supports VPC subnets, TGWs, Resolver rules, License Manager, etc.  
• RAM integrates with IAM + AWS Organizations  
• RAM is **free**, but resources themselves incur cost  

---

## Quick Summary
AWS Resource Access Manager (RAM) allows secure, scalable sharing of supported AWS resources across accounts, OUs, and AWS Organizations. It eliminates resource duplication, simplifies multi-account operations, and enforces access boundaries using IAM and AWS Organizations making it a critical service for modern multi-account AWS architectures.

