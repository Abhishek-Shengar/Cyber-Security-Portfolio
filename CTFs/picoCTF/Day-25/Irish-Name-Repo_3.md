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
3. Opened the side menu and selected **Admin Login**.

---

4. The Admin Login page displayed an input field requesting a password.
5. Inspected the page source using **Ctrl + U**, but no credentials or flag were found.

---

6. Attempted a classic SQL Injection payload: ' OR 1=1;--

