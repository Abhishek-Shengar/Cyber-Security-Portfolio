# Day 05 – picoCTF Web Exploitation Challenge

## Challenge Name
Bookmarklet

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** Jeffery John  

Why search for the flag when I can make a bookmarklet to print it for me?  
Browse here, and find the flag!

URL: http://titan.picoctf.net:52275/

---

## Objective
To analyze a JavaScript bookmarklet and decrypt an encrypted flag using client-side JavaScript execution.

---

## Commands / Techniques Learned
- Ctrl + U (View Page Source)
- JavaScript Code Analysis
- Understanding Encryption & Decryption Logic
- Executing JavaScript using an Online Compiler

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The webpage displayed the following message:

<img width="1919" height="968" alt="Screenshot 2026-01-02 182832" src="https://github.com/user-attachments/assets/bfacbe14-ed80-4289-899b-44fcc6dc28b7" />

3. Used **Ctrl + U** to inspect the page source but did not find the flag directly.
4. Carefully reviewed the webpage content and noticed a **JavaScript bookmarklet** provided on the page.

<img width="1919" height="972" alt="Screenshot 2026-01-02 183040" src="https://github.com/user-attachments/assets/99f7add4-2add-4bd7-a08d-5a2ac4c585be" />

5. Observed that the JavaScript code contained an **encrypted flag** stored in a variable and a decryption loop using a key.
6. Copied the complete JavaScript code from the webpage.

<img width="1917" height="970" alt="Screenshot 2026-01-02 182906" src="https://github.com/user-attachments/assets/dd58f32e-8427-4134-8817-8ef0e5b25cdd" />

7. Opened an **online JavaScript compiler** in a new browser tab.
8. Pasted the copied JavaScript code into the compiler and executed it.
9. Upon running the code, a **popup alert** appeared displaying the decrypted flag.

<img width="1918" height="974" alt="Flag" src="https://github.com/user-attachments/assets/6e015b1a-7eaf-4a21-8b31-609b250ec30f" />

---

## Flag
picoCTF{***************}

---

## Summary
This was my **Day 05 CTF challenge**, focused on understanding JavaScript bookmarklets and basic client-side encryption logic.

By analyzing the provided JavaScript code and executing it in an online JavaScript compiler, I was able to decrypt and retrieve the flag. This challenge demonstrated how sensitive information can be hidden using simple encryption techniques and why exposing such logic on the client side can lead to information disclosure.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*



