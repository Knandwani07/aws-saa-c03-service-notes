# AWS Cost Management

AWS provides a suite of tools to track, estimate, forecast, optimize, and alert on your cloud spending.  
These tools give visibility, control, budgeting, and optimization capabilities across your AWS environment.

---

## 1. AWS Pricing Calculator

• Helps estimate monthly AWS costs before deployment  
• Supports EC2, S3, RDS, and many other services  
• Useful for planning and cost comparisons  
• Results can be exported and shared  

---

## 2. AWS Free Tier

• Offers free usage of AWS services:  
– 12-month Free Tier (EC2, S3, RDS, etc.)  
– Always Free Tier (IAM, DynamoDB, Lambda – limited usage)  

• Helps users explore AWS at no cost  
• Free Tier usage tracked in Billing Dashboard  

---

## 3. AWS Billing and Cost Management Dashboard

• Central place to:  
– View and download billing and usage reports  
– Set budgets and alerts  
– Manage payment methods and invoices  
– Monitor Free Tier usage  
– Access Cost Explorer, CUR, and Budgets  

---

## 4. AWS Budgets

• Set spending/usage limits and send alerts when thresholds are crossed  
• Types of budgets:  
– Cost Budgets (monitor total spend)  
– Usage Budgets (track usage units)  
– RI / Savings Plans Budgets (coverage/utilization)  

• Supports notifications via SNS or AWS Chatbot  
• Can trigger automated actions (e.g., stop resources)  

---

## 5. AWS Cost Explorer

• Interactive tool to analyse past and current spend  
• Group/filter by service, region, account, tag, etc.  
• Forecast future costs  
• Visualize RI/Savings Plans use and coverage  
• Identify cost trends and inefficiencies  

---

## 6. AWS Cost and Usage Report (CUR)

• Most detailed billing dataset (CSV in S3)  
• Hourly and daily granularity  
• Query with Athena  
• Visualize in QuickSight  
• Load into Redshift for data warehousing  

---

## 7. Consolidated Billing (AWS Organizations)

• Combines charges for multiple accounts into one payer account  
• Benefits:  
– Volume discounts shared across accounts  
– Simplifies centralized cost control  
– Still retains per-account usage tracking  

---

## 8. Cost Allocation Tags

• Categorize/attribute costs by:  
– Project, team, environment, department  

• Types:  
– AWS-generated tags  
– User-defined tags  

• Must be activated in Billing Console  
• Required for cost allocation and chargeback  

---

## 9. Reserved Instances & Savings Plans

• Discount models for long-term workloads  

### Reserved Instances (RIs)
• Commit to specific instance type and region  
• Apply to EC2, RDS, ElastiCache, Redshift  

### Savings Plans
• More flexible pricing model  
• Commit to a dollar amount per hour  
• Apply to EC2, Lambda, Fargate  

---

## 10. AWS Trusted Advisor – Cost Optimization

• Identifies cost savings:  
– Idle/underutilized resources  
– Unassociated Elastic IPs  
– Low-traffic Load Balancers  

• Part of five categories of checks  
• Some checks require Business/Enterprise support plans  

---

## 11. AWS Compute Optimizer

• Uses ML to recommend optimal EC2 instance types  
• Based on historical usage  
• Helps reduce costs with rightsizing  

---

## 12. AWS Cost Anomaly Detection

• Uses machine learning to detect unexpected cost spikes  
• Sends alerts via:  
– Email  
– SNS  

• Can monitor by:  
– Linked accounts  
– Services  
– Linked account + service combination  

• Helps prevent budget surprises  

---

## Exam Tips

• Cost Explorer = visual breakdown, trend analysis, forecasting  
• AWS Budgets = threshold alerts (cost, usage, RI/SP)  
• CUR = detailed, granular billing data  
• Tags must be activated to appear in cost reports  
• Savings Plans = more flexible than RIs  
• Cost Anomaly Detection = ML-based spike detection  
• Consolidated Billing = centralized billing + volume discounts  
• Compute Optimizer + Trusted Advisor = optimization insights  

---

## Quick Summary

AWS Cost Management tools help estimate, monitor, control, and optimize cloud spending.  
Using tools like Pricing Calculator, Cost Explorer, CUR, Budgets, and Anomaly Detection, organizations gain financial visibility and cost efficiency across AWS workloads.
