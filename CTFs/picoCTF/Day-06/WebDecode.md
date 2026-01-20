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

8. Copied the encoded string and opened **CyberChef** in a new browser tab.
9. Pasted the encoded value into CyberChef and applied the **From Base64** operation.

<img width="1918" height="968" alt="Screenshot 2026-01-03 201047" src="https://github.com/user-attachments/assets/b02eab23-9389-4612-8ad0-f57330c87438" />

10. The decoded output revealed the flag.

---

## Flag
picoCTF{***************}


---

## Summary
This was my **Day 06 CTF challenge**, focused on using web inspection techniques and decoding encoded data found in page source code.

By navigating through different pages, inspecting the HTML source, and decoding a Base64-encoded string using CyberChef, I was able to retrieve the flag. This challenge reinforced the importance of inspecting all accessible web pages and understanding common encoding techniques used to hide sensitive information.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*


