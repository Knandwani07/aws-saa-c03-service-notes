# AWS CloudFormation

---

## What It Is

AWS CloudFormation is an infrastructure as code (IaC) service that lets you model, provision, and manage AWS resources (and some third party resources) via declarative templates (JSON or YAML).  
You define everything (instances, networks, databases, permissions) as code; CloudFormation handles the creation, updates, deletions as “stacks”.

---

## Key Features

• Templates: YAML/JSON file with sections like Parameters, Mappings, Conditions, Resources, Outputs.  
• Stacks: A deployed collection of AWS resources defined by a template. You manage all resources as one unit.  
• Change Sets: Preview updates/changes before applying so you can see what will change or be replaced.  
• Nested Stacks / Modules / Registry: Reuse templates/components for modularizing infrastructure.  
• StackSets: Deploy stacks across multiple AWS accounts/regions with a single template.  
• Drift Detection: Detect when stack resources diverge from the declared template.  
• Integration: Works with CI/CD pipelines (since you’re a DevOps intern, this is gold).  
• Free to use for the service; you pay for the resources provisioned via CloudFormation.  

---

## Core Concepts & Components

• Template: The blueprint (YAML/JSON) defining resources.  
• Resources: The only required section in a template; each resource maps to AWS service (EC2, VPC, S3…).  
• Parameters: Inputs you can provide when creating/updating stacks for flexibility.  
• Mappings / Conditions: Provide region/OS/AMI variations or conditionally deploy resources.  
• Outputs: Values you want to export, or make available after stack creation (e.g., VPC ID).  
• Ref / GetAtt / Fn::ImportValue: Intrinsic functions for referencing resources, attributes, cross stack imports.  
• Stack: The runtime instantiation of a template (i.e., the actual deployed set of resources).  
• Cross Stack References: Export outputs from one stack and import into another (modular design).  
• Module / Nested Stack: Reusable, nested templates/components for better organization.  
• StackSet: For multi account/multi region deployments.  

---

## Security, Governance & Cost

• You control access via AWS IAM to allow who can create/update/delete stacks.  
• Don’t hard code credentials in templates; use secure parameter types, Secrets Manager or SSM Parameter Store.  
• Use Stack Policies, drift detection, CloudTrail logging to ensure governance/compliance.  
• Cost: CloudFormation itself has no extra charge; you pay for the resources the stack creates.  

---

## Use Cases

• You need repeatable infrastructure provisioning across environments (dev/stage/prod). → Use CloudFormation.  
• You want version controlled infrastructure and ability to roll back changes. → CloudFormation templates + Change Sets.  
• You must deploy identical infrastructure in multiple regions/accounts. → Use StackSets.  
• You want to modularize infrastructure (e.g., network stack, application stack referencing network outputs). → Use Cross Stack references/modules.  
• You’re building a CI/CD pipeline for infrastructure changes (DevOps flow). → Use CloudFormation integration with pipelines, change sets.  

---

## Best Practices

• Keep templates modular: separate logical parts of architecture into individual stacks.  
• Validate templates (linting, tools like cfn lint) before deploying.  
• Use version control for template files, treat as code (IaC).  
• Use Stack Policies/Change Sets before applying to production stacks.  
• Use parameter constraints, pseudo parameters, avoid hard coding credentials.  
• Monitor drift, deploy via modules, manage resource lifecycle.  

---

## Exam Tips

• If question: “Repeatable, immutable infrastructure” → CloudFormation (or CDK under the hood) is likely.  
• If they mention “deal with account/region automation” → StackSets might be the answer.  
• If they mention “preview changes” or “what will be replaced” → Look for Change Sets.  
• If they mention “resources created together / logical grouping” → Think “stack”.  
• If they require “inject variables at runtime” (like AMI ID, instance type) → Parameters/Mappings.  
• If they ask “cost of the service”, CloudFormation itself is free; you pay for underlying resources.  
• Trick: CloudFormation vs other services (e.g., Terraform) — CloudFormation is AWS native, supported by exam.  

---

## Quick Summary

AWS CloudFormation is your go to for automating and managing AWS infrastructure as code. Define resources in templates, deploy stacks, reuse modules, govern with policies, embed into DevOps pipelines. For the SAA exam you’ll often pick it when the requirement emphasizes automation, repeatability, infrastructure lifecycle management, account/region scale, and version controlled provisioning.

