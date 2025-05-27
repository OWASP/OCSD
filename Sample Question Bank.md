Question 1: What is the most effective way to prevent SQL Injection attacks?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Use string concatenation with input validation\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Store queries in environment variables\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Sanitize outputs using HTML encoding\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Use parameterized (prepared) statements\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Limit input length to 255 characters\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Encrypt all user inputs\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: D\
—\
Question 2: Which of the following best mitigates Cross-Site Scripting (XSS) attacks?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Escaping output in the HTML context\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Using HTTPS instead of HTTP\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Restricting access with a firewall\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Setting up rate limiting\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Validating passwords on the client side\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Running antivirus software on the server\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: A\
—\
Question 3: What is CSRF (Cross-Site Request Forgery)?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. An attack where SQL commands are injected into queries\
 &nbsp; &nbsp; &nbsp; &nbsp; B. An attack where scripts are injected into web pages\
 &nbsp; &nbsp; &nbsp; &nbsp; C. An attack where a user is tricked into submitting a request unknowingly\
 &nbsp; &nbsp; &nbsp; &nbsp; D. An attack that installs ransomware via cookies\
 &nbsp; &nbsp; &nbsp; &nbsp; E. A misconfiguration in the firewall rules\
 &nbsp; &nbsp; &nbsp; &nbsp; F. A server-side directory traversal exploit\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 4: Which of the following is a good practice for storing user passwords securely?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Storing them in plaintext in a secure database\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Encrypting them with AES and storing the key in code\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Hashing them using SHA1\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Hashing them using bcrypt with a salt\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Using Base64 encoding\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Encrypting them with SSL certificates\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: D\
—\
Question 5: Which HTTP response header is used to prevent the browser from loading a site over HTTP?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. X-Frame-Options\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Content-Security-Policy\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Referrer-Policy\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Strict-Transport-Security\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Access-Control-Allow-Origin\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Cache-Control\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: D\
—\
Question 6: Which of the following is a secure way to handle API secrets?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Hardcoding them into source code\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Saving them in JavaScript files served to the browser\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Storing them in a version-controlled .env file\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Storing them in a secrets manager like AWS Secrets Manager\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Emailing them to developers\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Putting them in cookies with HTTPOnly disabled\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: D\
—\
Question 7: What is the purpose of Content Security Policy (CSP)?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. To encrypt API data in transit\
 &nbsp; &nbsp; &nbsp; &nbsp; B. To block access to the website from foreign IPs\
 &nbsp; &nbsp; &nbsp; &nbsp; C. To define which content sources are allowed to load\
 &nbsp; &nbsp; &nbsp; &nbsp; D. To enforce password complexity\
 &nbsp; &nbsp; &nbsp; &nbsp; E. To set cookie expiration times\
 &nbsp; &nbsp; &nbsp; &nbsp; F. To protect against SQL injection\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 8: Which technique helps prevent session hijacking?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Using JavaScript to store sessions in localStorage\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Setting session cookies with the Secure and HttpOnly flags\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Disabling all cookies\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Using GET parameters for session IDs\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Enabling CORS on all endpoints\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Allowing unlimited login attempts\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: B\
—\
Question 9: What is the best way to ensure third-party packages don’t introduce security risks?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Only install from well-known vendors\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Manually inspect the code of all dependencies\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Use automated tools like npm audit\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Avoid open-source software\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Enable all browser security headers\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Use static IP allowlists\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 10: What does the principle of least privilege mean?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Give all users admin access by default\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Deny all access by default and manually whitelist actions\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Grant only the minimum access rights necessary for users to do their job\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Use default credentials for testing\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Allow users to escalate privileges if needed\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Encrypt user passwords using base64\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 11: Which of these is a sign of broken authentication?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Using a JSON Web Token\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Limiting login attempts\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Hardcoded admin credentials\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Using MFA\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Applying rate limiting\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Hashing passwords with bcrypt\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 12: What is the role of a JWT (JSON Web Token) in web applications?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Encrypting all user data\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Logging user activity\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Signing and transmitting claims between parties securely\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Performing SQL queries\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Preventing DDoS attacks\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Compressing large images\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 13: Why is HTTPS important for all pages, not just login pages?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. It improves search engine rankings\
 &nbsp; &nbsp; &nbsp; &nbsp; B. It reduces the server load\
 &nbsp; &nbsp; &nbsp; &nbsp; C. It prevents passive eavesdropping on sensitive data\
 &nbsp; &nbsp; &nbsp; &nbsp; D. It allows cookies to work\
 &nbsp; &nbsp; &nbsp; &nbsp; E. It bypasses the firewall\
 &nbsp; &nbsp; &nbsp; &nbsp; F. It blocks SQL injection\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C\
—\
Question 14: What is a static application security testing (SAST) tool used for?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Monitoring traffic between client and server\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Analyzing code for vulnerabilities before execution\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Preventing XSS at runtime\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Managing firewall rules\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Enforcing role-based access controls\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Automating login flows\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: B\
—\
Question 15: Which of the following would best help detect suspicious user behavior?\
 &nbsp; &nbsp; &nbsp; &nbsp; A. Enforcing password rotation every week\
 &nbsp; &nbsp; &nbsp; &nbsp; B. Configuring HTTPS\
 &nbsp; &nbsp; &nbsp; &nbsp; C. Logging and monitoring application activity\
 &nbsp; &nbsp; &nbsp; &nbsp; D. Running npm audit on frontend code\
 &nbsp; &nbsp; &nbsp; &nbsp; E. Blocking all cookies\
 &nbsp; &nbsp; &nbsp; &nbsp; F. Using SHA-1 for password hashing\
 &nbsp; &nbsp; &nbsp; &nbsp; ✅ Correct Answer: C



