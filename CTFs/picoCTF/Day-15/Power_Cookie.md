# Day 15 – picoCTF Web Exploitation Challenge

## Challenge Name
Power Cookie

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

Can you get the flag?  
Go to this website and see what you can discover.

URL: http://saturn.picoctf.net:58568/

---

## Objective
To analyze how cookies are used for authorization and manipulate cookie values to gain elevated privileges.

---

## Commands / Techniques Learned
- Browser Developer Tools
- Inspecting and Modifying Cookies
- Understanding Boolean Authorization Flags
- Client-Side Privilege Escalation

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed an **Online Gradebook** interface with a button labeled **Continue as Guest**.

<img width="1915" height="968" alt="Screenshot 2026-01-14 223819" src="https://github.com/user-attachments/assets/39e53932-845b-47fd-a3a2-a1e46ac885a8" />

3. Clicked on **Continue as Guest**.
4. The application redirected to another page displaying the message:

<img width="1917" height="967" alt="Screenshot 2026-01-14 223855" src="https://github.com/user-attachments/assets/acb646a8-1f4a-40d1-acd9-0c7f6f17ea89" />


