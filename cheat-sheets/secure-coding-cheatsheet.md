# Secure Coding Cheat Sheet

## ✅ Input Validation
- Never trust user input
- Whitelist instead of blacklist
- Use built-in sanitizers

## 🔐 Authentication
- Store passwords with bcrypt or Argon2
- Implement account lockout
- Use MFA wherever possible

## 🧾 Session Management
- Use `HttpOnly` and `Secure` flags on cookies
- Rotate session IDs after login
- Invalidate sessions on logout

## 📦 Dependency Management
- Use tools like Snyk or OWASP Dependency-Check
- Avoid outdated/abandoned packages

## 🛡️ Error Handling
- Don’t expose stack traces or detailed errors to users
- Log errors internally
