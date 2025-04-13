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

### 4. 🌐 DAST
- OWASP ZAP in GitHub Actions
- Burp Suite Enterprise (for org-level scanning)

### 5. 🔐 Container Security
- Trivy
- Docker Bench
- Clair, Grype

---

## 🛡 Security Best Practices

- Least privilege for CI runners
- Isolate secrets using vaults (e.g., GitHub Secrets)
- Run tests in clean environments (no developer tokens)
- Use signed commits and releases (Sigstore/Cosign)
