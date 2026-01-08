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

URL: http://fickle-tempest.picoctf.net:59691/

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

<img width="1919" height="968" alt="Screenshot 2026-01-08 183208" src="https://github.com/user-attachments/assets/ec590744-2456-4c87-9946-0e5ec7d4f03e" />

3. Used **Ctrl + U** to inspect the page source, but no flag or credentials were found.
4. Attempted to log in using:
   - **Username:** Joe  
   - **Password:** Random value  
5. The application returned the message: I'm sorry Joe's password is super secure. You're not getting in that way.

<img width="1919" height="969" alt="Screenshot 2026-01-08 183806" src="https://github.com/user-attachments/assets/aa96e339-ebd4-439a-b0ee-1b5b67eaecc4" />


6. Attempted to log in again using:
- **Username:** Bob  
- **Password:** Random value  

7. This time, login was successful and the page displayed:

