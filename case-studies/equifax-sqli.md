# Equifax Breach (2017) - Case Study

---

## 📅 Overview
- Breach Date: May–July 2017
- Data Compromised: SSNs, DOBs, driver’s license numbers
- Impact: 147 million people

---

## 🔍 Root Cause
- Apache Struts vulnerability (CVE-2017-5638)
- Remote code execution via crafted `Content-Type` header

---

## ⚠️ Security Lapse
- Failed to patch a known CVE for months
- No WAF or runtime protection

---

## ✅ Lessons Learned
- Set up automated patch pipelines
- Prioritize patching based on CVSS
- Monitor logs for RCE indicators
