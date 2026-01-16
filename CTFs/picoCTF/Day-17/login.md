# Day 17 – picoCTF Web Exploitation Challenge

## Challenge Name
Login

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** BrownieInMotion  

My dog-sitter's brother made this website but I can't get in; can you help?

URL: http://login.mars.picoctf.net/

---

## Objective
To analyze client-side JavaScript files and identify encoded sensitive information left in the website source.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Inspecting Linked JavaScript Files
- Client-Side Code Analysis
- Base64 Decoding
- Using CyberChef

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login page** requesting a username and password.

<img width="1919" height="967" alt="Screenshot 2026-01-16 182846" src="https://github.com/user-attachments/assets/e90676f8-a800-47f5-8d7c-04d5dd6c6a53" />

3. Used **Ctrl + U** to inspect the HTML source code, but no credentials or flag were found.
4. Observed that the page referenced external files, including:
   - `style.css`
   - `index.js`

<img width="1919" height="972" alt="Screenshot 2026-01-16 183427" src="https://github.com/user-attachments/assets/efeb2144-f794-4584-90a8-c2efa8ec62a1" />

5. Opened the **`index.js`** file to analyze the client-side JavaScript logic.
6. Carefully reviewed the JavaScript code and identified an encoded string:

