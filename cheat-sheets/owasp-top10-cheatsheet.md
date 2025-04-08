# OWASP Top 10 (2021) Cheat Sheet

| Risk | Description | Example Tools | Mitigation |
|------|-------------|----------------|------------|
| A01: Broken Access Control | Failures to restrict user access to resources | Burp Suite, ZAP | Enforce role-based access, deny by default |
| A02: Cryptographic Failures | Insecure encryption, key exposure | testssl.sh, Qualys SSL Labs | Use HTTPS, strong algorithms, secure key storage |
| A03: Injection | SQL/OS/LDAP injection flaws | sqlmap, Burp Suite | Use prepared statements, input validation |
| A04: Insecure Design | Flawed application logic | Threat modeling tools | Shift-left, design review |
| A05: Security Misconfiguration | Default configs, open S3 buckets | ScoutSuite, Lynis | Harden configs, automate deployment checks |
| A06: Vulnerable and Outdated Components | Use of insecure libraries | OWASP Dependency-Check, Snyk | Update deps, SBOM usage |
| A07: Identification and Authentication Failures | Broken login/session management | Hydra, Burp | MFA, strong password policies |
| A08: Software and Data Integrity Failures | CI/CD pipeline tampering, unsigned code | GitLeaks, SLSA | Sign code, verify integrity |
| A09: Security Logging and Monitoring Failures | Lack of incident detection | ELK Stack, Splunk | Centralized logging, alerts |
| A10: SSRF | Server-side request to internal systems | ZAP, Burp | Whitelisting, deny internal IPs |
