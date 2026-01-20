# Day 20 – picoCTF Web Exploitation Challenge

## Challenge Name
JAuth

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Geoffrey Njogu  

Most web application developers use third-party components without testing their security.  
Several real-world breaches have occurred due to vulnerable or misconfigured components.

Can you identify the vulnerable component and exploit it?  
Can you become an admin?

You can log in as:
- **Username:** test  
- **Password:** Test123!

URL: http://saturn.picoctf.net:50936/

---

## Objective
To identify and exploit a vulnerability in JSON Web Token (JWT) authentication by manipulating token contents to escalate privileges.

---

## Commands / Techniques Learned
- JWT (JSON Web Token) Analysis
- Inspecting Cookies via Browser Developer Tools
- Understanding JWT Header, Payload, and Signature
- Algorithm Confusion / `alg: none` Attack
- Client-Side Privilege Escalation

---

## Methodology

1. Opened the challenge URL in a web browser.


<img width="1919" height="968" alt="Screenshot 2026-01-20 215217" src="https://github.com/user-attachments/assets/3cfc14e7-7d23-4720-8775-7f4ad172951d" />

2. Logged in using the provided credentials:
   - **Username:** test  
   - **Password:** Test123!


<img width="1919" height="969" alt="Screenshot 2026-01-20 215235" src="https://github.com/user-attachments/assets/497d1146-30e0-4ce7-b675-d0beb4bc8fe6" />

3. After successful login, shown a message: Hello, You have logged in the testing page. There is nothing to see here.

<img width="1919" height="967" alt="Screenshot 2026-01-20 215249" src="https://github.com/user-attachments/assets/dd1dd1d0-1fc3-4bde-9c2b-a29020bdd17c" />

4. Opened **Developer Tools** by right-clicking and selecting **Inspect**.Navigated to the **Application** tab.
5. Selected **Cookies** under the Storage section.
6. Observed a cookie containing a value named **`token`**.
7. Noticed that the token value started with: eyJ... which is a common indicator of a **JWT (JSON Web Token)**.

<img width="1919" height="970" alt="Screenshot 2026-01-20 215327" src="https://github.com/user-attachments/assets/0ec3af07-fd21-4d91-bfd7-db3d27f082b3" />



---

8. Copied the JWT token value.
9. Opened an online JWT decoder (e.g., FusionAuth JWT Decoder).
10. Pasted the token into the decoder to inspect its contents.

---

11. Analyzed the decoded JWT and observed:
 - **Header:** algorithm set to `HS256`
 - **Payload:** role set to `user`

12. Identified that the application was vulnerable to an **insecure JWT implementation** that trusted the token without proper signature verification.

---

13. Modified the JWT as follows:
 - Changed the **Header** algorithm:
   ```
   "alg": "none"
   ```
 - Changed the **Payload** role:
   ```
   "role": "admin"
   ```

14. Re-encoded the modified header and payload as a new JWT **without a signature**.
15. Copied the newly generated JWT token.

---

16. Replaced the original JWT value in the browser cookies with the modified token.
17. Refreshed the page.

18. The application accepted the modified token and granted **admin access**, revealing the flag.

---

## Flag (Masked)
