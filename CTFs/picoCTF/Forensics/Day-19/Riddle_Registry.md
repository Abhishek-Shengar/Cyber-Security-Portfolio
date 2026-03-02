# Day 19 – picoCTF Forensics Challenge

## Challenge Name
Riddle Registry

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Prince Niyonshuti N.  

Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered.

Find the PDF file here: https://challenge-files.picoctf.net/c_amiable_citadel/85ff7059d0bc98abe4aa040e2dd70a342f9f9aaa8edd70ccba166efeb6249afa/confidential.pdf

---

## Objective
To analyze a PDF document and recover hidden information embedded within its metadata.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `exiftool`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://challenge-files.picoctf.net/c_amiable_citadel/85ff7059d0bc98abe4aa040e2dd70a342f9f9aaa8edd70ccba166efeb6249afa/confidential.pdf
```
4. Verified the file type:
```bash
file confidential.pdf
```

<img width="1919" height="1079" alt="Screenshot 2026-03-02 223335" src="https://github.com/user-attachments/assets/de2d324e-a357-4ea2-a829-6f03be32679b" />

5. Confirmed that the file was a PDF document.
6. Opened the PDF file to inspect its visible content but did not find any readable flag.
7. Suspected that the flag might be hidden within the document metadata.
8. Extracted the metadata using:
```bash
exiftool confidential.pdf
```

<img width="1919" height="1079" alt="Screenshot 2026-03-02 224817" src="https://github.com/user-attachments/assets/048b557d-c5d6-4128-8a3e-e273f90d5deb" />

9. Observed that the **Author field** contained an encoded string ending with `=` which suggested **Base64 encoding**.
10. Copied the encoded string and opened **CyberChef**.
11. Applied the **From Base64** operation to decode the string.
12. The decoded output revealed the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **PDF metadata analysis and Base64 decoding techniques**.

Although the document appeared to contain meaningless text, the hidden flag was embedded within the metadata fields. By extracting metadata using `exiftool`, I discovered a Base64-encoded string stored in the Author field. Decoding the string revealed the flag. This challenge highlights the importance of examining document metadata during forensic investigations.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
