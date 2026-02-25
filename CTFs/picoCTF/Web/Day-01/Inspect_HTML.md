
# Day 01 – picoCTF Web Exploitation Challenge

## Challenge Name
Inspect HTML

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
Author: LT ‘syreal’ Jones  

Can you get the flag?  
Go to this website and see what you can discover.

URL:  http://saturn.picoctf.net:51510/

---
## Objective
To identify hidden information in a web page using basic web inspection techniques.

---
## Commands / Techniques Learned
- Ctrl + U (View Page Source)

---

## Methodology
1. Opened the challenge URL in a web browser.
2. The webpage displayed basic HTML content.

<img width="1918" height="969" alt="Screenshot 2025-12-29 225625" src="https://github.com/user-attachments/assets/3b4f7acb-e50c-4cc0-b1e8-f9d85ede4652" />

3. Used **Ctrl + U** to inspect the page source.
4. Analyzed the HTML code for hidden comments


<img width="1915" height="968" alt="Flag" src="https://github.com/user-attachments/assets/ddaab668-46b1-4460-8dd0-fc9a070104b1" />

5. Found the flag embedded inside an HTML comment.

---

## Flag
picoCTF{***************}

---
## Summary
This was my **Day 01 CTF challenge**, focused on basic web exploitation techniques. By inspecting the HTML source code, I discovered sensitive information exposed inside an HTML comment.

This challenge helped me understand how client-side information disclosure occurs and why developers must avoid leaving confidential data in HTML source code.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*


