<img width="1919" height="1079" alt="Screenshot 2026-03-20 233237" src="https://github.com/user-attachments/assets/8b7f0380-4a83-448d-aea8-300056ca6adb" /># Day 25 – picoCTF Forensics Challenge

## Challenge Name
Glory of the Garden

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** jedavis / Danny  

This file contains more than it seems.  
Get the flag from garden.jpg.

Download Link: https://challenge-files.picoctf.net/c_fickle_tempest/6013221da747114c37db29c554381dbe4bb4e746cf6bd880f9c3b5d0b495a823/garden.jpg

---

## Objective
To analyze a JPEG file and extract hidden textual data using efficient forensic techniques.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `strings`
- `grep`
- `thunar`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/6013221da747114c37db29c554381dbe4bb4e746cf6bd880f9c3b5d0b495a823/garden.jpg
```
4. Verified the file type:
```bash
file garden.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-03-20 233237" src="https://github.com/user-attachments/assets/34e5968c-37c7-4a7d-aa40-0eb4bd4df913" />

5. Confirmed that the file was a JPEG image file.
6. Opened the image using a file manager to visually inspect it:
```bash
thunar garden.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-03-20 233635" src="https://github.com/user-attachments/assets/248c3f92-194d-4882-9994-13f116ea2f2e" />






---

## Flag (Masked)
picoCTF{***************}

---
