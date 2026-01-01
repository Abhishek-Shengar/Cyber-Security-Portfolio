# Day 04 – picoCTF Web Exploitation Challenge

## Challenge Name
Unminify

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
I don't like scrolling down to read the code of my website, so I've squished it.  
As a bonus, my pages load faster!

Browse here, and find the flag!

**URL:**  
http://titan.picoctf.net:58451/

---

## Objective
To analyze minified HTML source code and identify hidden information embedded within it.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Understanding Minified HTML
- Careful Code Inspection

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed the following content:

<img width="1914" height="971" alt="Screenshot 2026-01-01 204858" src="https://github.com/user-attachments/assets/ff7c3eea-30b8-4082-b8ca-dd0fa2117ad2" />

3. Used **Ctrl + U** to inspect the page source.
4. Observed that the entire HTML source code was **minified into a single long line**, making it difficult to read.
5. Carefully analyzed the single-line HTML code.
6. Noticed multiple occurrences of the pattern `picoCTF{}` within the code.
7. Identified the correct flag embedded inside a paragraph tag in the following format:

<img width="1919" height="972" alt="Screenshot 2026-01-01 204954" src="https://github.com/user-attachments/assets/c9b0af4c-623e-47e9-aa9f-8a1f9ca856d9" />

## Summary

This was my Day 04 CTF challenge, focused on understanding minified web content and careful source code analysis.

By inspecting a single-line minified HTML file and paying close attention to repeated patterns, I was able to locate the correct flag. This challenge demonstrated that even heavily compressed or minified code can still expose sensitive information if not handled securely.
