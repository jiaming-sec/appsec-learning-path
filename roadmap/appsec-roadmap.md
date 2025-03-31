## 📌 1. OWASP Top 10 (2021)

The OWASP Top 10 is a list of the most critical security risks in web applications. Learn what they are, how they work, and how to prevent them.

### 🔎 Examples & Practice:
| Vulnerability | Description | Example | Practice Lab |
|---------------|-------------|---------|--------------|
| A01: Broken Access Control | Users access data/actions they shouldn’t | Changing `/user/123` to `/user/124` to access another user’s data | [Juice Shop - Admin Panel Bypass](https://owasp.org/www-project-juice-shop/) |
| A02: Cryptographic Failures | Insecure data storage/transmission | Not using HTTPS or storing passwords in plaintext | [PortSwigger - Insecure Transport](https://portswigger.net/web-security/ssl) |
| A03: Injection | Malicious input altering queries | `' OR 1=1--` in login forms (SQL Injection) | [TryHackMe - Injection Room](https://tryhackme.com/room/owaspinjections) |
| A07: Auth Failures | Weak login, no MFA, session hijack | Reusing predictable session tokens | [Web Security Academy - Auth Lab](https://portswigger.net/web-security/authentication) |

