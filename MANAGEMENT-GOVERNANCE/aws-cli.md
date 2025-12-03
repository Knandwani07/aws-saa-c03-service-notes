# AWS Command Line Interface (CLI)

---

## What It Is

The AWS CLI is a unified command-line tool that enables you to interact with nearly all AWS services directly from your terminal. It supports automation, scripting, CI/CD integration, and replaces manual console operations with repeatable commands.

---

## Key Features

• Single tool to manage AWS services through commands  
• Works on Windows, macOS, Linux, and AWS CloudShell  
• Supports multiple configuration profiles and regions  
• Commands can run interactively or inside scripts/pipelines  
• Output formats: JSON, text, table  
• Supports pagination, filters, and advanced querying via `--query`  
• Integrates well with automation frameworks (bash, PowerShell, CI/CD)

---

## Core Concepts & Syntax

• Installation & configuration:  
  `aws configure` — set access key, secret key, region, output  
  `aws configure --profile myprofile` — create named profile  

• Profiles:  
  Use `--profile <name>` to switch credentials  

• Region override:  
  `--region us-west-2` per command  

• Output formats:  
  `--output json|text|table`  

---

## Security / Governance & Cost Considerations

• Credentials must be stored securely — avoid embedding keys in scripts  
• Prefer IAM Roles, environment variables, or named profiles  
• Actions executed via CLI appear in CloudTrail for auditing  
• Be careful with region/account context to avoid accidental resource creation  
• Automated scripts can generate unintended costs if cleanup isn't handled  

---

## Use Cases

• Automating S3 bucket creation, IAM roles, deployments  
• Multi-region EC2 cleanup or reporting scripts  
• Querying multiple profiles/accounts for resource states  
• Integrating AWS commands into Jenkins, GitHub Actions, GitLab CI pipelines  

---

## Best Practices

• Use named profiles for dev/test/prod environments  
• Keep credentials in `~/.aws/config` and `~/.aws/credentials` — never commit them  
• Use `--dry-run` whenever available  
• Combine CLI automation with CloudFormation or CDK for full IaC workflows  
• Add logging, retries, and cleanup logic in automation scripts  
• Use table output for human readability and JSON for parsing  
• Update the CLI regularly (`aws --version`) to access new features  

---

## Exam Tips

• For questions about automation, scripting, or repeatable operations → choose AWS CLI  
• If scenario mentions “run commands from terminal” → CLI  
• CLI actions require IAM permissions and correct region/profile  
• CLI is not a service — it is the interface to AWS services  
• Good for retrieving resource details, automating tasks, and running DevOps pipelines  

---

## Quick Summary

AWS CLI is the command-line interface for interacting with AWS services in an automated, scriptable, and repeatable way. Ideal for DevOps workflows, CI/CD, multi-account automation, and managing AWS resources without using the console.

