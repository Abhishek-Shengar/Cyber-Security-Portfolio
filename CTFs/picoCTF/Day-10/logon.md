# Day 10 – picoCTF Web Exploitation Challenge

## Challenge Name
Logon

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** bobson  

The factory is hiding things from all of its users.  
Can you login as Joe and find what they've been looking at?

**URL:**  
http://fickle-tempest.picoctf.net:59691/

---

## Objective
To analyze authentication logic and identify insecure client-side authorization controls that can be manipulated to gain elevated access.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Browser Developer Tools
- Inspecting Application Storage
- Modifying Client-Side Values
- Understanding Broken Access Control

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login page** asking for a username and password.
3. Used **Ctrl + U** to inspect the page source, but no flag or credentials were found.

---

4. Attempted to log in using:
   - **Username:** Joe  
   - **Password:** Random value  

5. The application returned the message:

