# Day 02 – picoCTF Web Exploitation Challenge

## Challenge Name
Local Authority

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
Can you get the flag?
Go to this website and see what you can discover.

URL:  http://saturn.picoctf.net:64969/

The challenge provides a login page that requires a username and password to access protected content.

---

## Objective
To analyze the login functionality and identify insecure authorization logic that exposes sensitive information.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Browser Developer Tools (Inspect Element)
- URL Path Manipulation
- Client-Side JavaScript Analysis

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login page** asking for a username and password.

<img width="1915" height="970" alt="image" src="https://github.com/user-attachments/assets/e19705b9-d25e-465a-8a1b-fd838de8ef7f" />

3. Used **Ctrl + U** to inspect the page source, but no flag or credentials were found.

<img width="1918" height="973" alt="Screenshot 2025-12-30 222640" src="https://github.com/user-attachments/assets/bef1cae3-856b-480f-abde-9c32675a4774" />

4. Right-clicked on the page and selected **Inspect**, but still did not find any useful information.
5. Entered an **invalid username and password** and attempted to log in.

<img width="1919" height="973" alt="Screenshot 2025-12-29 234838" src="https://github.com/user-attachments/assets/ad7351d8-693b-4770-bef6-fa7b794752c7" />
   
6. The application redirected to a **Login Failed** page.

<img width="1913" height="968" alt="Screenshot 2025-12-30 223035" src="https://github.com/user-attachments/assets/b171cf4a-2290-464a-9252-9eeea8ac941b" />

7. Right-clicked on the page and selected **Inspect**, and noticed a JavaScript file reference:

<img width="1916" height="970" alt="Screenshot 2025-12-29 235255" src="https://github.com/user-attachments/assets/f3c60764-75e0-4d84-bf42-4faa449620fb" />

8. Copied the JavaScript file name and analyzed how the application handled authentication.
9. Manually modified the URL path from: login.php to secure.php

<img width="1919" height="975" alt="Screenshot 2025-12-29 234912" src="https://github.com/user-attachments/assets/f93f09bb-386d-4ccf-85fd-e0702160ee8e" />

10. Accessing `secure.php` revealed valid login credentials inside the page.

<img width="1919" height="968" alt="Credentials" src="https://github.com/user-attachments/assets/45b177e7-81da-4372-b0af-1866e40c089e" />

11. Used the discovered username and password to log in successfully.
12. After successful authentication, the application displayed the flag.

<img width="1919" height="972" alt="Solution" src="https://github.com/user-attachments/assets/c4f11d64-4029-4dc4-90e6-c31c92c56ba4" />

---

## Flag
picoCTF{***************}

---
## Summary
This was my **Day 02 CTF challenge**, focused on understanding broken authentication and insecure authorization mechanisms.

By analyzing login behavior, inspecting JavaScript references, and manipulating URL paths, I was able to access sensitive credentials that should not have been exposed. This challenge demonstrated how improper access control and client-side trust issues can lead to serious security vulnerabilities.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*




