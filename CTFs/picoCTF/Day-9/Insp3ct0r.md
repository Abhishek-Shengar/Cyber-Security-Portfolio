# Day 09 – picoCTF Web Exploitation Challenge

## Challenge Name
Insp3ct0r

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** zaratec / danny  

Kishor Balan tipped us off that the following code may need inspection.

URL: http://fickle-tempest.picoctf.net:63965/

---

## Objective
To inspect client-side web resources and identify sensitive information distributed across HTML, CSS, and JavaScript files.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Inspecting Linked CSS and JavaScript files
- Client-Side Code Analysis
- Understanding Information Disclosure

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage loaded a simple home page.
3. Used **Ctrl + U** to inspect the HTML source code of the page.
4. Found the **first part of the flag** embedded directly in the HTML source.

---

5. While reviewing the page source, observed that the page linked two external files:
   - `mycss.css`
   - `myjs.js`

6. Clicked on **`mycss.css`** to inspect its contents.
7. Found the **second part of the flag** inside the CSS file.

---

8. Navigated back and clicked on **`myjs.js`**.
9. Inspected the JavaScript file and found the **final part of the flag**.

---

10. Combined all three parts obtained from:
   - HTML source
   - CSS file
   - JavaScript file

11. Submitted the reconstructed flag successfully.

---

## Flag (Masked)

