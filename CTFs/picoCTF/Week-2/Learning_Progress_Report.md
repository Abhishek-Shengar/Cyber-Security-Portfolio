# Week 02 – CTF Learning Progress Report  
*picoCTF Web Exploitation Track*

---

## Overview
This report summarizes my **Week 02 progress** while solving **web exploitation challenges** on the picoCTF platform.  
During this week, I focused on **client-side trust issues, cookie manipulation, web enumeration, and server misconfiguration**, strengthening my understanding of how real-world web vulnerabilities are identified and exploited.

All challenges were solved in **legal, controlled environments** for educational purposes only.

---

## Challenges Completed (Week 02)

| Day | Challenge Name | Primary Focus Area |
|----|----------------|-------------------|
| Day 07 | Cookie Monster Secret Recipe | Cookie Inspection & Base64 Decoding |
| Day 08 | Scavenger Hunt | Web Enumeration & Hidden Files |
| Day 09 | Insp3ct0r | Client-Side Information Disclosure |
| Day 10 | Logon | Broken Access Control |
| Day 11 | Cookies | Cookie-Based Logic Flaws |
| Day 12 | Where are the robots | `robots.txt` Enumeration |

---

## Skills & Techniques Learned

### Cookie Analysis & Manipulation
- Inspecting cookies using browser developer tools
- Identifying encoded values stored in cookies
- Decoding cookie values using Base64
- Understanding risks of trusting client-side cookie data

---

### Authentication & Access Control Weaknesses
- Analyzing login behavior and error messages
- Identifying insecure client-side authorization checks
- Modifying application storage values (e.g., `admin = false → true`)
- Understanding **Broken Access Control** vulnerabilities

---

### Web Enumeration & Reconnaissance
- Inspecting HTML source, CSS, and JavaScript files
- Discovering sensitive data across client-side resources
- Enumerating server files such as:
  - `robots.txt`
  - `.htaccess`
  - `.DS_Store`
- Understanding why `robots.txt` is not a security mechanism

---

### Client-Side Code Analysis
- Analyzing minified HTML
- Reading JavaScript logic to identify encryption/decryption routines
- Identifying insecure design patterns in front-end code

---

### Encoding & Decoding
- Recognizing Base64-encoded data
- Decoding encoded strings using **CyberChef**
- Understanding how encoded values are used to hide sensitive information

---

## Tools Used

- **Web Browser (Chrome)**
- **Browser Developer Tools**
  - Elements
  - Application (Cookies & Storage)
- **Ctrl + U** (View Page Source)
- **CyberChef**
- **Online JavaScript Compiler**
- **Git & GitHub**
- **Markdown (`.md`) for documentation**

---

## Key Security Concepts Reinforced

- Client-side data should never be trusted
- Authorization must be enforced server-side
- Cookies can be abused if improperly validated
- Sensitive files should not be publicly accessible
- Security through obscurity is ineffective
- Misconfigurations often lead to information disclosure

---

## Documentation & Professional Practices

- Created **daily structured Markdown writeups**
- Documented **clear methodology and reasoning**
- Avoided luck-based or trial-and-error explanations
- Used **ethical flag masking**
- Maintained **consistent folder structure**
- Used descriptive **Git commit messages**
- Practiced writing like a **junior penetration tester**

---

## Learning Outcome (Week 02)

This week significantly improved my ability to:
- Perform systematic web reconnaissance
- Identify logic flaws instead of relying on guessing
- Understand how attackers abuse client-side trust
- Think in terms of **security impact**, not just CTF flags

The challenges emphasized that **small implementation mistakes**—especially around cookies and access control—can result in serious vulnerabilities.

---

## Next Steps (Week 03 Goals)

- Practice challenges involving parameters and request manipulation
- Explore cookies, headers, and sessions more deeply
- Begin mapping challenges explicitly to **OWASP Top 10**
- Continue maintaining daily, professional documentation
- Improve speed and efficiency of analysis

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical CTF challenges conducted in controlled environments.*

