# Day 13 – picoCTF Web Exploitation Challenge

## Challenge Name
SQLiLite

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Mubarak Mikail  

Can you login to this website?  
Try to login.

URL: http://saturn.picoctf.net:60017/

---

## Objective
To identify and exploit a SQL Injection vulnerability in a login form in order to bypass authentication and access hidden information.

---

## Commands / Techniques Learned
- SQL Injection (Authentication Bypass)
- Understanding SQL Logic
- Using SQL Injection Payloads
- Ctrl + U (View Page Source)
- Client-Side Inspection After Authentication

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login page** requesting a username and password.

<img width="1919" height="970" alt="Screenshot 2026-01-12 220613" src="https://github.com/user-attachments/assets/20037699-59ea-4837-8e98-ac904ea75a3b" />

3. Inspected the page source using **Ctrl + U**, but no credentials or flag were found.
4. Attempted to log in using random credentials:
   - **Username:** admin  
   - **Password:** password  

<img width="1919" height="972" alt="Screenshot 2026-01-12 215419" src="https://github.com/user-attachments/assets/c8b8551c-ce36-4a96-9f59-6f2212901d54" />

5. The application responded with a **Login Failed** message, indicating credentials were being validated against a backend database.

6. Based on the challenge name **SQLiLite**, inferred that the application might be vulnerable to **SQL Injection**.
7. Crafted a classic SQL Injection authentication bypass payload:

