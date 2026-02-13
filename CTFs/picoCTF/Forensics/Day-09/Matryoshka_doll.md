# Day 9 – picoCTF Forensics Challenge

## Challenge Name
Matryoshka doll

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Susie / Pandu  

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?

Image: dolls.jpg  

Download Link: https://challenge-files.picoctf.net/c_wily_courier/feaddb84eaaa2f8d6b83bda9e7a9c46a86474361e095fea9ee3840873f3506b4/dolls.jpg

---

## Objective
To identify and extract recursively nested files hidden within an image file until the final embedded content is revealed.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `unzip`
- `cat`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file using:
```bash
wget https://challenge-files.picoctf.net/c_wily_courier/feaddb84eaaa2f8d6b83bda9e7a9c46a86474361e095fea9ee3840873f3506b4/dolls.jpg
```
4. Checked the file type:
```bash
file dolls.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-02-11 223035" src="https://github.com/user-attachments/assets/d6532eef-d011-4c9d-86a5-1723da005ff5" />

5. Although the file had a .jpg extension, the file command revealed that it was actually a ZIP archive.
6. Checked the file type:
```bash
unzip dolls.jpg
```
7. Listed the contents:
```bash
ls
```
8. Listed the contents:
```bash
base_images
```
9. Observed a directory named:
```bash
cd base_images
```
10. Found another file named 2_c.jpg, which again appeared to be a JPG file.
11. Verified and extracted it:
```bash
unzip 2_c.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-02-11 223618" src="https://github.com/user-attachments/assets/d0e4ea29-ed0d-40cc-b0f9-aa94de61542f" />

12. This revealed another nested base_images directory.
13. Repeated the same steps recursively:
```bash
cd base_images
unzip 3_c.jpg
cd base_images
unzip 4_c.jpg
```

<img width="1919" height="1079" alt="Screenshot 2026-02-11 223644" src="https://github.com/user-attachments/assets/44031e9a-d019-4a0c-9a85-7321eb8e106a" />

14. Repeated the same steps recursively:
```bash
flag.txt
```
15. Viewed the contents of the file:
```bash
cat flag.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-02-11 224106" src="https://github.com/user-attachments/assets/b368584f-87b5-411c-b439-fb91c046ee64" />

16. The contents displayed the flag.
---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated **recursive file extraction and disguised file formats**.

Although the file appeared to be a JPG image, it was actually a ZIP archive containing additional nested archives. By repeatedly extracting each layer—similar to opening Matryoshka dolls—I was able to reach the final embedded file containing the flag. This challenge highlights the importance of verifying file signatures rather than trusting file extensions.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
