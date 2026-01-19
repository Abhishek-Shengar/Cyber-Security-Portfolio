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
2. The homepage displayed the following information:
Cowsay as a Service
Make a request to the following URL to cowsay your message:
https://caas.mars.picoctf.net/cowsay/{message}


3. Copied the provided URL format and opened it in a new browser tab.
4. Replaced `{message}` with a simple string: https://caas.mars.picoctf.net/cowsay/Hello
5. The server returned a cowsay output displaying the message “Hello”, confirming that user input was being processed by the backend.

---

6. Based on the challenge context, inferred that the service might be executing a shell command using the user-provided input.
7. Researched common vulnerabilities related to services that wrap system commands and identified **command injection** as a likely attack vector.

---

8. Tested command substitution by injecting $(ls) into the URL: https://caas.mars.picoctf.net/cowsay/$(ls)

9. The response displayed a list of files present on the server, confirming that **command injection was possible**.
10. Observed a file named:
 ```
 flag.txt
 ```

---

11. Used command substitution again to read the contents of the file:
 ```
 $(cat flag.txt)
 ```
12. Submitted the payload:
 ```
 https://caas.mars.picoctf.net/cowsay/$(cat flag.txt)
 ```

13. The server returned the contents of `flag.txt`, revealing the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge focused on exploiting a **command injection vulnerability** in a web service that directly passed user input to a system command.

By identifying that the application executed shell commands without proper input sanitization, I was able to inject additional commands using shell substitution syntax. This allowed me to enumerate files on the server and read a sensitive file containing the flag. The challenge demonstrated why user input must never be passed directly to system commands without strict validation and sanitization.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
