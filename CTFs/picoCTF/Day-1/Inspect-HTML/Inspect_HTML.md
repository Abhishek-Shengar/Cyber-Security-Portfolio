
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

4. Used **Ctrl + U** to inspect the page source.

<img width="1915" height="968" alt="Flag" src="https://github.com/user-attachments/assets/ddaab668-46b1-4460-8dd0-fc9a070104b1" />

6. Analyzed the HTML code for hidden comments.
7. Found the flag embedded inside an HTML comment.

----

## Flag
picoCTF{***************}
