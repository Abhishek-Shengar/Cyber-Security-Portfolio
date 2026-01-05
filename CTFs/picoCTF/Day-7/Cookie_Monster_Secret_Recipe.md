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
5. The page redirected and displayed the message:

<img width="1919" height="966" alt="Screenshot 2026-01-05 215852" src="https://github.com/user-attachments/assets/29a8f6a4-9f7e-451d-ad67-1ac8902c794e" />


