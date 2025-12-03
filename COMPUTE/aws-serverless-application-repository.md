# AWS Serverless Application Repository (SAR)

AWS Serverless Application Repository (SAR) is a managed repository that enables developers, teams, and organizations to discover, deploy, and share serverless applications.  
It simplifies reuse of serverless components and complete applications built using AWS services.

---

## What It Is

• Fully managed repository for serverless applications  
• Supports public or private sharing within AWS accounts or organizations  
• Applications packaged using AWS SAM templates  
• Deployable from AWS Console, CLI, SDKs, or SAM CLI  
• Supports versioning for tracking application changes  
• Integrated with AWS IAM for permission control  

---

## Publishing Applications

• Developers publish serverless applications built using AWS SAM  
• Requires an AWS SAM template defining resources and configuration  
• Supports metadata such as application name, description, license, and usage details  
• Applications may be published publicly or shared with specific AWS accounts/organizations  
• Supports versioning for iterative releases and rollback  

---

## Deploying Applications

• Deploy applications directly to your AWS account from Console, CLI, or SAM CLI  
• Provisioning and deployment handled via AWS CloudFormation  
• Supports parameter customization during deployment  
• Ensforces best practices through packaging and permission validation  

---

## Security and Access Control

• Integrated with AWS IAM for fine-grained access management  
• Publishers define who can view or deploy applications  
• IAM permissions embedded in SAM templates are reviewed at deployment time  
• Automated scanning detects known security issues in published applications  

---

## Integration with AWS Services

• Works with Lambda, API Gateway, DynamoDB, Step Functions, SNS, SQS, and other serverless components  
• Deployments use CloudFormation for consistent provisioning  
• AWS SAM CLI supports local testing and publishing workflows  

---

## Benefits

• Accelerates development through reuse of validated serverless components  
• Reduces duplication of effort across teams  
• Enables sharing of standardized patterns and best practices  
• Improves consistency across an organization  
• Supports CI/CD pipelines and automated deployments  

---

## Use Cases

• Sharing serverless microservices within an organization  
• Publishing open-source serverless solutions  
• Creating internal catalogs of reusable serverless patterns  
• Rapid deployment of utilities, integrations, and common workflows  

---

## Pricing

• No cost to use SAR itself  
• You pay only for underlying AWS resources provisioned (Lambda, API Gateway, DynamoDB, etc.)  

---

## Exam Tips

• SAR is the managed repository for packaging, sharing, and deploying serverless applications  
• All applications are defined using AWS SAM templates  
• Supports both public and private sharing models  
• Deployments run through AWS CloudFormation  
• Ideal for promoting reuse and consistency in serverless environments  

---

## Quick Summary

AWS Serverless Application Repository is a fully managed platform for discovering, sharing, and deploying serverless applications defined with AWS SAM.  
It enables rapid delivery, reuse of proven architectures, and standardized serverless development across teams and organizations.

