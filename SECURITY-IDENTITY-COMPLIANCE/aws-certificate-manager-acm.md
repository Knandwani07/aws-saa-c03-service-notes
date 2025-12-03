# AWS Certificate Manager (ACM)

---

## What It Is
AWS Certificate Manager (ACM) is a fully managed service that **provisions, manages, and deploys SSL/TLS certificates** for securing websites, APIs, and applications on AWS. It handles certificate lifecycle tasks such as renewal and deployment automatically.

---

## Key Features

### 1. Free Public Certificates
• Request free public SSL/TLS certificates for:  
  – Elastic Load Balancers (ALB/CLB/NLB)  
  – Amazon CloudFront  
  – Amazon API Gateway  
• Certificates are **auto-renewed** and managed by AWS.  
• Cannot export private keys for public ACM certificates.

### 2. Private Certificates (ACM PCA)
• Managed private Certificate Authority (CA).  
• Issue private certificates for internal services, devices, zero-trust architectures.  
• Paid service with granular issuance controls.

### 3. Automatic Renewal
• ACM automatically renews certificates and deploys them to integrated AWS resources.  
• Prevents downtime caused by expired certificates.

### 4. Integration with AWS Services
• Works seamlessly with:  
  – CloudFront  
  – Elastic Load Balancers  
  – API Gateway  
  – Elastic Beanstalk  
  – AWS CloudFormation  
• Simple, one-click certificate association with supported services.

### 5. Secure Key Management
• ACM manages private keys securely.  
• Private keys for public certificates cannot be downloaded or exported.  
• Supports RSA 2048-bit and ECDSA certificates.

---

## Validation Methods

### 1. DNS Validation (Recommended)
• Add a CNAME record to verify domain ownership.  
• Best for automation and seamless renewals.

### 2. Email Validation
• Verification sent to domain WHOIS contacts.  
• More manual and prone to missed renewals.

---

## Use Cases
• Securing HTTPS on web apps and APIs.  
• Custom domains on CloudFront, ALB, and API Gateway.  
• Automatic certificate lifecycle management.  
• Internal TLS certificates using ACM Private CA.  

---

## Pricing
• **Public certificates** → Free  
• **ACM Private CA (PCA)** → Charges for CA usage + certificate issuance  

---

## Security & Compliance
• Certificates encrypted at rest and in transit.  
• AWS manages private keys securely (HSM-backed).  
• Supports FIPS-compliant algorithms and ECDSA.  
• CloudTrail logs certificate actions for auditing.

---

## Exam Tips
• ACM = SSL/TLS certificate provisioning + management.  
• Public certs are free but usable **only with AWS-integrated services**.  
• For internal certs → use ACM Private CA.  
• DNS validation is recommended for automation.  
• CloudFront custom domain requires ACM certificate in **us-east-1**.  
• Private key for public ACM certificates cannot be exported.  

---

## Quick Summary
AWS Certificate Manager provides free public SSL/TLS certificates and a scalable private certificate authority service, with automatic provisioning, renewal, and secure key management. It’s the simplest way to enable HTTPS for AWS applications while minimizing operational overhead.

