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





