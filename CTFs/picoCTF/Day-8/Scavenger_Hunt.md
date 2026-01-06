# Day 08 – picoCTF Web Exploitation Challenge

## Challenge Name
Scavenger Hunt

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** madStacks  

There is some interesting information hidden around this site.  
Can you find it?

**URL:**  
http://wily-courier.picoctf.net:51085/

---

## Objective
To perform web reconnaissance by inspecting multiple client-side and server-side files to uncover hidden information distributed across the website.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Inspecting CSS and JavaScript files
- Understanding `robots.txt`
- Apache configuration files (`.htaccess`)
- Hidden system files (`.DS_Store`)
- URL Path Manipulation
- Web Enumeration

---

## Methodology

1. Opened the challenge URL in a web browser.

<img width="1919" height="966" alt="Screenshot 2026-01-06 223138" src="https://github.com/user-attachments/assets/3db8674f-71c4-4bd3-af38-731820e1b5fd" />

2. Inspected the **home page source code** using **Ctrl + U**.
3. Found the **first part of the flag** embedded in the HTML source.

<img width="1919" height="966" alt="Flag 1" src="https://github.com/user-attachments/assets/e7aa3e34-7983-4fd7-9cd0-4ffb51f99e51" />

4. Observed linked client-side files and inspected the **CSS file**.
5. Found the **second part of the flag** inside the CSS source code.
6. Checked the JavaScript file, but it did not contain any flag information.

---

7. While reviewing the HTML source, noticed an external font link:

