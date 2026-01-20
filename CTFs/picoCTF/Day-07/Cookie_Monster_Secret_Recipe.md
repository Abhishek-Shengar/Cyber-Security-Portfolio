# Day 07 – picoCTF Web Exploitation Challenge

## Challenge Name
Cookie Monster Secret Recipe

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** Brhane Giday and Prince Niyonshuti N.  

Cookie Monster has hidden his top-secret cookie recipe somewhere on his website.  
As an aspiring cookie detective, your mission is to uncover this delectable secret.

Can you outsmart Cookie Monster and find the hidden recipe?

**URL:**  
http://verbal-sleep.picoctf.net:53631/

---

## Objective
To analyze HTTP cookies used by a web application and decode hidden information stored in cookie values.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Browser Developer Tools
- Inspecting Cookies via Application Tab
- Base64 Decoding
- Using CyberChef

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed a **login page** asking for a username and password.

<img width="1919" height="967" alt="Screenshot 2026-01-05 211129" src="https://github.com/user-attachments/assets/1f901b93-33ba-4729-8623-c22ddfd89587" />

3. Used **Ctrl + U** to inspect the page source but did not find any credentials or flag.
4. Entered a **random username and password** and attempted to log in.
5. The page redirected and displayed the message: Cookie Monster Says:
"Me no need password. Me just need cookies!" along with the hint: Have you checked your cookies lately?


<img width="1919" height="966" alt="Screenshot 2026-01-05 215852" src="https://github.com/user-attachments/assets/29a8f6a4-9f7e-451d-ad67-1ac8902c794e" />


6. Right-clicked on the page and selected **Inspect** to open Developer Tools.
7. Navigated to the **Application** tab in Chrome Developer Tools.

<img width="1915" height="965" alt="Screenshot 2026-01-05 214154" src="https://github.com/user-attachments/assets/c1b2da0d-f70b-4ccd-ad7d-4642d4ed7d11" />

8. Selected **Cookies** under the Storage section.
9. Initially, no cookies were present.

<img width="1919" height="970" alt="Screenshot 2026-01-05 214240" src="https://github.com/user-attachments/assets/8d51b4d0-23e2-4684-a54e-0ec96b1d1614" />

10. After submitting random login credentials again, a cookie appeared in the cookies table with an **encoded value**.
11. Copied the encoded cookie value.

<img width="1911" height="971" alt="Screenshot 2026-01-05 213449" src="https://github.com/user-attachments/assets/4561bfed-4b95-417c-8a7f-ad3d112767c0" />

12. Opened **CyberChef** in a new browser tab.
13. Pasted the cookie value into CyberChef and applied the **From Base64** operation.
14. The decoded output revealed the flag.

<img width="1919" height="969" alt="flag" src="https://github.com/user-attachments/assets/672f9474-e3d2-4288-8f59-0cb5894a5ac2" />

---

## Flag
picoCTF{***************}

---

## Summary
This was my **Day 07 CTF challenge**, focused on analyzing browser cookies and understanding how sensitive data can be stored and exposed through them.

By inspecting cookies using browser developer tools and decoding a Base64-encoded cookie value with CyberChef, I was able to retrieve the flag. This challenge highlighted the importance of secure cookie handling and demonstrated how attackers can exploit improperly protected cookie data.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*

