# Day 13 – picoCTF Forensics Challenge

## Challenge Name
extensions

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Sanjay C / Danny  

This is a really weird text file. Can you find the flag?  
Get the flag from TXT.

Download Link: https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt

---

## Objective
To identify mismatched file extensions and recover hidden data by analyzing the true file type.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `eog` (Eye of GNOME Image Viewer)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt
```
4. Verified the file type:
```bash
file flag.txt
```
5. Although the file extension was .txt, the file command revealed that the actual file type was a PNG image.
6. Recognized that the file extension had been intentionally misleading.

<img width="1919" height="1077" alt="Screenshot 2026-02-19 233550" src="https://github.com/user-attachments/assets/02d691cf-6912-407b-b63e-fc9069a2f7b5" />

7. Opened the file using an image viewer:
```bash
eog flag.txt
```
8. The image opened successfully and displayed the flag.

<img width="1919" height="1079" alt="Screenshot 2026-02-19 233811" src="https://github.com/user-attachments/assets/3f594a81-0cf0-47af-8082-a2de7f4a0df4" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **file extension spoofing and file signature verification**.

Although the file was named with a `.txt` extension, its actual file signature identified it as a PNG image. By verifying the true file type and opening it with the appropriate viewer, I was able to recover the flag. This challenge highlights the importance of validating file signatures rather than relying solely on file extensions during forensic analysis.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
