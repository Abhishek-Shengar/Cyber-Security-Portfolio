# Day 17 – picoCTF Forensics Challenge

## Challenge Name
CanYouSee

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Mubarak Mikail  

How about some hide and seek?

Download Link: https://artifacts.picoctf.net/c_titan/130/unknown.zip

---

## Objective
To analyze a compressed file and recover hidden information from image metadata.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `unzip`
- `exiftool`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the compressed file:
```bash
wget https://artifacts.picoctf.net/c_titan/130/unknown.zip
```
4. Verified the file type:
```bash
file unknown.zip
```
5. Confirmed that the file was a ZIP archive.

<img width="1919" height="1072" alt="Screenshot 2026-02-27 181020" src="https://github.com/user-attachments/assets/8ad50958-06f2-4b8c-8f72-a1a730a54a19" />

6. Extracted the archive:
```bash
unzip unknown.zip
```
7. After extraction, a new file appeared: ukn_reality.jpg
8. Analyzed the image metadata using exiftool:
```bash
exiftool ukn_reality.jpg
```

<img width="1919" height="1075" alt="Screenshot 2026-02-27 181751" src="https://github.com/user-attachments/assets/23473e3b-0f2f-49b4-a21f-68e50c2f45c4" />

9. Observed a Base64-encoded string within the metadata fields.
10. Copied the encoded data and decoded it using CyberChef with the From Base64 operation.

<img width="1919" height="968" alt="Screenshot 2026-02-27 181931" src="https://github.com/user-attachments/assets/7750d3a6-13ab-4592-a9ff-a8350c18c9a8" />

11. The decoded output revealed the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **image metadata analysis and Base64 decoding**.

Although the image appeared normal visually, important information was hidden within its metadata. Using `exiftool`, I extracted the embedded metadata and identified a Base64-encoded string. Decoding the string revealed the flag. This challenge highlights the importance of inspecting file metadata during forensic investigations.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
