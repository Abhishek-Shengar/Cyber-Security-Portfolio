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
6. Extracted the archive:
```bash
unzip unknown.zip
```
7. After extraction, a new file appeared: ukn_reality.jpg
8. Analyzed the image metadata using exiftool:
```bash
exiftool ukn_reality.jpg
```
9. Observed a Base64-encoded string within the metadata fields.
10. Copied the encoded data and decoded it using CyberChef with the From Base64 operation.
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
