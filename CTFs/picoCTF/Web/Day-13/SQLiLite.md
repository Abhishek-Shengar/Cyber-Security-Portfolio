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

<img width="1917" height="967" alt="Screenshot 2026-01-12 215436" src="https://github.com/user-attachments/assets/1fa631f8-56a4-4bb0-bb52-4657562345cc" />

6. Based on the challenge name **SQLiLite**, inferred that the application might be vulnerable to **SQL Injection**.
7. Crafted a classic SQL Injection authentication bypass payload: ' OR 1=1--

<img width="1916" height="970" alt="Screenshot 2026-01-12 215233" src="https://github.com/user-attachments/assets/24d3649c-ac51-4efb-822e-e7284135f561" />

8. Entered the payload into both the username and password fields.
9. Submitted the login form.
10. The application responded with: Logged in!
But can you see the flag? It is in plain sight.

<img width="1919" height="970" alt="Screenshot 2026-01-12 215327" src="https://github.com/user-attachments/assets/20425659-3f4a-40f7-b9d5-817aaa2520cc" />

11. After successful login, used **Ctrl + U** to inspect the page source.


<img width="1915" height="971" alt="Flag" src="https://github.com/user-attachments/assets/b8dfbac9-2689-453d-89a5-cf79d9ecbe4b" />

12. Found the flag embedded directly in the HTML source code
---

# Flag
picoCTF{***************}

---

## Summary
This challenge focused on exploiting a **SQL Injection vulnerability** in a login form.

By injecting a logical condition that always evaluates to true (`OR 1=1`), I was able to bypass authentication without valid credentials. After logging in, inspecting the page source revealed the flag. This challenge demonstrated how improper input validation and insecure SQL query construction can lead to complete authentication bypass.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
