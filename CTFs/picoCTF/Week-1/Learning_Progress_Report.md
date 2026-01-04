# Week 01 – CTF Learning Progress Report  
*picoCTF Web Exploitation Track*

---

## Overview
This document summarizes my **Week 01 progress** while practicing **web exploitation CTF challenges** on the picoCTF platform. The focus of this week was to build a **strong foundation in client-side web security**, source code inspection, authentication flaws, and basic data decoding techniques.

All challenges were solved in **legal, controlled environments** for educational purposes.

---

## Challenges Completed (Week 01)

| Day | Challenge Name     | Key Focus Area |
|----|-------------------|---------------|
| Day 01 | Inspect HTML | HTML Source Code Inspection |
| Day 02 | Local Authority | Broken Authentication / Authorization |
| Day 03 | Includes | Client-Side File Exposure (CSS & JS) |
| Day 04 | Unminify | Minified Code Analysis |
| Day 05 | Bookmarklet | JavaScript Analysis & Decryption |
| Day 06 | WebDecode | Web Inspection & Base64 Decoding |

---

## Skills & Techniques Learned

### 🔍 Web Inspection & Reconnaissance
- Viewing page source using **Ctrl + U**
- Using browser **Inspect / Developer Tools**
- Identifying hidden information in HTML comments
- Understanding how client-side files are loaded and exposed

---

### 🔐 Authentication & Authorization Weaknesses
- Analyzing login workflows
- Observing error handling and failed login behavior
- Identifying insecure access to protected endpoints
- Understanding improper trust in client-side logic

---

### 📁 Client-Side File Analysis
- Inspecting **CSS (`.css`)** and **JavaScript (`.js`)** files
- Finding sensitive data exposed in included resources
- Understanding risks of placing secrets in client-side files

---

### 🧩 Code Reading & Analysis
- Analyzing **minified HTML**
- Identifying meaningful patterns in compressed code
- Carefully reviewing long single-line source code

---

### 🔑 Encoding & Decryption
- Recognizing **Base64-encoded** data
- Decoding encoded strings using **CyberChef**
- Understanding simple encryption/decryption logic in JavaScript

---

## Tools Used

- **Web Browser (Chrome/Firefox)**
- **Browser Developer Tools**
- **Ctrl + U (View Page Source)**
- **CyberChef** (for decoding Base64 data)
- **Online JavaScript Compiler** (for executing client-side scripts)
- **Git & GitHub** (for documentation and version control)
- **Markdown (`.md`)** for professional reporting

---

## Key Security Concepts Understood

- Client-side information disclosure
- Risks of exposing secrets in HTML, CSS, and JavaScript
- Insecure authentication logic
- Improper access control
- Weak client-side encryption practices
- Importance of secure coding and validation

---

## Documentation & Professional Practices

- Created **daily, structured Markdown writeups**
- Used **ethical flag masking**
- Included **step-by-step methodology**
- Added **screenshots for visual proof**
- Maintained **consistent folder structure**
- Used meaningful **Git commit messages**

---

## Learning Outcome (Week 01)

This week strengthened my understanding of **how attackers analyze web applications at the client side**.  
I developed the habit of:
- Observing application behavior carefully
- Inspecting all accessible resources
- Thinking like a security tester rather than only searching for flags

The challenges reinforced that **small implementation mistakes** can lead to serious security issues.

---

## Next Steps (Week 02 Goals)

- Practice more advanced web exploitation challenges
- Begin mapping challenges to **OWASP Top 10**
- Explore parameters, cookies, and headers
- Continue maintaining daily CTF documentation
- Improve automation and efficiency in analysis

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical CTF challenges conducted in controlled environments.*

