# OWASP Juice Shop Security Assessment

![Platform](https://img.shields.io/badge/Platform-OWASP%20Juice%20Shop-blue)
![Tool](https://img.shields.io/badge/Tool-Burp%20Suite-orange)
![Language](https://img.shields.io/badge/Language-English-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Overview

This repository documents a security assessment performed against **OWASP Juice Shop**, an intentionally vulnerable web application designed for security training and awareness. The assessment was conducted in a controlled homelab environment for educational purposes only.

The objective of this project was to practice web application penetration testing, identify common vulnerabilities, and document findings following a structured reporting methodology.

> **Disclaimer**
>
> All testing was performed exclusively against OWASP Juice Shop in a local homelab environment. No unauthorized testing was conducted against production or third-party systems.

---

## Objectives

- Build hands-on experience in Web Application Security.
- Practice identifying common web vulnerabilities.
- Improve technical reporting and documentation skills.
- Learn secure coding recommendations based on OWASP guidance.

---

## Lab Environment

| Component | Description |
|-----------|-------------|
| Host OS | Windows 10 |
| Target | OWASP Juice Shop |
| Deployment | Docker |
| Browser | Chromium |
| Proxy | Burp Suite Community Edition |

---

## Methodology

The assessment followed the workflow below:

1. Application reconnaissance
2. Feature exploration
3. Vulnerability identification
4. Vulnerability validation
5. Documentation and reporting

---

## Findings

| Vulnerability | Severity | Report |
|---------------|----------|--------|
| Authentication Bypass via SQL Injection | High | [sql-injection.md](findings/sql-injection.md) |
| Reflected Cross-Site Scripting (XSS) | Medium | [reflected-xss.md](findings/xss.md) |
| Insecure Direct Object Reference (IDOR) | High | [idor.md](findings/idor.md) |

---

## Risk Summary

| Severity | Count |
|----------|------:|
| High | 2 |
| Medium | 1 |
| Low | 0 |

---

## Report

The complete assessment report is available in:

```
reports/report.pdf
```

---

## References

- OWASP Juice Shop
- OWASP Top 10
- OWASP Web Security Testing Guide (WSTG)
- Burp Suite Documentation

---

## Author

**Indra Risqiawan**

Cybersecurity Enthusiast | Web Application Security | Penetration Testing