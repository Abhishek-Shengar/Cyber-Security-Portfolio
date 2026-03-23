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
9. Selected the first whitespace and used `Ctrl + H` to open the "Find and Replace" page.

<img width="1919" height="1079" alt="Screenshot 2026-03-22 193440" src="https://github.com/user-attachments/assets/d3436a34-e706-4940-81b4-9911eeec2f33" />

10. Replaced one type of whitespace character with `0`.

<img width="1919" height="1079" alt="Screenshot 2026-03-22 193503" src="https://github.com/user-attachments/assets/5628cade-8f6a-4e2a-9de9-5c182e84250f" />

10. Closed the tab and it shown all converted whitespaces with `0` and along with that remaning hiddien whitespaces.

<img width="1919" height="1078" alt="Screenshot 2026-03-22 193611" src="https://github.com/user-attachments/assets/ee36bca2-2491-40ec-9595-79046ef48922" />

11. Double clicked on the next whitespace.


10. Then replaced another type with `1` using a text editor.
11. This conversion resulted in a sequence of **binary digits (0s and 1s)**.

<img width="1919" height="1079" alt="Screenshot 2026-03-22 193939" src="https://github.com/user-attachments/assets/831708db-cce4-4689-a6d5-6100cfda148d" />

12. Copied the binary data and opened **CyberChef**.

<img width="1919" height="1079" alt="Screenshot 2026-03-22 194325" src="https://github.com/user-attachments/assets/32ba60e9-8543-4c9e-a1e9-b2a76db34483" />

13. Applied the **From Binary** operation or used the **Magic** function to decode the data.

<img width="1919" height="1079" alt="Screenshot 2026-03-22 194345" src="https://github.com/user-attachments/assets/8a6d1403-9d7c-4eda-b08c-2b26db8973c7" />

14. The decoded output revealed readable text containing the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **whitespace steganography and binary decoding**.

Although the file appeared empty, it contained hidden data encoded using different whitespace characters. By identifying and converting these invisible characters into binary values, I was able to reconstruct the encoded data. Decoding the binary data revealed the flag. This challenge highlights how even invisible characters can be used to conceal information.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
