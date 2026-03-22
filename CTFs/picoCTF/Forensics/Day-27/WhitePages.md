# Day 27 – picoCTF Forensics Challenge

## Challenge Name
WhitePages

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** John Hammond  

I stopped using YellowPages and moved onto WhitePages... but the page they gave me is all blank!

Download Link: https://challenge-files.picoctf.net/c_fickle_tempest/ab5453de03105a8aab9c68b0b46e66a4fe0a781c3915ab519f7fab31b3ce6894/whitepages.txt

---

## Objective
To analyze a seemingly empty text file and recover hidden information encoded using whitespace characters.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- Text Editor
- CyberChef

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/ab5453de03105a8aab9c68b0b46e66a4fe0a781c3915ab519f7fab31b3ce6894/whitepages.txt
```
4. Verified the file type:
```bash
file whitepages.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-03-22 192941" src="https://github.com/user-attachments/assets/2c0db3e3-f14d-4b31-8ae8-5419357a62b5" />

5. Confirmed that the file was **Unicode (UTF-8) text data**.
6. Opened the file and observed that it appeared visually blank.
7. Carefully inspected the file and noticed the presence of **invisible whitespace characters**.

<img width="1919" height="1078" alt="Screenshot 2026-03-22 193409" src="https://github.com/user-attachments/assets/133d23e3-7f1b-479a-b2c1-ff4f0d0478f4" />

8. Identified that different types of whitespace were being used to encode binary data.
9. Replaced one type of whitespace character with `0` and another type with `1` using a text editor.
10. This conversion resulted in a sequence of **binary digits (0s and 1s)**.
11. Copied the binary data and opened **CyberChef**.
12. Applied the **From Binary** operation or used the **Magic** function to decode the data.
13. The decoded output revealed readable text containing the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **whitespace steganography and binary decoding**.

Although the file appeared empty, it contained hidden data encoded using different whitespace characters. By identifying and converting these invisible characters into binary values, I was able to reconstruct the encoded data. Decoding the binary data revealed the flag. This challenge highlights how even invisible characters can be used to conceal information.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
