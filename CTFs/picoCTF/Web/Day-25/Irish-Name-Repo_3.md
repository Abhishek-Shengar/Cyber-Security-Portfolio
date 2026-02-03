# Day 25 – picoCTF Web Exploitation Challenge

## Challenge Name
Irish-Name-Repo 3

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Xingyang Pan  

Try to see if you can login as admin!

URL: http://fickle-tempest.picoctf.net:62095/

---

## Objective
To bypass authentication by exploiting a filtered SQL Injection vulnerability in an admin login page.

---

## Commands / Techniques Learned
- SQL Injection (Filtered Environment)
- SQLite Error Analysis
- Understanding Keyword Transformation
- ROT13 Encoding Bypass
- Authentication Bypass

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed a list of people with their names and quotes.

<img width="1919" height="968" alt="Screenshot 2026-01-26 101633" src="https://github.com/user-attachments/assets/085e4683-f59c-4661-a526-5b4dcc160c59" />

3. Opened the side menu and selected **Admin Login**.

<img width="1919" height="968" alt="Screenshot 2026-01-26 101657" src="https://github.com/user-attachments/assets/887c8037-44ce-4580-8190-b710ee786308" />

4. The Admin Login page displayed an input field requesting a password.

<img width="1919" height="966" alt="Screenshot 2026-01-26 101711" src="https://github.com/user-attachments/assets/781304f4-1f7c-4d72-ab5a-0672222e0f09" />

5. Inspected the page source using **Ctrl + U**, but no credentials or flag were found.
6. Attempted a classic SQL Injection payload: ' OR 1=1;--

<img width="1919" height="967" alt="Screenshot 2026-01-26 102559" src="https://github.com/user-attachments/assets/9df88bcc-faa3-4dd8-94d0-4849817ec732" />

7. The application returned an error message: SQLite3::query(): Unable to prepare statement
indicating that:
- The backend database was **SQLite**
- Input was being filtered or transformed before execution

<img width="1919" height="965" alt="Screenshot 2026-01-26 102658" src="https://github.com/user-attachments/assets/d4a657af-fe0d-4361-b308-57ffaa35d7d0" />

8. From the error behavior and challenge context, inferred that **SQL keywords were being filtered or modified**.
9. Researched and identified that this application applies **ROT13 encoding** to certain SQL keywords.
10. Since:
 ```
 or  → be  (ROT13)
 ```
11. Crafted a ROT13-encoded SQL Injection payload: ' be 1=1;--
 ```
 ' be 1=1;--
 ```
12. Submitted the payload in the password field.

<img width="1919" height="967" alt="Screenshot 2026-01-26 102559" src="https://github.com/user-attachments/assets/0a2243f3-bfae-4db9-ae3e-4d80708fc12a" />

13. The backend decoded the input internally, reconstructing a valid SQL condition.
14. Authentication was bypassed, and admin access was granted.
15. The application revealed the flag.

<img width="1919" height="967" alt="Screenshot 2026-01-26 102610" src="https://github.com/user-attachments/assets/a2dee1b8-a76c-4ccd-a3b2-cf5802faf315" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated how **input transformation mechanisms**, such as ROT13 encoding, can be abused to bypass SQL Injection filters.

Although the application attempted to block common SQL keywords, it relied on insecure filtering rather than proper parameterized queries. By encoding the SQL keyword using ROT13, I was able to bypass the filter and execute a successful authentication bypass. This highlights why keyword-based filtering is ineffective against SQL Injection attacks.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*

