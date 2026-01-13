# Day 14 – picoCTF Web Exploitation Challenge

## Challenge Name
Forbidden Paths

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

Can you get the flag?

We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt`,  
but the website is filtering absolute file paths.  
Can you get past the filter to read the flag?

URL: http://saturn.picoctf.net:50903/

---

## Objective
To bypass file path restrictions and read a sensitive file using directory traversal techniques.

---

## Commands / Techniques Learned
- Directory Traversal (Path Traversal)
- Relative File Paths
- Understanding Linux File System Structure
- Bypassing Input Filters

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed an input field that allowed users to read files by specifying a file path.

<img width="1715" height="786" alt="Screenshot 2026-01-13 183554" src="https://github.com/user-attachments/assets/727db9fb-b1c1-47a3-9502-8d80a5d26e13" />

3. Attempted to read files using an **absolute path**, such as: /usr/share/nginx/html/flag.txt

<img width="1918" height="964" alt="Screenshot 2026-01-13 190256" src="https://github.com/user-attachments/assets/03c26010-a26e-479c-aed1-1e1b3cc4cc7a" />

4. The application returned a **Not Authorized** message, indicating that absolute paths were being filtered.

<img width="1716" height="788" alt="Screenshot 2026-01-13 183533" src="https://github.com/user-attachments/assets/e19cb913-6eb8-4fb5-81f0-32a77f227491" />

5. Inspected the page source using **Ctrl + U**, but did not find any useful information related to the file validation logic.
6. Based on the challenge description and Linux file system behavior, inferred that **relative paths** might not be filtered.
7. Used a **directory traversal payload** to move up the directory hierarchy: ../../../../../flag.txt

<img width="1716" height="786" alt="Screenshot 2026-01-13 183325" src="https://github.com/user-attachments/assets/76857733-a91b-4850-a17a-ff233d7281a8" />

8. This payload works by repeatedly moving to the parent directory (`..`) until reaching the root directory, and then accessing the target file (`flag.txt`).
9. Submitted the traversal payload in the input field.
10. The application successfully read and displayed the contents of `flag.txt`, revealing the flag.

<img width="1714" height="788" alt="Screenshot 2026-01-13 183248" src="https://github.com/user-attachments/assets/6a2a9908-dc9f-4036-80c3-f2c09973eca4" />

---

## Flag

