# Day 18 – picoCTF Web Exploitation Challenge

## Challenge Name
Web Gauntlet 2

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** madStacks  

This website looks familiar...  
Log in as **admin**.

Site: http://wily-courier.picoctf.net:61211/

Filter: http://wily-courier.picoctf.net:61211/filter.php

---

## Objective
To bypass server-side input filters and exploit a SQL injection vulnerability in order to authenticate as an administrator.

---

## Commands / Techniques Learned
- SQL Injection (SQLite)
- Filter Evasion Techniques
- Understanding Blocked Keywords
- Boolean Logic Abuse
- Input Validation Bypass

---

## Methodology

1. Opened the main challenge URL in a web browser.
2. The webpage displayed a **login form** requesting a username and password.

<img width="1919" height="968" alt="Screenshot 2026-01-17 184054" src="https://github.com/user-attachments/assets/3dfae926-bfc6-4e42-bc08-739dc09b4ef5" />

3. Attempted to log in using:
   - **Username:** admin  
   - **Password:** random value  
4. The application rejected the login attempt, indicating that authentication checks were enforced.

<img width="1919" height="967" alt="Screenshot 2026-01-17 182335" src="https://github.com/user-attachments/assets/47e711f9-ba31-4d64-9dc5-13a5a4b2e267" />

5. Inspected the page source but did not find any useful credentials or flags.
6. Noticed an encoded hash (SHA-384), but determined that it was not directly useful for authentication bypass.

<img width="1919" height="949" alt="Screenshot 2026-01-17 182424" src="https://github.com/user-attachments/assets/fbe6ee16-5265-4dac-9ea7-f25847df9b10" />

7. Opened the second provided URL: /filter.php
8. This page listed **filtered keywords and characters**, including: or, and, true, false, union, like, =, >, <, ;, --, /* */, admin

<img width="1919" height="967" alt="Screenshot 2026-01-17 182126" src="https://github.com/user-attachments/assets/91a45188-027c-48f3-9960-2bb9b9f1ba2d" />

9. From this information, concluded that the application was filtering **common SQL injection payloads** and keywords.
10. Based on SQLite behavior, researched **alternative logical operators** and filter bypass techniques.
11. Identified that SQLite supports string concatenation using:
 ```
 ||
 ```

12. Crafted a filter-evasion SQL injection payload:
 - **Username:**
   ```
   adm'||'in
   ```
 - **Password:**
   ```
   ' is not '0
   ```

<img width="1918" height="966" alt="Screenshot 2026-01-17 184712" src="https://github.com/user-attachments/assets/20787918-238a-4401-8a77-eb9b1c1df5c5" />

13. Submitted the payload through the login form.
14. The application displayed the message: Congrats! You won! Check out filter.php

<img width="1919" height="969" alt="Screenshot 2026-01-17 183419" src="https://github.com/user-attachments/assets/c75bc813-b07a-4b1c-98e8-0a286d9ae254" />

15. Navigated back to `/filter.php` and refreshed the page.
16. The page revealed the flag.

<img width="1919" height="967" alt="Screenshot 2026-01-17 182157" src="https://github.com/user-attachments/assets/ad6239f8-e2c1-414d-9558-095126e29e2b" />

## Flag (Masked)

