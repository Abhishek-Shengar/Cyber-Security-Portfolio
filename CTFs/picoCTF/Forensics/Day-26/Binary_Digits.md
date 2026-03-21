# Day 26 – picoCTF Forensics Challenge

## Challenge Name
Binary Digits

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Yahaya Meddy  

This file doesn't look like much... just a bunch of 1s and 0s. But maybe it's not just random noise. Can you recover anything meaningful from this?

Download Link: https://challenge-files.picoctf.net/c_plain_mesa/5da9b14e68244128d275e45ba304b51dbd45554b4eb25ef68c74b4a7579c6626/digits.bin

---

## Objective
To analyze binary data stored in a text file and convert it into meaningful information.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `cat`
- CyberChef

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://challenge-files.picoctf.net/c_plain_mesa/5da9b14e68244128d275e45ba304b51dbd45554b4eb25ef68c74b4a7579c6626/digits.bin
```
4. Verified the file type:
```bash
file digits.bin
```

<img width="1919" height="1079" alt="Screenshot 2026-03-21 225450" src="https://github.com/user-attachments/assets/2caa82dc-77a2-4255-b0b5-2574dbe392c5" />

5. Confirmed that the file contained ASCII text data.
6. Viewed the file contents:
```bash
cat digits.bin
```

<img width="1918" height="1068" alt="Screenshot 2026-03-21 225921" src="https://github.com/user-attachments/assets/ddda839b-de13-4796-8000-0fdae4c7afe9" />

7. Observed that the file contained a long sequence of binary digits (0s and 1s).
8. Copied the binary data and opened CyberChef.
9. Applied the From Binary operation to convert the binary data into raw bytes.
10. Used the Magic function in CyberChef to automatically interpret the output format.

<img width="1919" height="1079" alt="Screenshot 2026-03-21 232102" src="https://github.com/user-attachments/assets/9e4bf491-0dac-468c-bd81-2a8b5d59db9f" />

11. The decoded output rendered an image containing the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **binary data decoding and data format reconstruction**.

Although the file appeared to contain only binary digits, converting the data using the From Binary operation revealed underlying raw data. Using CyberChef’s Magic feature, the data was interpreted as an image, which contained the flag. This challenge highlights how encoded binary data can represent structured formats such as images.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
