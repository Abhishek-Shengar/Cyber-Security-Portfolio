# Day 22 – picoCTF Web Exploitation Challenge

## Challenge Name
SSTI2

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Venax  

I made a cool website where you can announce whatever you want!  
I read about input sanitization, so now I remove any kind of characters that could be a problem :)  
I heard templating is a cool and modular way to build web apps!

**URL:**  
http://shape-facility.picoctf.net:54951/

---

## Objective
To exploit a Server-Side Template Injection (SSTI) vulnerability while bypassing input sanitization filters in order to execute server-side commands and read the flag.

---

## Commands / Techniques Learned
- Server-Side Template Injection (SSTI)
- Jinja2 Template Exploitation
- Filter Bypass Techniques
- Hex Encoding for Restricted Characters
- Server-Side Command Execution

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed an input field asking: What do you want to announce?

<img width="1919" height="963" alt="Screenshot 2026-01-22 212633" src="https://github.com/user-attachments/assets/8b83b3df-bc3b-49af-8244-acd839376829" />

3. Entered a simple input: Hello and submitted it.

<img width="1919" height="966" alt="Screenshot 2026-01-22 212658" src="https://github.com/user-attachments/assets/c46b6c1b-23a1-492f-941e-653c3597287f" />


