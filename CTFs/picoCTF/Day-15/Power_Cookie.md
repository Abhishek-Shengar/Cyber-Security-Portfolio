# Day 15 – picoCTF Web Exploitation Challenge

## Challenge Name
Power Cookie

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

Can you get the flag?  
Go to this website and see what you can discover.

URL: http://saturn.picoctf.net:58568/

---

## Objective
To analyze how cookies are used for authorization and manipulate cookie values to gain elevated privileges.

---

## Commands / Techniques Learned
- Browser Developer Tools
- Inspecting and Modifying Cookies
- Understanding Boolean Authorization Flags
- Client-Side Privilege Escalation

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed an **Online Gradebook** interface with a button labeled **Continue as Guest**.

<img width="1915" height="968" alt="Screenshot 2026-01-14 223819" src="https://github.com/user-attachments/assets/39e53932-845b-47fd-a3a2-a1e46ac885a8" />

3. Clicked on **Continue as Guest**.
4. The application redirected to another page displaying the message: We apologize, but we have no guest services at the moment.

<img width="1917" height="967" alt="Screenshot 2026-01-14 223855" src="https://github.com/user-attachments/assets/acb646a8-1f4a-40d1-acd9-0c7f6f17ea89" />

5. Based on the challenge name **Power Cookie**, inferred that access control might be handled using browser cookies.
6. Opened **Developer Tools** by right-clicking on the page and selecting **Inspect**.
7. Navigated to the **Application** tab.
8. Selected **Cookies** under the Storage section.

<img width="1916" height="973" alt="Screenshot 2026-01-14 223736" src="https://github.com/user-attachments/assets/3a46e332-db33-4182-97e8-617d0813fac2" />

9. Observed a cookie with:
- **Name:** `isAdmin`
- **Value:** `0`
10. Interpreted the value:
 - `0` → false (guest user)
 - `1` → true (admin user)
11. Modified the cookie value from:
 ```
 isAdmin = 0
 ```
 to:
 ```
 isAdmin = 1
 ```

12. Refreshed the page.
13. After refreshing, the application displayed the flag.

<img width="1917" height="969" alt="Screenshot 2026-01-14 223759" src="https://github.com/user-attachments/assets/2baa1d3a-c6f3-4cc7-9f84-54643be7e31d" />

---

## Flag

