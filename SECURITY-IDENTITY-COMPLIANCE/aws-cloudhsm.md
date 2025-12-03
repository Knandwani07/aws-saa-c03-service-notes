# AWS CloudHSM

---

## What It Is
AWS CloudHSM is a **managed Hardware Security Module (HSM)** service that provides **dedicated, single-tenant cryptographic hardware** inside your VPC. Unlike AWS KMS, CloudHSM gives **full customer control** over keys and operations and meets the **strictest compliance needs** (FIPS 140-2 Level 3).

---

## Key Features
• Dedicated, single-tenant HSM appliances inside your VPC  
• Fully customer-controlled key creation, storage, and usage  
• FIPS 140-2 Level 3 validated hardware  
• Supports industry-standard cryptographic APIs (PKCS#11, Java JCE, Microsoft CNG)  
• Horizontally scalable clusters—you add HSMs for performance and HA  
• Automated backups for durability  
• Integrated with some AWS services (less seamless than KMS)  

---

## How It Works
• AWS deploys the HSM appliance inside your VPC  
• You manage:  
  – HSM users  
  – Cryptographic keys  
  – Access policies  
• You connect via standard HSM libraries and clients  
• AWS handles hardware health, backups, and patching—but **AWS never has access to your keys**  

---

## Use Cases
• Workloads requiring **FIPS 140-2 Level 3** compliance  
• Regulatory environments demanding **exclusive, customer-owned key control**  
• Building and managing a **PKI**  
• Secure key generation and long-term key storage  
• Offloading SSL/TLS termination  
• Code-signing operations  

---

## Differences from AWS KMS
| AWS KMS | AWS CloudHSM |
|--------|--------------|
| AWS-managed | Customer-managed |
| Shared hardware (multi-tenant) | Dedicated HSMs |
| Easiest to use, deeply integrated | Full control, more complex |
| FIPS 140-2 Level 2 | FIPS 140-2 Level 3 |
| Cannot export or manage keys directly | Full key export/import control |

CloudHSM is chosen when **full, exclusive control and compliance** are required.

---

## Pricing
• Charged **per HSM instance per hour**  
• Additional data transfer charges may apply  
• No upfront fees  

---

## Security & Compliance
• FIPS 140-2 Level 3 certified hardware  
• Keys never leave the HSM in plaintext  
• AWS cannot access, recover, or see your keys  
• Customer-controlled authentication and access  
• Encryption operations always remain inside the HSM  

---

## Exam Tips
• CloudHSM = **dedicated HSM with full key control**  
• Used for: PKI, code signing, SSL/TLS offloading, regulatory compliance  
• Compare with KMS: KMS is managed/easy; CloudHSM is controlled/strict  
• FIPS 140-2 Level 3 → key phrase for exam questions  
• Keys generated in CloudHSM stay entirely under customer ownership  
• CloudHSM clusters scale horizontally  

---

## Quick Summary
AWS CloudHSM is a **dedicated, fully managed HSM appliance** inside your VPC that gives you complete control over your cryptographic keys and operations. It meets the highest compliance requirements (FIPS 140-2 Level 3) and is ideal for PKI, sensitive encryption workloads, and regulated industries needing hardware isolation and customer-exclusive control.

