# Day 18 – picoCTF Forensics Challenge

## Challenge Name
Secret of the Polyglot

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** syreal  

The Network Operations Center (NOC) of your local institution picked up a suspicious file. They are getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?

Download Link: https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf

---

## Objective
To analyze a suspicious file and extract hidden information by identifying and interpreting multiple file formats within the same file.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `mv`
- PDF Viewer
- Image Viewer

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf
```
5. The `file` command identified the file as a **PDF document**.

6. Opened the PDF file using a PDF viewer and observed that it contained **the second part of the flag**.

7. Based on the challenge hint indicating conflicting file types, suspected the file might be a **polyglot file** (a file valid as multiple formats).

8. Renamed the file extension from `.pdf` to `.jpg`.

9. Opened the renamed file using an image viewer.

10. The image displayed **the first part of the flag**.

11. Combined both parts to obtain the complete flag.

---

## Flag (Masked)

picoCTF{***************}

---

## Summary

This challenge demonstrated **polyglot file analysis and multi-format file interpretation**.

Although the file initially appeared to be a PDF document, it was actually a polyglot file that was also valid as a JPEG image. By opening the file in different formats, I was able to extract both parts of the flag. This challenge highlights the importance of examining files in multiple ways when conflicting file type information is encountered.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*

