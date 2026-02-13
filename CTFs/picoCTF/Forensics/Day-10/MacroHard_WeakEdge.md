# Day 10 – picoCTF Forensics Challenge

## Challenge Name
MacroHard WeakEdge

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** madStacks  

I've hidden a flag in this file. Can you find it?

File: Forensics_is_fun.pptm  

Download Link: https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm

---

## Objective
To analyze a macro-enabled PowerPoint file and locate hidden data within its internal file structure.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `unzip`
- `cat`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file using:
```bash
wget https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm
```
4. Verified the file type:
```bash
file Forensics_is_fun.pptm
```

<img width="1919" height="1067" alt="Screenshot 2026-02-12 233445" src="https://github.com/user-attachments/assets/07fce99c-923d-4775-8a3f-6aeb697e2265" />

5. Confirmed that the .pptm file is a Microsoft PowerPoint macro-enabled document, which internally uses a ZIP-based structure (Office Open XML format).
6. Extracted the file contents using:
```bash
unzip Forensics_is_fun.pptm
```

<img width="1919" height="1077" alt="Screenshot 2026-02-12 233735" src="https://github.com/user-attachments/assets/6c4b0c74-277a-40da-909c-704ca75593fd" />

7. Observed multiple folders including:
```bash
ppt/
```
8. Navigated into the PowerPoint internal directory structure:
```bash
cd ppt/slideMasters/
```
9. Identified a suspicious file named:
```bash
hidden
```
10. Read the contents of the hidden file:
```bash
cat hidden
```

<img width="1919" height="1072" alt="Screenshot 2026-02-12 235721" src="https://github.com/user-attachments/assets/28547292-e4ee-489f-8456-ec5551f8a2f4" />

11. The file contained encoded text.
12. Based on the structure and character set, recognized the data as Base64-encoded.
13. Copied the encoded string and opened CyberChef.

<img width="1919" height="969" alt="Screenshot 2026-02-13 192150" src="https://github.com/user-attachments/assets/c7f97a92-dcaa-4f04-ba74-b88eb828b37b" />

14. Applied the From Base64 decoding operation.
15. The decoded output revealed the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **Office document forensics and hidden data extraction**.

Although the file appeared to be a standard PowerPoint document, it was internally structured as a ZIP archive. By extracting its contents and inspecting the internal directory structure, I discovered a hidden file containing Base64-encoded data. Decoding the data revealed the flag. This challenge highlights the importance of analyzing file structures rather than relying solely on file extensions.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
