# Day 12 – picoCTF Web Exploitation Challenge

## Challenge Name
Where are the robots

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** zaratec / Danny  

Can you find the robots?

URL: http://fickle-tempest.picoctf.net:53551/

---

## Objective
To identify hidden resources by analyzing the `robots.txt` file and accessing disallowed paths exposed by the web server.

---

## Commands / Techniques Learned
- Understanding `robots.txt`
- URL Path Manipulation
- Web Enumeration
- Identifying Disallowed Resources

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed a message: Welcome
Where are the robots?

<img width="1919" height="969" alt="Screenshot 2026-01-10 231830" src="https://github.com/user-attachments/assets/3200bb7d-5302-41e2-8e89-2f3f9478e557" />

3. Based on the challenge name and hint, inferred that the solution involved the **`robots.txt`** file.
4. Modified the URL to access: /robots.txt
5. Viewed the contents of the `robots.txt` file.
6. Found a **disallowed HTML file** listed under the `Disallow` directive.

<img width="1915" height="964" alt="Screenshot 2026-01-10 231729" src="https://github.com/user-attachments/assets/c601bd3e-27d4-4772-9849-888bab0b7c19" />

7. Copied the disallowed file name.
8. Modified the URL by replacing: /robots.txt with /<disallowed-file-name>
9. Accessed the disallowed path directly through the browser.
10. The page revealed the flag.

<img width="1915" height="965" alt="Flag" src="https://github.com/user-attachments/assets/fa8c7ed6-30de-4112-a0b7-476db5a856f9" />

---

## Flag
picoCTF{***************}

---

## Summary
This challenge demonstrated how sensitive information can be unintentionally exposed through `robots.txt`.

By inspecting the `robots.txt` file and accessing a disallowed resource directly, I was able to retrieve the flag. This highlights a common misconception that `robots.txt` provides security, when in reality it only instructs web crawlers and does not prevent direct access to sensitive files.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
