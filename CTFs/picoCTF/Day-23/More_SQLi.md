# Day 23 – picoCTF Web Exploitation Challenge

## Challenge Name
More SQLi

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Mubarak Mikail  

Can you find the flag on this website?  
Try to find the flag here.

URL: http://saturn.picoctf.net:50851/

---

## Objective
To exploit a SQL Injection vulnerability in a login form and analyze server responses to retrieve sensitive information.

---

## Commands / Techniques Learned
- SQL Injection (Authentication Bypass)
- Understanding SQL Queries
- HTTP Request & Response Analysis
- Using Burp Suite for Intercepting Traffic
- Identifying Sensitive Data in Responses

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login form** requesting a username and password.

<img width="1918" height="966" alt="Screenshot 2026-01-24 182359" src="https://github.com/user-attachments/assets/2d73f128-d2be-48a4-9680-b5c5d0b37518" />

3. Attempted to log in using:
   - **Username:** admin  
   - **Password:** password  

<img width="1919" height="966" alt="Screenshot 2026-01-24 182423" src="https://github.com/user-attachments/assets/afe884dd-456d-4c23-a7b0-a382745924e8" />

4. After submitting the form, the application displayed the executed SQL query: SELECT id FROM users WHERE password = 'password' AND username = 'admin'

<img width="1919" height="966" alt="Screenshot 2026-01-24 182438" src="https://github.com/user-attachments/assets/b59df6f2-7e40-440c-87a8-4cdd7221f750" />

5. From this output, confirmed that:
- User input was directly embedded into the SQL query
- The application was vulnerable to **SQL Injection**

6. Crafted a SQL Injection payload to bypass authentication:
- **Username:** admin  
- **Password:** `' OR 1=1--`
7. This payload modifies the SQL logic so that the condition always evaluates to true, bypassing the password check.

<img width="1917" height="968" alt="Screenshot 2026-01-24 190459" src="https://github.com/user-attachments/assets/8820f7c5-7aa6-4448-83d6-11884760ad43" />

8. To better observe server behavior, opened **Burp Suite** and enabled intercept.
9. Submitted the login request again with the SQL Injection payload.

<img width="1919" height="1018" alt="Screenshot 2026-01-24 184918" src="https://github.com/user-attachments/assets/7d073cd7-acce-4980-ab29-ccd9c2598fa3" />

10. Observed multiple HTTP responses in Burp Suite, including responses with:
 - **Status Code:** 302 (Redirect)
11. Inspected the **302 redirect responses** carefully.
12. Found that one of the responses contained sensitive data in the response body, including the flag.

<img width="1919" height="1016" alt="Screenshot 2026-01-24 190814" src="https://github.com/user-attachments/assets/7505e3d8-51f9-4e51-8860-bf1d4a9ea22b" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated how SQL Injection vulnerabilities can lead to unintended information disclosure.

By injecting a logical condition into the login query, I bypassed authentication and triggered database output. Analyzing the HTTP responses—particularly redirect responses—revealed sensitive information that should not have been exposed. This highlights the importance of proper input sanitization and careful handling of server responses.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
