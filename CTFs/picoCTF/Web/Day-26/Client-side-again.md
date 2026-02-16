# Day 26 – picoCTF Web Exploitation Challenge

## Challenge Name
Client-side-again

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** Danny  

Can you break into this super secure portal?

URL: http://fickle-tempest.picoctf.net:51090/

---

## Objective
To analyze and reverse client-side JavaScript obfuscation used for password verification in order to recover the correct password and obtain the flag.

---

## Commands / Techniques Learned
- Client-Side JavaScript Analysis
- Understanding JavaScript Obfuscation
- Browser Developer Tools (Sources & Console)
- Decoding Obfuscated Functions
- Reverse Engineering Client-Side Logic

---

## Methodology

1. Opened the challenge URL in a web browser.
2. The homepage displayed: New and Improved Login
Enter valid credentials to proceed along with an input box for a password.

<img width="1919" height="963" alt="Screenshot 2026-01-28 175658" src="https://github.com/user-attachments/assets/39812425-35c3-4181-a5f6-4777c99988e7" />

3. Entered a random password and submitted it.

<img width="1919" height="965" alt="Screenshot 2026-01-28 175721" src="https://github.com/user-attachments/assets/dc267c72-0a7b-4a96-ba94-59bd9795cf5c" />

4. The application responded with a popup: Incorrect password

<img width="1919" height="963" alt="Screenshot 2026-01-28 175736" src="https://github.com/user-attachments/assets/5e23181d-9527-4ee8-9478-d8fe32dc350f" />

5. Used **Ctrl + U** and browser **Developer Tools** to inspect the page source.
6. Identified an **obfuscated JavaScript file** responsible for password verification.

<img width="1919" height="966" alt="Screenshot 2026-01-28 175932" src="https://github.com/user-attachments/assets/b04427ae-9682-4cf9-a2a7-16ed21b4e14f" />

7. Observed the following characteristics in the JavaScript code:
- A string array (`_0x5a46`) containing fragments of meaningful text
- A rotation (array shifting) function
- A lookup function (`_0x4b5b`) used to access array values dynamically
- Multiple `substring()` checks used to validate parts of the password

<img width="1919" height="969" alt="Screenshot 2026-01-28 180010" src="https://github.com/user-attachments/assets/0c776512-defb-4ad3-8fe1-8733fb43f886" />

8. Determined that the password was being validated **entirely on the client side**, making it possible to reconstruct it without brute force.
9. Opened the **Console** tab in Developer Tools.
10. Manually evaluated the obfuscated lookup function calls, for example:
 ```
 _0x4b5b('0x7')
 _0x4b5b('0x6')
 _0x4b5b('0x5')
 ```
11. Each evaluation returned a readable string fragment.
12. Collected all decoded string fragments returned by the lookup function.

<img width="1919" height="966" alt="Screenshot 2026-01-28 180751" src="https://github.com/user-attachments/assets/6766273c-a172-4606-9ddb-ee7e78bd34f8" />

13. Analyzed the `substring()` index checks in the `verify()` function to determine the correct order of the fragments.
14. Combined the decoded fragments according to the logic in the script.
15. Reconstructed the full password, which matched the picoCTF flag format.
16. Entered the reconstructed password into the input field.
17. The application validated the password and revealed the flag.

<img width="1918" height="963" alt="Screenshot 2026-01-28 183517" src="https://github.com/user-attachments/assets/97efab8a-74a4-45c3-8484-94a7a5e7f0ac" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated how **client-side-only authentication mechanisms** can be bypassed through JavaScript analysis.

Even though the password verification logic was obfuscated, it was fully exposed to the user. By decoding the obfuscated strings and understanding how the verification function checked substrings, I was able to reconstruct the correct password. This highlights why sensitive authentication logic must never be implemented solely on the client side.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
