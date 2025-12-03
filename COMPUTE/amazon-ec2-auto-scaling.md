# AWS EC2 Auto Scaling

AWS Auto Scaling is a fully managed service that automatically adjusts capacity to maintain performance and minimize costs.  
It can scale EC2 instances, ECS tasks, DynamoDB throughput, Aurora Replicas, and Spot Fleets, supporting both vertical and horizontal scaling.

---

## What It Is

• Automatically scales resources based on demand  
• Helps improve application availability and reduce costs  
• Works with EC2 Auto Scaling, ECS, DynamoDB, Aurora, Spot Fleets  
• Unified scaling plans for multiple resources  
• Predictive scaling using machine learning  

---

## Components of EC2 Auto Scaling

1. Launch Template or Launch Configuration  
– Specifies AMI, instance type, key pair, security groups  
– Launch Template is recommended  

2. Auto Scaling Group (ASG)  
– Logical group of EC2 instances  
– Defines min, max, and desired capacity  
– Can span multiple AZs  
– Automatically replaces unhealthy instances  

3. Scaling Policies  
– **Dynamic Scaling:**  
  • Target Tracking — maintain metric at target  
  • Step Scaling — adjust in steps  
  • Simple Scaling — triggered by CloudWatch alarm  
– **Predictive Scaling:**  
  Forecasts traffic and scales proactively  
– **Scheduled Scaling:**  
  Scales at fixed times  

---

## Health Checks

• Performed via EC2 and optional ELB  
• Unhealthy instances are replaced automatically  
• Grace period allows warm-up time  

---

## Elastic Load Balancer Integration

• ASG registers/deregisters with ELB automatically  
• Traffic only routed to healthy instances  
• Supports ALB, NLB, and Classic Load Balancer  

---

## Lifecycle Hooks

• Pause launch/terminate actions for custom logic  
• Supports bootstrapping, logging, cleanup tasks  

---

## Monitoring and Alarms

• Uses CloudWatch metrics and alarms  
• Key metrics include CPUUtilization, NetworkIn, NetworkOut  
• Scaling actions triggered by alarms  

---

## Instance Refresh

• Replace instances with updated configuration  
• Enables patching without downtime  

---

## Warm Pools

• Pre-initialize EC2 instances in stopped state  
• Reduces scale-out time  

---

## Pricing

• Auto Scaling has no cost  
• Pay only for EC2, ELB, and other resources used  

---

## Use Cases

• Unpredictable or spiky traffic  
• High availability and fault tolerance  
• Automated scaling workflows  
• Cost reduction during low demand  

---

## Exam Tips

• Use Target Tracking scaling for consistent performance  
• Predictive Scaling for known traffic patterns  
• Health checks maintain availability  
• Launch Templates preferred over Launch Configurations  
• Lifecycle Hooks for custom automation  
• Warm Pools help reduce response time  
• ASG spans multiple AZs, not multiple regions  
• ELB + ASG improves HA and traffic distribution  
• Instance Refresh for rolling updates  

---

## Quick Summary

AWS Auto Scaling maintains performance and cost efficiency by adjusting capacity based on real-time metrics or forecasts.  
It integrates with EC2, ELB, CloudWatch, and more to create scalable, fault-tolerant, highly available systems.  
Understanding scaling policies, lifecycle hooks, launch templates, and monitoring is essential for architecting resilient workloads.

