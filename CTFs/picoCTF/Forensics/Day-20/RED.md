# Day 20 – picoCTF Forensics Challenge

## Challenge Name
RED

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Shuailin Pan (LeConjuror)  

RED, RED, RED, RED  

Download Link: https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png

---

## Objective
To analyze a PNG image for hidden steganographic data and recover the concealed flag.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `zsteg`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png
```
4. Verified the file type:
```bash
file red.png
```

<img width="1919" height="1079" alt="Screenshot 2026-03-03 212107" src="https://github.com/user-attachments/assets/fc4cd342-7aef-42a6-9d40-2c968cfa2710" />

5. Confirmed that the file was a PNG image.
6. Based on the challenge title and category, suspected hidden steganographic data.
7. Used zsteg to analyze the image for hidden content:
```bash
zsteg red.png
```

<img width="1919" height="1078" alt="Screenshot 2026-03-03 212835" src="https://github.com/user-attachments/assets/10d13a5e-42c8-4014-9f4f-9cb640f08c50" />

8. The tool output revealed an encoded string embedded within one of the color channel bit planes.
9. The extracted string appeared to be Base64-encoded text.
10. Copied the encoded string and opened **CyberChef**.
11. Applied the **From Base64** operation to decode the string.

<img width="1919" height="970" alt="Screenshot 2026-03-03 213014" src="https://github.com/user-attachments/assets/3007f375-1b71-4a56-aaf6-3432b4dfad18" />

12. The decoded output revealed the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **PNG steganography detection and Base64 decoding**.

Although the image appeared visually simple, hidden data was embedded within its bit planes. Using `zsteg`, I identified the concealed encoded string and decoded it using Base64 decoding techniques. This challenge reinforces the importance of inspecting image files beyond their visual content when conducting forensic analysis.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
