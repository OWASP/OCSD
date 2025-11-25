
02. Authentication and Credential Management

2.1 What is Authentication?
- The process of verifying an identity
- Attributes used for verifying an identity
- Various authentication methods

2.2 Entities that need authentication
- Devices
- Applications
- Humans
- Services
- Docker images
- Containers

2.3 Credential Lifecycle Management
- Credential Provisioning:**  
- Credential Rotation:**  
- Credential Revocation:**  
- Secure Credential Recovery:**  

# Secure Password Storage

**Never** store passwords in plaintext. All passwords must be stored as one-way cryptographic hashes.
Use a strong, modern password hashing algorithm. Prefer algorithms specifically designed for password hashing, such as **Argon2**, **scrypt**, or **bcrypt**.
Avoid outdated or weak hashing algorithms. Do **not** use generic hash functions like MD5 or SHA-256 for password storage, as they are too fast and susceptible to brute-force attacks.
Salt every password with a unique, random salt. A salt is a random string added to a password before hashing. A unique salt for each user prevents attackers from using pre-computed rainbow tables and increases security.
Adjust the cost factor of the hashing algorithm. Password hashing algorithms are designed to be computationally expensive. The cost factor should be increased over time as computing power improves.

---

# Multi-Factor Authentication (MFA)

Implement MFA for all users, especially for privileged accounts. MFA requires users to provide two or more verification factors, such as:

**Something you know:** a password
**Something you have:** a phone or hardware token
**Something you are:** biometrics like a fingerprint

Prioritize strong MFA methods:

**Hardware security tokens (FIDO2/WebAuthn):** Gold standard, resistant to phishing.
**Authenticator apps using Time-based One-Time Passwords (TOTP):** Secure and widely adopted method.
**Push notifications from a trusted app:** More user-friendly and secure than SMS.

Use SMS-based MFA with caution. While better than no MFA, SMS can be vulnerable to SIM swapping attacks. Use it as a last resort or a temporary fallback.

Securely implement the MFA enrollment and recovery processes. MFA recovery should be as secure as initial authentication to prevent account takeovers.

---

# Credential Lifecycle Management



---

# Federation and Single Sign-On (SSO)

Understand the difference between authentication and authorization. Authentication is verifying a user's identity. Authorization is determining what that user is allowed to do.

**OAuth 2.0** is an authorization framework. It allows an application to get limited access to a user's account on another service without knowing their password.
**OpenID Connect (OIDC)** is an authentication layer built on top of OAuth 2.0. It is used to verify the user's identity and obtain basic profile information.
**SAML (Security Assertion Markup Language)** is another standard for authentication and authorization, often used for enterprise SSO solutions.

When implementing these protocols, always use a well-vetted, official library. Do not try to implement these complex protocols from scratch.

Validate tokens and assertions. Always verify the digital signature, issuer, audience, and expiration of tokens (e.g., JSON Web Tokens) to ensure they are legitimate.
Use the `state` parameter. This parameter should be used to protect against Cross-Site Request Forgery (CSRF) attacks when redirecting users.
