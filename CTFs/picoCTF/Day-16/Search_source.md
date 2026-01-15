# Day 16 – picoCTF Web Exploitation Challenge

## Challenge Name
Search Source

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Mubarak Mikail  

The developer of this website mistakenly left an important artifact in the website source.  
Can you find it?

**URL:**  
http://saturn.picoctf.net:52349/

---

## Objective
To efficiently search through multiple client-side source files and locate sensitive information left behind by the developer.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Browser Developer Tools
- Searching Across All Source Files
- Efficient Source Code Analysis

---

## Methodology

1. Opened the challenge URL in a web browser.

<img width="1915" height="965" alt="Screenshot 2026-01-15 231537" src="https://github.com/user-attachments/assets/d3aed557-b55f-4f9f-af66-5e1297d0cc1c" />

2. Initially used **Ctrl + U** to view the page source.
3. Observed that the source code was very large and referenced multiple external files such as CSS, JavaScript, images, and other resources.

<img width="1916" height="969" alt="Screenshot 2026-01-15 233051" src="https://github.com/user-attachments/assets/bc4eb321-d966-4309-acc3-d79bd5c3a89f" />

4. Recognized that manually scanning each file would be inefficient.
5. Opened **Developer Tools** by right-clicking on the page and selecting **Inspect**.
6. Navigated to the **Sources** tab in Developer Tools.
7. Located the website root under: http://saturn.picoctf.net:52349/

<img width="1917" height="969" alt="Screenshot 2026-01-15 231717" src="https://github.com/user-attachments/assets/a524a4bc-37d6-45a5-98b1-7f797067ce9f" />

8. Observed multiple files and directories, including:
- HTML files
- CSS files
- JavaScript files
- Image resources
9. Right-clicked on the website root inside the **Sources** tab.
10. Selected **Search in all files**.

<img width="1918" height="968" alt="Screenshot 2026-01-15 231746" src="https://github.com/user-attachments/assets/f1931ddc-6cad-4231-99b3-e5c2a7cce143" />

11. Used the global search feature to search for:
 ```
 pico
 ```
 (the known prefix of picoCTF flags)
12. The search returned a match inside the `style.css` file and located the flag embedded within the file.

<img width="1919" height="969" alt="Flag" src="https://github.com/user-attachments/assets/533dd5e9-a837-45be-81fe-deade5bdfbc7" />

---

## Flag (Masked)
picoCTF{***************}
