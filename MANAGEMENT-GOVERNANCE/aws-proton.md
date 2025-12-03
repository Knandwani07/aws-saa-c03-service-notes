# AWS Proton

---

## What It Is

AWS Proton is a fully managed delivery service that standardizes and automates the provisioning and deployment of container-based and serverless applications. Platform teams define reusable infrastructure + CI/CD templates, and developers deploy services from those templates ensuring speed, consistency, and governance across the organization.

---

## Key Features

• Template-based architecture with Environment Templates and Service Templates  
• Infrastructure as Code support using CloudFormation and Terraform  
• Versioned templates with controlled upgrades (major/minor versions)  
• Git-based template sync and automated version creation  
• Automated provisioning of CI/CD pipelines alongside application infrastructure  
• Supports AWS-managed, self-managed, and cross-account environments  

---

## Core Concepts & Components

### Environment Template  
Defines shared infrastructure (VPCs, clusters, load balancers) consumed by multiple services.

### Service Template  
Blueprint for a specific application or microservice including infrastructure + deployment pipeline.

### Service Instance  
A deployed copy of a Service Template inside an environment.

### Component  
Optional add-on infrastructure that attaches to a service instance.

### Template Bundle  
A ZIP/YAML package stored in S3 or Git, containing IaC files, manifests, and schema definitions.

### Template Versions  
Minor = backward compatible  
Major = may include breaking changes  

---

## Security, Governance & Cost

• Centralized architecture governance to ensure developers use only approved standards  
• IAM roles/policies control access to environments, templates, and deployments  
• No additional Proton service cost — pay only for provisioned AWS resources  
• Helps eliminate configuration drift and enforce compliance organization-wide  

---

## Use Cases

• Standardizing microservice and serverless deployments across teams  
• Providing self-service infrastructure + CI/CD workflows to developers  
• Enforcing architectural best practices via template versioning  
• Managing large-scale microservice fleets with regulated upgrade paths  

---

## Best Practices

• Keep templates modular for easier updates and maintenance  
• Use versioning to manage evolutionary changes in infrastructure  
• Integrate Proton with CloudFormation or Terraform for IaC consistency  
• Monitor template drift and automate upgrades across environments and services  

---

## Exam Tips

• Keywords: “self-service deployment”, “standardized templates”, “automated CI/CD”, “governed deployments”  
• Proton ≠ CloudFormation (IaC only)  
• Proton ≠ Service Catalog (product catalog)  
• Proton = governed, template-based application deployment platform  
• Ideal answer when the question mentions “platform teams building standard stacks”  

---

## Quick Summary

AWS Proton is a managed service that automates and governs deployment of containerized and serverless applications using standardized, versioned templates. It unifies IaC, CI/CD, governance, and self-service, enabling developers to deploy quickly while maintaining centralized platform control.

