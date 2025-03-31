## 📌 1. OWASP Top 10 (2021)

The OWASP Top 10 is a list of the most common and critical security risks in web applications. Each entry represents a category of vulnerability and includes details on risk, impact, and remediation.

### A01: Broken Access Control
- **What**: Users can access resources or perform actions beyond their intended permissions.
- **Example**: A regular user accesses an admin page by changing the URL (`/admin`).
- **Mitigation**: Implement role-based access control, deny by default, and test all endpoints.

### A02: Cryptographic Failures
- **What**: Weak or missing encryption of sensitive data.
- **Example**: Transmitting passwords over HTTP, storing data without encryption.
- 
### A03: Injection
- **What**: Malicious input alters the logic of an application.
- **Example**: SQL Injection (`' OR '1'='1` bypasses login).
- **Mitigation**: Use parameterized queries and input validation.
