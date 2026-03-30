# OWASP Top 10 — Web Application Security Lab

**Objective:** Identify and exploit OWASP Top 10 vulnerabilities in a controlled lab environment using DVWA (Damn Vulnerable Web Application).

---

## Lab Environment

| Virtual Machine | Role | IP Address |
|---|---|---|
| Kali Linux | Attacker machine | 192.168.56.102 |
| DVWA (Docker on Kali) | Target application | localhost:80 |
| Windows VM | Victim browser | 192.168.56.104 |
| Ubuntu VM | RFI payload host | 192.168.56.103 |

---

## Tasks Performed

| # | Task | What Was Done |
|---|---|---|
| 1 | SQL Injection | Extracted usernames and passwords from DVWA database using manual payloads and sqlmap. Prevention demonstrated using Prepared Statements. |
| 2 | Cross-Site Scripting (XSS) | Stored and Reflected XSS attacks performed. Session cookie stolen via XSS payload. Mitigated using CSP headers and input validation. |
| 3 | Cross-Site Request Forgery (CSRF) | Malicious HTML page created to silently change admin password. Token-based protection demonstrated as fix. |
| 4 | File Inclusion (LFI + RFI) | Local File Inclusion used to read /etc/passwd. Remote File Inclusion used to execute a web shell hosted on Ubuntu VM. |
| 5 | Burp Suite Advanced | Login requests intercepted and modified via Burp Proxy. Password brute forced using Burp Intruder Sniper attack. |
| 6 | Web Security Headers | Missing headers identified via curl and securityheaders.com. Seven security headers added to Apache config and verified. |

---

> All attacks were performed in a fully isolated, controlled lab environment on intentionally vulnerable software (DVWA). Strictly for educational purposes only.
