# Secure CI/CD Pipeline Cheat Sheet

Shift security left by embedding checks into your CI/CD pipelines.

---

## 🏗 Tools & Techniques by Stage

### 1. 📝 Pre-Commit
- Secret scanning (`truffleHog`, `gitleaks`)
- Linting and secure code formatters

### 2. 🔍 Static Analysis (SAST)
- GitHub CodeQL
- SonarQube
- Checkmarx

### 3. 🧪 Dependency Scanning (SCA)
- OWASP Dependency-Check
- Snyk
- `npm audit`, `pip-audit`
