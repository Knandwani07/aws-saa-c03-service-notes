# AWS License Manager

---

## What It Is

AWS License Manager is a service that helps you centrally manage, track, and enforce software licenses across AWS and on-premises environments. It reduces compliance risk, simplifies administration, and optimizes license usage especially in Bring Your Own License (BYOL) scenarios.

---

## Key Features

• Centralized license management for AWS and on-premises  
• Supports BYOL (Bring Your Own License) models  
• Define rules to track and enforce license usage  
• Integrates with AWS Systems Manager for software discovery  
• Provides visibility across accounts in an AWS Organization  
• Supports AWS Marketplace license management  

---

## License Configurations

• Define custom licensing rules:  
o Number of vCPUs or cores  
o Number of instances or sockets  
o Per-VM or per-core licensing metrics  

• Create rules aligned with vendor agreements  
• Enforce compliance by preventing overuse  

---

## License Tracking

• Automatically track license consumption  
• Supports tracking for:  
o EC2 instances  
o On-premises servers via AWS Systems Manager  

• Visibility into usage vs. defined limits  
• Generate audit-ready usage and compliance reports  

---

## Enforcement

• Enforces licensing rules at launch time  
• Prevents creation of non-compliant resources  
• Integrates with AWS Service Catalog for compliant deployments  
• Helps ensure usage follows vendor terms  

---

## Integration with AWS Systems Manager

• Uses Systems Manager Inventory to discover installed software  
• Tracks licenses across hybrid environments  
• Provides detailed usage insight across AWS and on-premises  

---

## Cross-Account Management

• Integrates with AWS Organizations for centralized governance  
• Share license configurations across multiple accounts  
• Standardize license enforcement at scale  

---

## AWS Marketplace Integration

• Manage licenses and entitlements for Marketplace products  
• Centralized view of software purchased through AWS Marketplace  
• Track and enforce Marketplace usage  

---

## Reporting and Visibility

• Dashboard for viewing license configurations and compliance status  
• Detailed reports for audits and vendor negotiations  
• Alerts for nearing license limits or compliance risks  

---

## BYOL (Bring Your Own License)

• Supports importing your existing licenses  
• Define and enforce BYOL rules for compliant usage  
• Track usage to reduce risk of non-compliance  

---

## Security and Access Control

• Integrates with IAM for fine-grained access control  
• IAM permissions define who can manage license configurations  
• CloudTrail logs API calls for auditing and compliance visibility  

---

## Pricing

• No additional cost for using AWS License Manager  
• Pay only for the underlying AWS resources  
• Helps optimize cost by preventing over-provisioning of licenses  

---

## Use Cases

• Enforcing vendor licensing rules in AWS environments  
• Centralized licensing for multi-account AWS setups  
• Managing license compliance in hybrid environments  
• Reducing cost by monitoring and optimizing license usage  
• Supporting BYOL for existing software investments  

---

## Best Practices

• Define license rules that match vendor agreements  
• Integrate with Systems Manager Inventory for accurate tracking  
• Enable cross-account sharing via AWS Organizations  
• Regularly review compliance and usage reports  
• Use IAM to restrict access to license configurations  

---

## Exam Tips

• License Manager tracks and enforces licensing rules across AWS and on-premises  
• BYOL support via custom license configurations  
• Integrated with Systems Manager for tracking installed software  
• Enforcement can prevent launching non-compliant resources  
• Supports multi-account governance via AWS Organizations  
• Manages Marketplace entitlements in addition to BYOL  

---

## Quick Summary

AWS License Manager enables centralized license tracking, enforcement, and compliance across AWS and on-premises environments. It supports BYOL, integrates with Systems Manager for discovery, enforces vendor licensing rules, and improves visibility and cost control across multi-account setups.

