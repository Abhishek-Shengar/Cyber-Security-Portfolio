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

---

7. Located the website root under:

