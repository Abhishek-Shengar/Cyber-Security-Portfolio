# Day 21 – picoCTF Forensics Challenge

## Challenge Name
Flag in Flame

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Prince Niyonshuti N.

The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within?

Download Link: https://challenge-files.picoctf.net/c_amiable_citadel/ade5acd5e8e7082fc52cbbb6b297da484b0656fa4ce51b3b923c9d2c0f4a93f7/logs.txt

---

## Objective
To analyze encoded log data and extract hidden information through multiple decoding and forensic analysis steps.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `strings`
- `base64`
- `tesseract`
- `cat`
- CyberChef

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the log file:
```bash
wget https://challenge-files.picoctf.net/c_amiable_citadel/ade5acd5e8e7082fc52cbbb6b297da484b0656fa4ce51b3b923c9d2c0f4a93f7/logs.txt
```
4. Verified the file type:
```bash
file logs.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-03-05 232712" src="https://github.com/user-attachments/assets/5bbcc2da-e8a9-4e25-bb01-8e5b42772f7a" />

5. Confirmed that the file contained large encoded text data.
6. Inspected the content and identified that the data appeared to be Base64 encoded.
7. Decoded the Base64 data and redirected the output into an image file:
```bash
strings logs.txt | base64 -d > flag.jpg
```
8. The decoded output generated an image file named flag.jpg.
9. Opened the image and observed encoded text embedded inside the image.
10. Used OCR to extract the text from the image:
```bash
tesseract flag.jpg output
```
11. This generated a file named: output.txt
12. Read the extracted text:
```bash
cat output.txt
```
13. Observed that the extracted text was hexadecimal encoded.
14. Copied the hex string and decoded it using CyberChef with the From Hex operation.
15. The decoded output revealed the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **multi-layer data decoding and forensic analysis**.

The log file contained Base64-encoded data which decoded into an image. The image contained encoded text that required OCR extraction using `tesseract`. The extracted text was hexadecimal encoded and decoding it revealed the flag. This challenge highlights how attackers may layer multiple encoding techniques to conceal sensitive information.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
