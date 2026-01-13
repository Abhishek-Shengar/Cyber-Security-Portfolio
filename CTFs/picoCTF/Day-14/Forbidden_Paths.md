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

**URL:**  
http://saturn.picoctf.net:50903/

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

---

3. Attempted to read files using an **absolute path**, such as:

