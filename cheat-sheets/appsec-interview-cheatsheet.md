# AppSec Interview Cheat Sheet

Quick notes and go-to answers for common application security interview questions.

---

## 🔑 Key Concepts

- **OWASP Top 10** — be ready to explain 3 in detail (e.g., SQLi, XSS, Auth Failures)
- **SAST vs DAST** — SAST is static (code-based); DAST is dynamic (runtime)
- **Threat Modeling** — Use STRIDE/DREAD or LINDDUN, start early in SDLC
- **API Security** — Secure APIs with OAuth2, validate input, protect tokens
- **DevSecOps** — Security integration into CI/CD (e.g., GitHub Actions + ZAP)

---

## 🛠️ Tools to Know

- **Burp Suite / ZAP** — manual and automated web app testing
- **OWASP Dependency-Check** — detect vulnerable packages
- **Checkmarx / SonarQube / CodeQL** — SAST tools
- **Postman** — API testing and fuzzing

---

## 🧠 Sample Questions & Quick Tips

> ❓ *How do you prevent SQL injection?*  
✅ Use parameterized queries, ORM libraries, and sanitize inputs.

> ❓ *What is your approach to secure design?*  
✅ Threat modeling, secure defaults, use libraries with secure patterns.

> ❓ *What’s the difference between SAST and SCA?*  
✅ SAST scans source code; SCA scans for vulnerable dependencies.

> ❓ *What are the risks of broken access control?*  
✅ Unauthorized actions like viewing/editing other users' data. Mitigate using server-side RBAC.

> ❓ *How do you stay current in security?*  
✅ OWASP, HackerOne reports, Bugcrowd disclosures, Reddit r/netsec, blogs (e.g., Bishop Fox, PortSwigger).
