# Amazon Cognito

---

## What It Is
Amazon Cognito is a fully managed identity service that provides **authentication, authorization, and user management** for your web and mobile applications. It supports sign-up, sign-in, MFA, federated identities, and secure access to AWS resources — all at scale.

---

## Key Features
• User sign-up and sign-in with customizable/hosted UI  
• User Pools for managing users and authentication  
• Identity Pools (Federated Identities) for providing temporary AWS credentials  
• Social login support (Google, Facebook, Apple, Amazon)  
• Enterprise login via **SAML 2.0** and **OIDC**  
• Secure JWT token issuance (ID, Access, Refresh tokens)  
• MFA, adaptive authentication, device tracking  
• Deep integration with IAM and AWS services  
• Lambda triggers for custom authentication workflows  

---

## User Pools
• Fully managed **user directory** for registration + authentication  
• Supports email/phone verification  
• Built-in MFA using SMS or TOTP  
• Password policies + account recovery  
• Hosted UI for sign-up/sign-in  
• Integrates with social identity providers and SAML/OIDC  
• Issues JWT tokens: **ID Token**, **Access Token**, **Refresh Token**  
• OAuth2 flows (Authorization Code, Implicit)  
• Lambda triggers: Pre-sign-up, Pre-auth, Post-confirmation, Custom challenge, etc.  

---

## Identity Pools (Federated Identities)
• Provide **temporary AWS IAM credentials** using AWS STS  
• Works with Cognito User Pools + social providers + SAML/OIDC  
• Supports **unauthenticated guest access**  
• IAM role mapping based on identity provider or user attributes  
• Enables secure access to AWS services from client apps (S3, DynamoDB, etc.)  

---

## Authentication Flows
• User Pools handle authentication → return JWT tokens  
• Identity Pools exchange those tokens for AWS credentials  
• Supports custom authentication challenges via Lambda  
• OAuth2-compatible authentication methods  
• Secure session/token management  

---

## Security Features
• MFA (SMS / TOTP)  
• Adaptive risk-based authentication  
• Compromised credential detection (advanced security)  
• Encryption at rest & in transit  
• KMS-backed key protection  
• Device tracking and remembered devices  
• Account recovery workflows  

---

## Integration with AWS Services
• **API Gateway** – Cognito Authorizer for securing REST/WebSocket APIs  
• **AppSync** – Authenticate GraphQL APIs  
• **IAM** – Role-based permission control  
• **Lambda** – Invoke with user identity context  
• **S3** – Per-user or per-group file access  
• SDKs for Android, iOS, React, JavaScript, etc.  

---

## Tokens and Sessions
• **ID Token** – User profile info  
• **Access Token** – Authorization for API calls  
• **Refresh Token** – Retrieve new tokens without re-authentication  
• Configurable expiration settings  

---

## Deployment & Management
• Region-specific User Pools and Identity Pools  
• Scalability managed automatically  
• CloudWatch metrics for monitoring  
• Dedicated console for managing users and identities  

---

## Pricing
• **User Pools**: Pay by Monthly Active Users (MAUs)  
• Free tier: **50,000 MAUs/month**  
• **Identity Pools**: Pay for AWS STS calls + data transfer  
• Advanced security features are billed separately  

---

## Use Cases
• Add authentication to mobile/web apps  
• Federated login with enterprise/SAML providers  
• Provide AWS resource access to authenticated users  
• Serverless backend authentication (API Gateway + Lambda)  
• Implement MFA and adaptive security  
• Build secure app experiences with minimal custom backend code  

---

## Best Practices
• Enable MFA for user accounts  
• Use a **custom domain** for OAuth flows  
• Store minimal sensitive data in user attributes  
• Follow least privilege when assigning IAM roles  
• Secure Lambda triggers with IAM permissions  
• Monitor login metrics + anomalies in CloudWatch  
• Rotate keys and enforce password policies  

---

## Exam Tips
• **User Pools = authentication** (directory + JWT tokens)  
• **Identity Pools = authorization to AWS resources** (temporary credentials)  
• Supports federated identities (SAML, OIDC, social providers)  
• Cognito Authorizer integrates tightly with API Gateway  
• MFA + adaptive authentication built-in  
• Issues ID, Access, and Refresh tokens  
• Identity Pools map users → IAM roles  
• Differentiates between authentication vs authorization flows  

---

## Quick Summary
Amazon Cognito offers secure, scalable user authentication and authorization for apps. **User Pools** manage user identities and authentication, while **Identity Pools** provide temporary AWS credentials for accessing AWS services. With support for social login, SAML, MFA, adaptive security, and tight AWS integration, Cognito provides a complete, managed identity solution.

