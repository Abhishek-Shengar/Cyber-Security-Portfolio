# Week 04 – CTF Learning Progress Report  
*picoCTF Web Exploitation Track*

---

## Overview
This report summarizes my **Week 04 progress** while solving **medium-level and advanced web exploitation challenges** on the picoCTF platform.

During this week, I focused heavily on **server-side vulnerabilities**, including **command injection, JWT misconfiguration, eval-based RCE, Server-Side Template Injection (SSTI), advanced SQL injection, and HTTP redirect analysis**. These challenges closely resemble **real-world web application security issues** and required deeper analysis beyond basic inspection.

All activities were performed in **legal, controlled environments** for educational purposes only.

---

## Challenges Completed (Week 04)

| Day | Challenge Name | Primary Focus Area |
|----|---------------|-------------------|
| Day 19 | CaaS (Cowsay as a Service) | Command Injection |
| Day 20 | JAuth | JWT Misconfiguration & Privilege Escalation |
| Day 21 | 3v@l | Python `eval()` Injection (RCE) |
| Day 22 | SSTI2 | Server-Side Template Injection with Filter Bypass |
| Day 23 | More SQLi | Advanced SQL Injection & HTTP Response Analysis |
| Day 24 | findme | Redirect Analysis & Base64 Decoding |

---

## Skills & Techniques Learned

### Remote Code Execution (RCE)
- Identified unsafe use of system commands in web services
- Exploited **command injection** using shell substitution
- Achieved file read access on the server
- Understood real-world impact of RCE vulnerabilities

---

### JWT Authentication & Authorization Flaws
- Identified JWT tokens stored in browser cookies
- Decoded JWT headers and payloads
- Exploited **`alg: none`** misconfiguration
- Modified token roles to escalate privileges
- Learned why JWT signature validation is critical

---

### Python `eval()` Injection
- Recognized error messages indicating use of `eval()`
- Exploited unsafe evaluation of user input
- Bypassed regex filters using **dynamic string construction**
- Achieved server-side file access (`/flag.txt`)
- Understood why `eval()` must never process untrusted input

---

### Server-Side Template Injection (SSTI)
- Identified Jinja2-based template rendering
- Exploited SSTI to access Python internals
- Bypassed character filtering using hex encoding
- Executed server-side OS commands
- Demonstrated SSTI leading to RCE

---

### 💉 Advanced SQL Injection
- Performed authentication bypass using SQL injection
- Used SQLite-specific logic and operators
- Analyzed SQL queries reflected by the application
- Retrieved sensitive data from unexpected responses
- Combined SQLi with HTTP traffic analysis

---

### 🌐 HTTP Traffic & Redirect Analysis
- Used Browser DevTools Network tab for inspection
- Analyzed redirect chains (302 responses)
- Identified sensitive data in URL parameters
- Recognized Base64 encoding via padding (`==`)
- Decoded hidden data using CyberChef

---

## Tools Used

- **Web Browser (Chrome)**
- **Browser Developer Tools**
  - Elements
  - Application (Cookies & Storage)
  - Sources (Global Search)
  - Network (Redirect Analysis)
- **Burp Suite**
- **CyberChef**
- **JWT Decoder (FusionAuth)**
- **Linux Command Knowledge**
- **Git & GitHub**
- **Markdown (`.md`) for documentation**

---

## Key Security Concepts Reinforced

- Client-side controls cannot be trusted
- Encoding does not equal encryption
- Blacklist-based filtering is ineffective
- JWTs must be strictly validated server-side
- Template engines can lead to RCE if misused
- Redirects and responses may leak sensitive data
- Improper input handling can fully compromise systems

---

## OWASP Top 10 Mapping (Week 04)

- **A01: Broken Access Control**
- **A02: Cryptographic Failures**
- **A03: Injection**
- **A04: Insecure Design**
- **A05: Security Misconfiguration**
- **A06: Vulnerable and Outdated Components**

---

## Documentation & Professional Practices

- Maintained **daily Markdown writeups** for each challenge
- Documented **clear, logical exploitation steps**
- Avoided trial-and-error or luck-based explanations
- Used **ethical flag masking**
- Followed **consistent repository structure**
- Practiced writing reports like a **junior penetration tester**

---

## Learning Outcome (Week 04)

This week significantly strengthened my ability to:
- Identify **server-side vulnerabilities**
- Exploit misconfigured authentication mechanisms
- Chain vulnerabilities with logical reasoning
- Analyze application behavior beyond visible UI
- Understand the **real-world impact** of insecure design choices

The challenges reinforced that **complex applications fail when fundamental security principles are ignored**, even if partial protections exist.

---

## Next Steps (Week 05 Goals)

- Practice chaining multiple vulnerabilities
- Explore parameter tampering and API abuse
- Increase hands-on usage of Burp Suite
- Begin writing vulnerability impact summaries
- Continue building a recruiter-ready security portfolio

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical CTF challenges conducted in controlled environments.*

