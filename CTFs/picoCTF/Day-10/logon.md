# Day 10 – picoCTF Web Exploitation Challenge

## Challenge Name
Logon

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** bobson  

The factory is hiding things from all of its users.  
Can you login as Joe and find what they've been looking at?

URL: http://fickle-tempest.picoctf.net:59691/

---

## Objective
To analyze authentication logic and identify insecure client-side authorization controls that can be manipulated to gain elevated access.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Browser Developer Tools
- Inspecting Application Storage
- Modifying Client-Side Values
- Understanding Broken Access Control

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login page** asking for a username and password.

<img width="1919" height="968" alt="Screenshot 2026-01-08 183208" src="https://github.com/user-attachments/assets/ec590744-2456-4c87-9946-0e5ec7d4f03e" />

3. Used **Ctrl + U** to inspect the page source, but no flag or credentials were found.
4. Attempted to log in using:
   - **Username:** Joe  
   - **Password:** Random value  
5. The application returned the message: I'm sorry Joe's password is super secure. You're not getting in that way.

<img width="1919" height="969" alt="Screenshot 2026-01-08 183806" src="https://github.com/user-attachments/assets/aa96e339-ebd4-439a-b0ee-1b5b67eaecc4" />


6. Attempted to log in again using:
- **Username:** Bob  
- **Password:** Random value  
8. Also opened **Developer Tools** by right-clicking and selecting **Inspect**.
9. Navigated to the **Application** tab.

<img width="1915" height="970" alt="Screenshot 2026-01-08 183259" src="https://github.com/user-attachments/assets/4f0708f0-6425-4a9e-8eae-0aa86019bd47" />

7. This time, login was successful and the page displayed: Success: You logged in! Not sure you'll be able to see the flag though. No flag for you.

<img width="1918" height="963" alt="Screenshot 2026-01-08 183405" src="https://github.com/user-attachments/assets/0b9d4c1c-404f-4137-b29e-3022dcebe7bc" />

10. Under the storage section, found a table containing an entry:
 ```
 admin = false
 ```

11. Modified the value of `admin` from:
 ```
 false → true
 ```

12. Refreshed the page.
13. After refreshing, the application displayed the flag.

---

## Flag

