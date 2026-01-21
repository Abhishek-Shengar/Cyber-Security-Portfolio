# Day 21 – picoCTF Web Exploitation Challenge

## Challenge Name
3v@l

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Theoneste Byagutangaza  

ABC Bank's website has a loan calculator to help its clients calculate the amount they pay if they take a loan from the bank.  
Unfortunately, the calculator uses the `eval()` function to process user input.

Bypassing this will give you **Remote Code Execution (RCE)**.

**Hints Provided:**
- Bypass regex
- The flag file is `/flag.txt`
- You might need encoding or dynamic construction to bypass restrictions

URL: http://shape-facility.picoctf.net:64002/

---

## Objective
To exploit insecure use of the Python `eval()` function in a web application and achieve remote code execution in order to read a sensitive file.

---

## Commands / Techniques Learned
- Python `eval()` Injection
- Remote Code Execution (RCE)
- Regex Filter Bypass
- Dynamic String Construction
- Python Built-in Functions (`open`, `chr`)

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **loan calculator** with:
   - An input field labeled **“Enter the formula”**
   - An **Execute** button

<img width="1919" height="971" alt="Screenshot 2026-01-21 190226" src="https://github.com/user-attachments/assets/5ba48b28-b581-4445-9c35-8d88fe7ace5d" />

3. Entered a simple string: Hello and clicked on **Execute**.
4. The application returned: Error: name 'Hello' is not defined

<img width="1917" height="965" alt="Screenshot 2026-01-21 191140" src="https://github.com/user-attachments/assets/459fa3e0-00b9-46de-b145-5f490023f1e6" />



