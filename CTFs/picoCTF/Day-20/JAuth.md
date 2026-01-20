# Day 20 – picoCTF Web Exploitation Challenge

## Challenge Name
JAuth

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Geoffrey Njogu  

Most web application developers use third-party components without testing their security.  
Several real-world breaches have occurred due to vulnerable or misconfigured components.

Can you identify the vulnerable component and exploit it?  
Can you become an admin?

You can log in as:
- **Username:** test  
- **Password:** Test123!

URL: http://saturn.picoctf.net:50936/

---

## Objective
To identify and exploit a vulnerability in JSON Web Token (JWT) authentication by manipulating token contents to escalate privileges.

---

## Commands / Techniques Learned
- JWT (JSON Web Token) Analysis
- Inspecting Cookies via Browser Developer Tools
- Understanding JWT Header, Payload, and Signature
- Algorithm Confusion / `alg: none` Attack
- Client-Side Privilege Escalation

---

## Methodology

1. Opened the challenge URL in a web browser.
2. Logged in using the provided credentials:
   - **Username:** test  
   - **Password:** Test123!

3. After successful login, opened **Developer Tools** by right-clicking and selecting **Inspect**.
4. Navigated to the **Application** tab.
5. Selected **Cookies** under the Storage section.

---

6. Observed a cookie containing a value named **`token`**.
7. Noticed that the token value started with:

