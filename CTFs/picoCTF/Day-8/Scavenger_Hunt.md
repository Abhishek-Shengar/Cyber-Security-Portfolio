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

URL: http://wily-courier.picoctf.net:51085/

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

<img width="1919" height="969" alt="Flag 2" src="https://github.com/user-attachments/assets/b7a02953-ae03-4bce-8047-270393fb6367" />

6. Checked the JavaScript file, but it did not contain any flag information.
7. While reviewing the HTML source, noticed an external font link: https://fonts.googleapis.com/css?family=Open+Sans|Roboto
8. Recognized the word **Roboto** as a hint and modified the URL to: /robots.txt
9. Accessed `robots.txt` and found the **third part of the flag**, along with a clue: I think this is an apache server... can you Access the next flag?

<img width="1919" height="969" alt="Flag 3" src="https://github.com/user-attachments/assets/e07f1126-48c6-4115-ad85-5c88abf46fca" />

10. Researched Apache server files and identified that **`.htaccess`** is used to control access on Apache web servers.
11. Modified the URL to: /.htaccess
12. Accessed the file and obtained the **fourth part of the flag**.

<img width="1919" height="970" alt="Flag 4" src="https://github.com/user-attachments/assets/d5a39c80-161e-431c-b974-b04d2fc79328" />

13. Found another clue in the source: I love making websites on my Mac, I can store a lot of information there.

---

14. Researched common hidden files used by macOS.
15. Identified **`.DS_Store`** as a macOS system file that can sometimes be exposed on web servers.
16. Modified the URL to:
 ```
 /.DS_Store
 ```
17. Accessed the file and retrieved the **final part of the flag**.

---

18. Combined all the collected parts to form the complete flag.

---

## Flag (Masked)

