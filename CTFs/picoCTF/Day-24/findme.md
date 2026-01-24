# Day 24 – picoCTF Web Exploitation Challenge

## Challenge Name
findme

## Category
Web Exploitation

## Difficulty
Medium

## Description / Problem Statement
**Author:** Geoffrey Njogu  

Help us test the form by submitting the username as `test` and password as `test!`.

URL: http://saturn.picoctf.net:54337/

---

## Objective
To analyze HTTP redirects and encoded parameters in network traffic in order to uncover hidden information.

---

## Commands / Techniques Learned
- HTTP Redirect Analysis
- Browser Developer Tools (Network Tab)
- Understanding URL Parameters
- Base64 Identification & Decoding
- Using CyberChef

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed a **login form** requesting a username and password.

<img width="1919" height="964" alt="Screenshot 2026-01-24 191625" src="https://github.com/user-attachments/assets/24972de1-058f-4fad-8aa6-6574b1cc57af" />

3. Logged in using the provided credentials:
   - **Username:** `test`
   - **Password:** `test!`

<img width="1919" height="969" alt="Screenshot 2026-01-24 191644" src="https://github.com/user-attachments/assets/d75ce24e-b14a-45e3-af8a-220ffe046866" />

4. After login, the application redirected to a new page displaying: Welcome fellow Human
I was redirected here by a friend of mine but I couldn't find anything. Help me search for flags :-)
5. An input box was present, but entering values only caused the page to reload without any visible output.

<img width="1919" height="967" alt="Screenshot 2026-01-24 191714" src="https://github.com/user-attachments/assets/38bce205-e7ce-478b-aaeb-02c56c1f6d60" />

6. Based on this behavior, inferred that the flag might be present in **HTTP requests or redirects**, not directly on the page.
7. Opened **Developer Tools** and navigated to the **Network** tab.
8. Enabled network logging and performed the login process again.
9. Observed **multiple HTTP requests**, including **redirect (302) responses**.
10. Inspected the redirect requests carefully and noticed an **`id` parameter** in the URL.

<img width="1919" height="963" alt="Screenshot 2026-01-24 193603" src="https://github.com/user-attachments/assets/3ad4b4d0-3cb3-4db8-85e1-3dab09e6c64f" />

11. The value of the `id` parameter appeared **encoded** and only partially visible in the first redirect.
12. Followed the redirect chain (using the next request / arrow view in the Network tab).
13. Found a second encoded value in the `id` parameter from the subsequent redirect.

<img width="1919" height="966" alt="Screenshot 2026-01-24 193547" src="https://github.com/user-attachments/assets/c1aa163c-a10a-44be-aca9-e6c8bb337f10" />

14. Combined both encoded parts.
15. Observed that the combined string ended with: == which is a strong indicator of **Base64 encoding**.
16. Copied the encoded string and opened **CyberChef**.
17. Pasted the value and applied the **From Base64** operation.
18. The decoded output revealed the flag.

<img width="1919" height="969" alt="Screenshot 2026-01-24 193114" src="https://github.com/user-attachments/assets/023b242e-a82d-40b9-8335-e5734aeb0871" />

---

## Flag (Masked)
picoCTF{***************}

