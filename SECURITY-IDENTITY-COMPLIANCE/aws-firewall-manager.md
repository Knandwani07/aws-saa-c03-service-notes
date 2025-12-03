# AWS Firewall Manager

---

## What It Is
AWS Firewall Manager is a centralized security management service that lets you create and enforce firewall policies across multiple AWS accounts and resources. It is designed to work with AWS Organizations to ensure consistent, organization-wide protection.

---

## Key Features

### 1. Centralized Security Policy Management
• Create security policies once and apply them across accounts and resources  
• Manage all member accounts from a central admin account  
• Enforce organization-wide rules for consistent security posture  

### 2. Supported Security Services
• **AWS WAF** – Deploy and manage Web ACLs across accounts  
• **AWS Shield Advanced** – Apply advanced DDoS protection globally  
• **AWS Network Firewall** – Manage VPC-level traffic filtering  
• **VPC Security Groups** – Audit and auto-remediate misconfigured SGs  
• **Route 53 Resolver DNS Firewall** – Enforce DNS filtering policies  

### 3. Automatic Policy Enforcement
• Automatically applies required policies to new resources (ALBs, CloudFront, VPCs, etc.)  
• Ensures new accounts/resources remain compliant without manual updates  

### 4. Compliance Monitoring
• Continuously checks accounts for policy compliance  
• Flags noncompliant resources  
• Optionally auto-remediates issues to restore compliance  

### 5. Integration with AWS Organizations
• Requires AWS Organizations to function  
• Policies can target:  
  – Entire Organization  
  – Organizational Units (OUs)  
  – Specific AWS accounts  

---

## Use Cases
• Enforcing consistent WAF rules across all web applications  
• Auto-applying Shield Advanced for DDoS protection on new resources  
• Centralizing Network Firewall rule management for all VPCs  
• Detecting and fixing overly permissive or misconfigured security groups  
• Applying DNS Firewall rules to block malicious domains organization-wide  

---

## Security & Compliance
• Helps enforce enterprise security baselines  
• Reduces configuration drift and misconfigurations  
• Improves visibility into security posture across all accounts  

---

## Pricing
Charges depend on:  
• Number of AWS Firewall Manager policies  
• Usage of underlying services:  
  – AWS WAF  
  – AWS Shield Advanced  
  – AWS Network Firewall  
  – DNS Firewall  
• Additional costs for rules, protections, and network processing handled by underlying services  

---

## Exam Tips
• Firewall Manager = centralized multi-account security policy enforcement  
• Requires **AWS Organizations** (mandatory)  
• Supports: WAF, Shield Advanced, Network Firewall, Security Groups, DNS Firewall  
• Automatically protects new resources as they are created  
• Provides compliance checks + optional automated remediation  
• Best for multi-account enterprise setups  

---

## Quick Summary
AWS Firewall Manager provides centralized creation, deployment, and enforcement of security policies across all AWS accounts in an organization. It integrates with services like WAF, Shield Advanced, Network Firewall, Security Groups, and DNS Firewall to ensure consistent, automated security at scale.

