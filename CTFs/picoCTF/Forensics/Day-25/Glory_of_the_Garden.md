# Day 25 – picoCTF Forensics Challenge

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

7. No visible flag or hidden text was observed in the image.
8. Based on the challenge hint (hex editor), inferred that hidden data might exist in the file’s raw content.
9. Instead of manually inspecting with a hex editor, used a more efficient approach to extract readable strings:
```bash
strings garden.jpg | grep pico
```

<img width="1919" height="1075" alt="Screenshot 2026-03-20 233713" src="https://github.com/user-attachments/assets/f7832fb8-9845-4067-9c48-0213409bc5cd" />

10. The command directly revealed the flag embedded within the file.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **efficient data extraction from binary files using string analysis**.

Although the hint suggested using a hex editor, I used the `strings` command combined with `grep` to quickly locate readable text within the file. This approach allowed me to efficiently extract the embedded flag without manually analyzing hexadecimal data. The challenge highlights how simple command-line tools can be highly effective in forensic investigations.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
