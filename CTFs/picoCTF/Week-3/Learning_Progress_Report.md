# Week 03 – CTF Learning Progress Report  
*picoCTF Web Exploitation Track*

---

## Overview
This report summarizes my **Week 03 progress** while solving **medium-level web exploitation challenges** on the picoCTF platform.

During this week, I transitioned from basic client-side issues to **server-side vulnerabilities**, including **SQL Injection, directory traversal, filter bypass techniques, and advanced source inspection**. The focus was on understanding **how real-world web applications fail when input validation, access control, and filtering are poorly implemented**.

All challenges were solved in **legal, controlled environments** for educational purposes only.

---

## Challenges Completed (Week 03)

| Day | Challenge Name | Primary Focus Area |
|----|---------------|-------------------|
| Day 13 | SQLiLite | SQL Injection (Authentication Bypass) |
| Day 14 | Forbidden Paths | Directory Traversal |
| Day 15 | Power Cookie | Cookie-Based Privilege Escalation |
| Day 16 | Search Source | Large-Scale Source Code Analysis |
| Day 17 | Login | Client-Side JavaScript Disclosure |
| Day 18 | Web Gauntlet 2 | SQL Injection Filter Bypass (SQLite) |

---

## Skills & Techniques Learned

# SQL Injection (Intermediate Level)
- Identifying SQL Injection vulnerabilities based on application behavior
- Using boolean logic (`OR 1=1`) for authentication bypass
- Understanding SQLite-specific behavior
- Bypassing blacklisted SQL keywords using:
  - String concatenation (`||`)
  - Alternative logical expressions
- Exploiting insecure login implementations

---

### 📂 File Access & Path Traversal
- Understanding Linux file system structure
- Using relative paths (`../`) to bypass absolute path filters
- Exploiting directory traversal vulnerabilities to access sensitive files
- Recognizing improper file access validation

---

### 🍪 Cookie-Based Authorization Flaws
- Identifying cookies used for access control (`isAdmin`)
- Modifying boolean cookie values to escalate privileges
- Understanding why client-side authorization checks are insecure
- Observing how applications rely on cookies for logic control

---

### 🔍 Advanced Source Code Analysis
- Efficiently searching through large codebases
- Using **Developer Tools → Sources** instead of manual inspection
- Performing global searches across all loaded resources
- Identifying sensitive artifacts left in CSS and JavaScript files

---

### 🧩 Client-Side JavaScript Vulnerabilities
- Analyzing JavaScript logic for hidden or encoded data
- Identifying Base64-encoded secrets in client-side files
- Decoding encoded values using **CyberChef**
- Understanding why encoding is not a security control

---

## Tools Used

- **Web Browser (Chrome)**
- **Browser Developer Tools**
  - Elements
  - Application (Cookies & Storage)
  - Sources (Global Search)
- **Ctrl + U** (View Page Source)
- **CyberChef**
- **Online JavaScript Tools**
- **Git & GitHub**
- **Markdown (`.md`) for structured documentation**

---

## Key Security Concepts Reinforced

- SQL Injection remains one of the most critical web vulnerabilities
- Blacklist-based input filtering is ineffective
- Client-side data (cookies, JS variables) must never be trusted
- Authorization must always be enforced server-side
- Directory traversal vulnerabilities can expose critical system files
- Sensitive data should never be stored in client-side resources

---

## OWASP Top 10 Mapping (Week 03)

- **A01: Broken Access Control**
- **A03: Injection**
- **A04: Insecure Design**
- **A05: Security Misconfiguration**
- **A02: Cryptographic Failures (Information Disclosure)**

---

## Documentation & Professional Practices

- Maintained **daily Markdown writeups** for each challenge
- Documented **clear reasoning and exploitation steps**
- Avoided luck-based or trial-and-error explanations
- Used **ethical flag masking**
- Followed a **consistent folder structure**
- Practiced writing like a **junior penetration tester**

---

## Learning Outcome (Week 03)

This week significantly strengthened my ability to:
- Exploit **server-side vulnerabilities**
- Think in terms of **filter bypass and input validation weaknesses**
- Analyze applications at scale instead of line-by-line guessing
- Apply logic-driven exploitation rather than random testing

The challenges emphasized that **security controls must be correctly designed and enforced**, as partial protections often create a false sense of security.

---

## Next Steps (Week 04 Goals)

- Practice more advanced SQL Injection techniques
- Explore parameter tampering and request manipulation
- Begin hands-on testing with tools like Burp Suite
- Continue mapping challenges to OWASP Top 10
- Maintain professional, recruiter-ready documentation

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical CTF challenges conducted in controlled environments.*

