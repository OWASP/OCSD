# Authorisation 

## Concepts and Best Practices 

### Session timeout and renewal

The following two mechanisms ensure confidentiality, integrity, and availability of authenticated sessions.
1. **Session timeout:** The period of inactivity after which a user’s session is automatically terminated or requires re-authentication.
2. **Session renewal (or rotation):**  The act of issuing a new session identifier (token) to reduce the risk of session fixation or theft.


Best practices for session timeout include the following. 
* Use reasonable inactivity timeouts.
* Require re-authentication after max session lifetime.
* Provide clear user feedback.
* Terminate sessions server-side.

Best practices for session renewal (rotation) include the following. 
* Rotate session IDs after authentication.
* Periodically rotate long-lived tokens.
* Immediately invalidate old tokens.


### Cookie attributes: Secure, HttpOnly, SameSite


The following cookie attributes play an important role in secure software development.

* **Secure:**  This cookie attribute ensures that the cookie is only sent over encrypted HTTPS connections and protects the confidentiality and integrity of cookie data during transmission. Without this flag, cookies could be transmitted over unencrypted HTTP, allowing attackers on the same network to intercept or steal session cookies through man-in-the-middle (MITM) attacks.
* **HttpOnly:**  Prevents client-side scripts (e.g., JavaScript) from accessing the cookie.  If an attacker injects malicious JavaScript into your web page (via XSS), they could read cookies and hijack sessions. Marking cookies as `HttpOnly` ensures they can only be sent in HTTP requests, not accessed through `document.cookie`.  This helps to mitigate cross-site scripting (XSS)–based session theft.
* **SameSite:**  Restricts when cookies are sent with cross-site requests, helping prevent cross-site request forgery (CSRF) and some forms of cross-site tracking.  This protects against CSRF attacks by ensuring cookies aren’t automatically sent with cross-origin requests unless explicitly allowed.
  

### Token vs. cookie-based sessions

In web security, token-based and cookie-based sessions are two different approaches to managing user authentication and maintaining session state. Both aim to verify that a user remains authenticated as they navigate a site or API—but they differ in how they store and transmit that authentication data.
Below is a detailed breakdown of their differences:

* Where session data is stored
* Authentication flow
* Statelessness and scalability


### Logout and re-authentication

Logout security best practices include the following.
* Invalidating session tokens
* Removing authentication artifacts
* Server-side session expiry
* Redirecting to a safe page after logout
* Clearing browser cache

Re-authentication security best practices include the following.

* Requiring re-authentication for sensitive actions
* Using session age checks
* Multi-factor authentication (MFA) aware re-authentication
* Not storing passwords in a session
* Including visual indicators for authentication status

### Fixation and hijacking defenses

A session fixation attack is when an attacker tricks a user into authenticating with a session ID or token the attacker already knows (e.g., via a crafted URL, cookie injection, or hidden form). Once the victim logs in, the attacker uses the same session ID to impersonate them.

Developers can implement the following defenses against fixation attacks.
* Regenerate session IDs after login
* Avoid session IDs in URLs
* Invalidate old sessions

A session hijacking attack is when an attacker steals a valid user’s session token (e.g., via XSS, sniffing, CSRF, or session replay) and uses it to impersonate that user.

Developers can implement the following defenses against hijacking attacks.
* Use HTTPS everywhere
* Use strong session token entropy
* Implement short-lived and rotating tokens
* Bind sessions to client context
* Detect and revoke stolen sessions
* Implement CSRF protection
* Defend against XSS


### RBAC vs. ABAC

Roll-based access control (RBAC) and attribute-based access control (ABAC) are two different styles of access control policies.  

With RBAC, users of a system are assigned roles, and each role has a defined set of permissions. Access decisions are based on what role the user holds.  For example, in an electronic medical record (EMR) platform, a user with the `Nurse` role can view patient charts, and a `Doctor` role can view and update patient charts.

With ABAC, decisions are based on attributes, which can come from the user, resource, action, or environment.  For example, an ABAC policy might allow only employees in the Medical Department with clearance >= 3 to update patient charts while inside the hospital network. Attributes may fall under any of the following categories. 
* User attributes, such as job title, clearance level or department
* Resource attributes like document classification or owner
* Environment attributes, such as time of day, location or device trust level
* Action attributes like including read, write or approve


### Object-level authorisation

Object-Level Authorisation (OLA) is a fine-grained access control mechanism that ensures a user can only access or modify specific objects (records, files, or resources) they are permitted to.

It goes beyond checking whether a user is authenticated or has a general role, such as `Admin` or `User`.
Instead, it checks whether the user owns or has permission for the specific resource they’re trying to access.

Consider the following example.

1. A user with ID 123 requests `/api/orders/456`.

2. The application must check if order 456 belongs to user 123.

3. Even if the user is authenticated, they should not see or modify someone else’s order.

If this check is missing, it’s known as an Insecure Direct Object Reference (IDOR) — a common OWASP Top 10 vulnerability.

A developer can follow the following steps to enforce OLA.

1. **Authenticate the user:** Identify who is making the request (via session, token, etc.)
2. Extract the object identifier, such as the order ID, document ID, or record ID.
3. **Check object ownership or permissions:** Confirm the user has rights to that specific object.
4. **Enforce least privilege:** Users can only access what they truly need.

### Security of authorisation tokens (e.g. JWT)

Authorization tokens, such as JSON Web Tokens (JWTs), are widely used in modern web applications to authenticate and authorize users. Their security depends on how they are generated, signed, transmitted, and stored.


### Horizontal vs. vertical privilege escalation

Horizontal privilege escalation occurs when a user accesses resources of another user at the same privilege level.  It may result inser data exposure, impersonation, or data manipulation.

Prevention techniques for horizontal privilege escalation include the following.
1. Implementing object-level authorization (validating that the authenticated user owns or has rights to the resource)
2. Using indirect references, replacing predictable IDs with opaque identifiers (UUIDs, tokens)
3. Avoiding client-controlled identifiers
4. Regularly testing authorization logic

Vertical privilege escalation occurs when a low-privileged user gains higher-level privileges — for example, a normal user performing admin-only actions.  It may allow an attacker to modify or control the system (e.g., delete data, change permissions, access admin panels).

Prevention techniques for vertical privilege escalation include the following.
1. Enforcing role-based or attribute-based access control (RBAC/ABAC)
2. Applying the principle of least privilege (assigning only the permissions necessary for each role)
3. Secure backend enforcement (never relying on front-end checks alone (like hiding admin buttons in the UI)
4. Auditing and logging privileged actions (tracking when admin endpoints are accessed to detect misuse)


### Effective testing of access control 


The following are some best practices for software developers to effectively test access control, ensuring that permissions, authentication, and authorization mechanisms are correctly implemented and enforced.
1. Test all access control levels.
2. Use multiple user roles for testing.
3. Perform both positive and negative testing.
4. Test object-level authorization.
5. Automate access control tests.
6. Test for common access control vulnerabilities.
7. Enforce server-side authorization checks.
8. Include session and token tests.
9. Test multi-tenant and contextual scenarios.
10. Use security testing tools and frameworks.
11. Conduct peer review and penetration testing.
12. Trace and log authorization decisions.

## References

1. [OWASP Authorization Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html)

2. [NIST Computer Security Resource Center glossary](https://csrc.nist.gov/glossary/term/authorization)

3. [CWE-285: Improper Authorization - MITRE Common Weakness Enumeration](https://cwe.mitre.org/data/definitions/285.html)

4. [C1: Implement Access Control - OWASP Top 10 Proactive Controls](https://top10proactive.owasp.org/the-top-10/c1-accesscontrol/#6-do-not-hard-code-roles)
