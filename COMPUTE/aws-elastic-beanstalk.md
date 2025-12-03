# AWS Elastic Beanstalk

AWS Elastic Beanstalk is a fully managed service that simplifies deploying, running, and scaling web applications.  
It provisions infrastructure automatically (EC2, Auto Scaling, ELB) while still allowing full control when needed.

---

## What It Is

• Simplifies application deployment without managing servers  
• Automatically handles provisioning, load balancing, scaling, and health checks  
• Supports multiple programming languages and frameworks  
• Integrates with Git, Jenkins, IDEs  
• Customizable using configuration files and extensions  
• Provides full control over underlying AWS resources  
• Supports rolling, immutable, and blue/green deployments  

---

## Deployment Options

• All at Once — deploy to all instances simultaneously  
• Rolling — deploy in batches  
• Rolling with Additional Batch — adds new capacity before replacing old  
• Immutable — deploys to new instances first, then shifts traffic  
• Blue/Green — create new environment, test, and swap CNAME  

---

## Supported Platforms

• Java (Tomcat)  
• .NET (Windows IIS)  
• PHP  
• Python  
• Ruby  
• Go  
• Node.js  
• Docker (single and multi-container)  
• Custom platforms using Packer  

---

## Architecture and Components

• Application — logical collection of environments, versions, configs  
• Application Version — specific deployable version  
• Environment — AWS resources running the version  
• Environment Tier — web server or worker  
• Configuration Template — predefined environment settings  
• Configuration stored in `.ebextensions`  

---

## Environment Tiers

• Web Server Tier — handles HTTP/S traffic using Apache or Nginx  
• Worker Tier — processes background tasks via SQS  

---

## Customizations and Extensions

• `.ebextensions` YAML files to customize EC2 instances  
• Install software packages, add cron jobs, configure logs  
• Change instance types, modify resources  
• Supports embedded CloudFormation for advanced setup  

---

## Monitoring and Logging

• Real-time health monitoring  
• Integrated with CloudWatch metrics and ELB health checks  
• Logs viewable in console or stored in S3  
• SNS notifications for alerts  

---

## Scaling

• Integrated with Auto Scaling  
• Configurable min, max, desired capacity  
• Load balancing using ELB for HA  

---

## Security

• IAM roles for EC2 instances  
• VPC support for private networking  
• SSL termination at ELB  
• Environment variables encryptable with KMS  

---

## Application Lifecycle

• Upload application version  
• Deploy version to an environment  
• Monitor and update  
• Terminate environment when done  

---

## Pricing

• No cost for Elastic Beanstalk  
• Pay only for EC2, ELB, S3, and other underlying resources  

---

## Use Cases

• Web application hosting with minimal ops  
• Rapid deployment and iteration  
• Scalable environments for microservices  
• CI/CD pipelines in DevOps workflows  

---

## Best Practices

• Prefer immutable or blue/green deployments  
• Store `.ebextensions` in version control  
• Monitor health metrics and logs frequently  
• Clone environments for safe testing  
• Enable managed platform updates  

---

## Exam Tips

• Beanstalk provisions EC2, Auto Scaling, ELB, RDS automatically  
• Supports rolling, immutable, blue/green deployments  
• Still gives full access to underlying EC2 instances  
• Configuration handled via console and `.ebextensions`  
• Blue/green ensures zero-downtime updates  

---

## Quick Summary

AWS Elastic Beanstalk automates deployment and infrastructure management for web applications while still giving full control when needed.  
It supports many languages, multiple deployment strategies, scaling, monitoring, and deep customization—making it ideal for rapid, reliable application delivery.

