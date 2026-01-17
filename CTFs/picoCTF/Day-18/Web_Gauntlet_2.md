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

---

7. Opened the second provided URL: 
