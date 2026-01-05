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
3. Used **Ctrl + U** to inspect the page source but did not find any credentials or flag.
4. Entered a **random username and password** and attempted to log in.
5. The page redirected and displayed the message:
