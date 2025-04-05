## 📌 1. OWASP Top 10 (2021)

The OWASP Top 10 is a list of the most common and critical security risks in web applications. Each entry represents a category of vulnerability and includes details on risk, impact, and remediation.

### A01: Broken Access Control
- **What**: Users can access resources or perform actions beyond their intended permissions.
- **Example**: A regular user accesses an admin page by changing the URL (`/admin`).
- **Mitigation**: Implement role-based access control, deny by default, and test all endpoints.

### A02: Cryptographic Failures
- **What**: Weak or missing encryption of sensitive data.
- **Example**: Transmitting passwords over HTTP, storing data without encryption.
- **Mitigation**: Use HTTPS, strong algorithms (AES-256), and secure key management.

### A03: Injection
- **What**: Malicious input alters the logic of an application.
- **Example**: SQL Injection (`' OR '1'='1` bypasses login).
- **Mitigation**: Use parameterized queries and input validation.
  
### A04: Insecure Design
- **What**: Flaws in system architecture and logic.
- **Example**: No limits on failed login attempts.
- **Mitigation**: Apply security principles during the design phase (e.g., least privilege).

### A05: Security Misconfiguration
- **What**: Default settings, exposed files, open ports, verbose errors.
- **Example**: Admin panels left open, stack traces shown to users.
- **Mitigation**: Harden environments, remove unused services, use secure headers.

### A06: Vulnerable and Outdated Components
- **What**: Using libraries or platforms with known vulnerabilities.
- **Example**: Running jQuery v1.7, which has XSS vulnerabilities.
- **Mitigation**: Keep dependencies updated and monitor advisories.

### A07: Identification and Authentication Failures
- **What**: Weak login systems.
- **Example**: No multi-factor authentication (MFA), predictable credentials.
- **Mitigation**: Use MFA, limit login attempts, secure password storage.

### A08: Software and Data Integrity Failures
- **What**: Unverified code or updates, lack of integrity checks.
- **Example**: Auto-update features downloading unsigned files.
- **Mitigation**: Sign code, enforce integrity via checksums and secure pipelines.

### A09: Security Logging and Monitoring Failures
- **What**: Missing or ineffective logging.
- **Example**: No alert for failed login attempts or data exfiltration.
- **Mitigation**: Centralized logging, alerting, incident response planning.

### A10: Server-Side Request Forgery (SSRF)
- **What**: Attacker forces server to access internal resources.
- **Example**: Submitting URLs that access internal APIs (e.g., `http://localhost:8000`).
- **Mitigation**: Validate and restrict URLs, use firewall rules.

---

## 🧑‍💻 2. Secure Coding Practices - In Depth

Secure coding reduces the attack surface at the development stage.

### Key Practices:
- **Input Validation**: Always validate user input.
  - Use whitelisting, not blacklisting.
  - Example: Restrict allowed file types in file uploads.

- **Output Encoding**: Encode data before rendering in the browser.
  - Prevents XSS attacks.
  - Use libraries like OWASP Java Encoder or `htmlspecialchars()` in PHP.

- **Authentication and Authorization**:
  - Never roll your own auth. Use standard libraries (e.g., OAuth, OpenID Connect).
  - Ensure separation of authentication and authorization checks.

- **Secure Session Management**:
  - Use secure cookies, implement session expiration.
  - Regenerate session IDs after login.

- **Error Handling**:
  - Don’t expose internal errors to users.
  - Log securely and return generic error messages.

- **Secrets Management**:
  - Don’t hardcode credentials.
  - Use secret management systems like AWS Secrets Manager or HashiCorp Vault.

---

## 🧠 3. Threat Modeling - What, Why, and How

### What is Threat Modeling?
Threat modeling is the process of identifying potential security threats in an application and designing controls to prevent them.

### Why is it Important?
- Identifies vulnerabilities **before** they’re coded.
- Reduces cost of fixes by catching issues early.
- Improves architecture design and team awareness.

### How to Do It:
1. **Define the system**: Diagram data flows, assets, actors.
2. **Identify threats**: Use STRIDE to brainstorm threats.
3. **Prioritize**: Rate threats based on likelihood and impact.
4. **Mitigate**: Plan and implement defenses.

### Common Frameworks:
- **STRIDE** (Spoofing, Tampering, Repudiation, Info Disclosure, DoS, Privilege Escalation)
- **PASTA** (Process for Attack Simulation and Threat Analysis)
- **LINDDUN** (Privacy-focused)

### Tools:
- OWASP Threat Dragon
- Microsoft Threat Modeling Tool

---

## 🔍 4. Code Review for Security - Explained

Code review helps catch security issues during development

### What to Look For:
- Input not validated/sanitized
- Hardcoded secrets or API keys
- Direct object references without access checks
- Unsafe use of eval, exec, or reflection
- Insecure third-party libraries

### Best Practices:
- Use a checklist (OWASP Secure Code Review Guide)
- Review small chunks regularly
- Automate with static analysis (e.g., Semgrep, SonarQube)

### Tools:
- GitHub Code Scanning with CodeQL
- Semgrep
- SonarCloud / SonarQube

---
