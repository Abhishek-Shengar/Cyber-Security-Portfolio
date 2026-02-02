# Day 19 – picoCTF Web Exploitation Challenge

## Challenge Name
CaaS (Cowsay as a Service)

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** BrownieInMotion  

Now presenting cowsay as a service.

URL: https://caas.mars.picoctf.net/

---

## Objective
To identify and exploit a command injection vulnerability in a web service that executes system commands using user-controlled input.

---

## Commands / Techniques Learned
- Understanding Command Injection
- Linux Command Substitution
- URL Parameter Manipulation
- Basic Linux Commands (`ls`, `cat`)
- Server-Side Command Execution Risks

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed the following information: Cowsay as a Service
Make a request to the following URL to cowsay your message:
https://caas.mars.picoctf.net/cowsay/{message}

<img width="1919" height="966" alt="Screenshot 2026-01-19 210913" src="https://github.com/user-attachments/assets/a7ddc98c-1ada-44fe-b658-66fed88d1c0c" />

3. Copied the provided URL format and opened it in a new browser tab.

<img width="1919" height="968" alt="Screenshot 2026-01-19 214143" src="https://github.com/user-attachments/assets/d18003ad-9817-490f-9ee7-3c75adc166fc" />

4. Replaced `{message}` with a simple string: https://caas.mars.picoctf.net/cowsay/Hello
5. The server returned a cowsay output displaying the message “Hello”, confirming that user input was being processed by the backend.

<img width="1919" height="966" alt="Screenshot 2026-01-19 211218" src="https://github.com/user-attachments/assets/9c63f5f4-d9e7-4f73-8c68-524e6b2c2ef0" />

6. Based on the challenge context, inferred that the service might be executing a shell command using the user-provided input.
7. Researched common vulnerabilities related to services that wrap system commands and identified **command injection** as a likely attack vector.
8. Tested command substitution by injecting $(ls) into the URL: https://caas.mars.picoctf.net/cowsay/$(ls)
9. The response displayed a list of files present on the server, confirming that **command injection was possible**.
10. Observed a file named: falg.txt

<img width="1919" height="967" alt="Screenshot 2026-01-19 212322" src="https://github.com/user-attachments/assets/cf96a1d7-cec5-49fa-aa63-c89c13638c53" />

11. Used command substitution again to read the contents of the file: $(cat falg.txt)
12. Submitted the payload: https://caas.mars.picoctf.net/cowsay/$(cat falg.txt)

<img width="1919" height="968" alt="Screenshot 2026-01-19 212354" src="https://github.com/user-attachments/assets/17cbcc2f-1eb9-4b5f-bcac-27e3b481d20c" />

13. The server returned the contents of `falg.txt`, revealing the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge focused on exploiting a **command injection vulnerability** in a web service that directly passed user input to a system command.

By identifying that the application executed shell commands without proper input sanitization, I was able to inject additional commands using shell substitution syntax. This allowed me to enumerate files on the server and read a sensitive file containing the flag. The challenge demonstrated why user input must never be passed directly to system commands without strict validation and sanitization.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
