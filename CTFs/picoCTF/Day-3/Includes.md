# Day 03 – picoCTF Web Exploitation Challenge

## Challenge Name
Includes

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

Can you get the flag?  
Go to this website and see what you can discover.

URL: http://saturn.picoctf.net:62602/

---

## Objective
To inspect client-side included files and identify sensitive information exposed through improper file inclusion.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Client-Side File Inspection
- Understanding Included Files (CSS & JavaScript)

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage loaded a home page containing descriptive text about programming languages and include directives.

<img width="1912" height="972" alt="Screenshot 2025-12-31 193606" src="https://github.com/user-attachments/assets/4b9abd96-11db-4ad9-a432-b816e39af2ef" />

3. Used **Ctrl + U** to inspect the page source.
4. Observed that the HTML page included two external files: style.css and script.js

<img width="1916" height="980" alt="Screenshot 2025-12-31 193657" src="https://github.com/user-attachments/assets/5d028361-d386-40cd-a423-4561f8308bc0" />

5. Clicked on **`style.css`** and reviewed its contents.
6. Found the **first part of the flag** inside the CSS file.

<img width="1916" height="980" alt="Screenshot 2025-12-31 193740" src="https://github.com/user-attachments/assets/66030f83-a7d5-4da7-8d75-61606bff4c45" />

7. Navigated back and clicked on **`script.js`**.
8. Found the **remaining part of the flag** inside the JavaScript file.

<img width="1916" height="982" alt="Screenshot 2025-12-31 193712" src="https://github.com/user-attachments/assets/c9c6405f-36a2-4ea3-9b78-691c97396150" />

9. Combined both parts obtained from the CSS and JavaScript files to form the complete flag.

---

## Flag
picoCTF{***************}

---

## Summary
This was my **Day 03 CTF challenge**, focused on understanding how sensitive information can be exposed through client-side included files.

By inspecting the page source and reviewing externally included CSS and JavaScript files, I was able to retrieve different parts of the flag and combine them. This challenge demonstrated the risks of embedding sensitive information in publicly accessible client-side resources.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*



