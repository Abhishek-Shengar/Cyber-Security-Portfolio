# Day 06 – picoCTF Web Exploitation Challenge

## Challenge Name
WebDecode

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** Nana Ama Atombo-Sackey  

Do you know how to use the web inspector?  
Start searching here to find the flag.

URL: http://titan.picoctf.net:59483/

---

## Objective
To inspect different web pages and decode encoded data found in the source code to retrieve the flag.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- Web Navigation (Home / About Pages)
- Base64 Decoding
- Using CyberChef for Decoding

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed the following message: Ha!!!!!! You looking for a flag?
Keep Navigating

<img width="1918" height="974" alt="Screenshot 2026-01-03 201205" src="https://github.com/user-attachments/assets/6f6ae94d-130b-4c7f-bc20-8970b3d02a84" />

3. Used **Ctrl + U** to inspect the source code of the home page, but did not find any relevant information related to the flag.
4. Navigated to the **About** page using the website navigation.
5. The About page displayed a hint encouraging inspection of the page.

<img width="1918" height="971" alt="Screenshot 2026-01-03 201226" src="https://github.com/user-attachments/assets/5800ced3-47db-4e68-90ab-4386f54cd9e2" />

6. Used **Ctrl + U** on the About page to inspect the source code.
7. Found the following encoded string in the page source: cGljb0NURnt3ZWJ***************

<img width="1915" height="971" alt="Screenshot 2026-01-03 201133" src="https://github.com/user-attachments/assets/2824791c-ef42-4ab6-9535-b4224084da02" />


