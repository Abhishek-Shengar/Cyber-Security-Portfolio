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

**URL:**  
http://login.mars.picoctf.net/

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
3. Used **Ctrl + U** to inspect the HTML source code, but no credentials or flag were found.

---

4. Observed that the page referenced external files, including:
   - `style.css`
   - `index.js`

5. Opened the **`index.js`** file to analyze the client-side JavaScript logic.
6. Carefully reviewed the JavaScript code and identified an encoded string:

