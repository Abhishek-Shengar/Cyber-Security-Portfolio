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

5. From this error message, inferred that:
- User input was being evaluated as **Python code**
- The backend was using Python’s `eval()` function

<img width="1918" height="967" alt="Screenshot 2026-01-21 192003" src="https://github.com/user-attachments/assets/dfd9a5da-09a3-4b4b-bf3a-d3a2360eea68" />

6. Based on the hints, determined that:
- Direct file access might be blocked by regex filters
- The target file to read was `/flag.txt`

<img width="1919" height="966" alt="Screenshot 2026-01-21 192134" src="https://github.com/user-attachments/assets/049b8de3-a563-43e5-b04d-46d7a2d7e5c3" />

7. To bypass regex-based filtering, avoided directly typing `/flag.txt`.
8. Used **dynamic string construction** with `chr()` to build the file path at runtime.
9. Crafted a Python expression that:
- Dynamically builds `/flag.txt`
- Opens the file
- Reads its contents
Example logic: open(chr(47)+'f'+'l'+'a'+'g'+chr(46)+'t'+'x'+'t').read()

<img width="1919" height="969" alt="Screenshot 2026-01-21 190536" src="https://github.com/user-attachments/assets/a05b398d-03b5-4ecc-9a69-308f35d45619" />

10. Entered the crafted payload into the input field and clicked **Execute**.
11. The application executed the injected Python code.
12. The contents of `/flag.txt` were displayed, revealing the flag.

<img width="1919" height="964" alt="Screenshot 2026-01-21 190548" src="https://github.com/user-attachments/assets/be10b7df-4c10-47dc-a97b-f45a29ecee65" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated a critical **Remote Code Execution (RCE)** vulnerability caused by unsafe use of Python’s `eval()` function.

By understanding how `eval()` executes arbitrary Python expressions and using dynamic string construction to bypass regex-based input filtering, I was able to execute system-level file access and read a sensitive file. This highlights why `eval()` should never be used on untrusted user input and why input validation alone is not sufficient for security.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*


