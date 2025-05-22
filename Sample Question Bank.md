Question 1: What is the most effective way to prevent SQL Injection attacks?
A. Use string concatenation with input validation
 B. Store queries in environment variables
 C. Sanitize outputs using HTML encoding
 D. Use parameterized (prepared) statements
 E. Limit input length to 255 characters
 F. Encrypt all user inputs
✅ Correct Answer: D
—
Question 2: Which of the following best mitigates Cross-Site Scripting (XSS) attacks?
A. Escaping output in the HTML context
 B. Using HTTPS instead of HTTP
 C. Restricting access with a firewall
 D. Setting up rate limiting
 E. Validating passwords on the client side
 F. Running antivirus software on the server
✅ Correct Answer: A
—
Question 3: What is CSRF (Cross-Site Request Forgery)?
A. An attack where SQL commands are injected into queries
 B. An attack where scripts are injected into web pages
 C. An attack where a user is tricked into submitting a request unknowingly
 D. An attack that installs ransomware via cookies
 E. A misconfiguration in the firewall rules
 F. A server-side directory traversal exploit
✅ Correct Answer: C
—
Question 4: Which of the following is a good practice for storing user passwords securely?
A. Storing them in plaintext in a secure database
 B. Encrypting them with AES and storing the key in code
 C. Hashing them using SHA1
 D. Hashing them using bcrypt with a salt
 E. Using Base64 encoding
 F. Encrypting them with SSL certificates
✅ Correct Answer: D
—
Question 5: Which HTTP response header is used to prevent the browser from loading a site over HTTP?
A. X-Frame-Options
 B. Content-Security-Policy
 C. Referrer-Policy
 D. Strict-Transport-Security
 E. Access-Control-Allow-Origin
 F. Cache-Control
✅ Correct Answer: D
—
Question 6: Which of the following is a secure way to handle API secrets?
A. Hardcoding them into source code
 B. Saving them in JavaScript files served to the browser
 C. Storing them in a version-controlled .env file
 D. Storing them in a secrets manager like AWS Secrets Manager
 E. Emailing them to developers
 F. Putting them in cookies with HTTPOnly disabled
✅ Correct Answer: D
—
Question 7: What is the purpose of Content Security Policy (CSP)?
A. To encrypt API data in transit
 B. To block access to the website from foreign IPs
 C. To define which content sources are allowed to load
 D. To enforce password complexity
 E. To set cookie expiration times
 F. To protect against SQL injection
✅ Correct Answer: C
—
Question 8: Which technique helps prevent session hijacking?
A. Using JavaScript to store sessions in localStorage
 B. Setting session cookies with the Secure and HttpOnly flags
 C. Disabling all cookies
 D. Using GET parameters for session IDs
 E. Enabling CORS on all endpoints
 F. Allowing unlimited login attempts
✅ Correct Answer: B
—
Question 9: What is the best way to ensure third-party packages don’t introduce security risks?
A. Only install from well-known vendors
 B. Manually inspect the code of all dependencies
 C. Use automated tools like npm audit
 D. Avoid open-source software
 E. Enable all browser security headers
 F. Use static IP allowlists
✅ Correct Answer: C
—
Question 10: What does the principle of least privilege mean?
A. Give all users admin access by default
 B. Deny all access by default and manually whitelist actions
 C. Grant only the minimum access rights necessary for users to do their job
 D. Use default credentials for testing
 E. Allow users to escalate privileges if needed
 F. Encrypt user passwords using base64
✅ Correct Answer: C
—
Question 11: Which of these is a sign of broken authentication?
A. Using a JSON Web Token
 B. Limiting login attempts
 C. Hardcoded admin credentials
 D. Using MFA
 E. Applying rate limiting
 F. Hashing passwords with bcrypt
✅ Correct Answer: C
—
Question 12: What is the role of a JWT (JSON Web Token) in web applications?
A. Encrypting all user data
 B. Logging user activity
 C. Signing and transmitting claims between parties securely
 D. Performing SQL queries
 E. Preventing DDoS attacks
 F. Compressing large images
✅ Correct Answer: C
—
Question 13: Why is HTTPS important for all pages, not just login pages?
A. It improves search engine rankings
 B. It reduces the server load
 C. It prevents passive eavesdropping on sensitive data
 D. It allows cookies to work
 E. It bypasses the firewall
 F. It blocks SQL injection
✅ Correct Answer: C
—
Question 14: What is a static application security testing (SAST) tool used for?
A. Monitoring traffic between client and server
 B. Analyzing code for vulnerabilities before execution
 C. Preventing XSS at runtime
 D. Managing firewall rules
 E. Enforcing role-based access controls
 F. Automating login flows
✅ Correct Answer: B
—
Question 15: Which of the following would best help detect suspicious user behavior?
A. Enforcing password rotation every week
 B. Configuring HTTPS
 C. Logging and monitoring application activity
 D. Running npm audit on frontend code
 E. Blocking all cookies
 F. Using SHA-1 for password hashing
✅ Correct Answer: C
