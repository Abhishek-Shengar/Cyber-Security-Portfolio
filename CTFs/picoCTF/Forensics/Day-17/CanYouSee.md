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
5. Confirmed that the file was a ZIP archive.
6. Extracted the archive:
7. After extraction, a new file appeared:
8. Analyzed the image metadata using exiftool:
9. Observed a Base64-encoded string within the metadata fields.
10. Copied the encoded data and decoded it using CyberChef with the From Base64 operation.
11. The decoded output revealed the flag.
