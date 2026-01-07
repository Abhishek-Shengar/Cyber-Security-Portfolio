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

<img width="1919" height="967" alt="Screenshot 2026-01-07 222322" src="https://github.com/user-attachments/assets/af6deecb-40d9-4ea1-9004-b43fa71fb063" />

3. Used **Ctrl + U** to inspect the HTML source code of the page.
4. Found the **first part of the flag** embedded directly in the HTML source.

<img width="1919" height="969" alt="Flag 1" src="https://github.com/user-attachments/assets/5a623db7-d4ef-4c9b-b20c-7881535c4d16" />

5. While reviewing the page source, observed that the page linked two external files:
   - `mycss.css`
   - `myjs.js`

6. Clicked on **`mycss.css`** to inspect its contents.
7. Found the **second part of the flag** inside the CSS file.

<img width="1917" height="968" alt="Flag 2" src="https://github.com/user-attachments/assets/cb342b97-59c4-4846-8e8c-32ae5cb0f147" />

8. Navigated back and clicked on **`myjs.js`**.
9. Inspected the JavaScript file and found the **final part of the flag**.

<img width="1918" height="968" alt="Flag 3" src="https://github.com/user-attachments/assets/60dc7049-2095-48d8-a7f6-2e270b3551bc" />

10. Combined all three parts obtained from:
   - HTML source
   - CSS file
   - JavaScript file

11. Submitted the reconstructed flag successfully.

---

## Flag (Masked)

