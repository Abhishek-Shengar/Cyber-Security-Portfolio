# Day 24 – picoCTF Forensics Challenge

## Challenge Name
information

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** susie  

Files can always be changed in a secret way. Can you find the flag?

Download Link: https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg

---

## Objective
To analyze image metadata and recover hidden encoded information.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `exiftool`
- `nano`
- `base64`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg
```
4. Verified the file type:
```bash
file cat.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-03-17 233540" src="https://github.com/user-attachments/assets/92d21546-f84a-4d08-b72e-f1f3b0ecd690" />

5. Confirmed that the file was a JPEG image file.
6. Suspected hidden data within the image metadata.
7. Extracted metadata using:
```bash
exiftool cat.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-03-17 233732" src="https://github.com/user-attachments/assets/48d7dd4e-f987-414a-af4f-1dea99382f7d" />

8. Observed a Base64 encoded string in the License field.
9. Saved the encoded data into a file:
```bash
nano flagclue.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-03-17 234052" src="https://github.com/user-attachments/assets/eb850bc7-5e03-4b58-ae47-c667ae9cfac2" />

10. Pasted the encoded string, saved the file (Ctrl + O, Enter), and exited (Ctrl + X).

<img width="1919" height="1079" alt="Screenshot 2026-03-17 233842" src="https://github.com/user-attachments/assets/c3c42f57-81fd-42f8-b5e2-f7b2f498e22e" />

11. Decoded the Base64 encoded data:
```bash
base64 -d flagclue.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-03-17 234520" src="https://github.com/user-attachments/assets/6b657f23-79de-4729-8455-42d11657c804" />

12. The decoded output revealed the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **image metadata analysis and Base64 decoding**.

Although the image appeared normal, hidden information was embedded within its metadata. By extracting metadata using `exiftool`, I discovered a Base64 encoded string in the License field. Decoding the string revealed the flag. This challenge highlights the importance of examining metadata when performing forensic analysis on files.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
