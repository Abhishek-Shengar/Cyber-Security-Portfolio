# Day 5 – picoCTF Forensics Challenge

## Challenge Name
Redaction gone wrong

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Mubarak Mikail  

Now you DON’T see me.

This report has some critical data in it, some of which have been redacted correctly, while some were not.  
Can you find an important key that was not redacted properly?

Download Link: https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf

---

## Objective
To analyze a PDF document and recover sensitive information that was improperly redacted.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- File Manager (Thunar)
- PDF Viewer

---

## Methodology

1. Copied the PDF download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the PDF file using:
```bash
wget https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
```
4. Verified the file type:
```bash
file Financial_Report_for_ABC_Labs.pdf
```

<img width="1919" height="1079" alt="Screenshot 2026-02-07 183844" src="https://github.com/user-attachments/assets/f4a895e6-b451-49e7-a0b5-4ea100d504e8" />

5. Confirmed that the file was a PDF document.
6. Opened the file manager and accessed the PDF file.
7. Double-clicked the PDF to open it using the default PDF viewer.

<img width="1919" height="1079" alt="Screenshot 2026-02-07 184040" src="https://github.com/user-attachments/assets/89e5b8c3-268d-48da-a6cf-bf03bb883937" />

8. Observed that the document contained readable text along with black boxes, indicating redacted content.
9. Suspected that the redaction might have been performed visually rather than removing the underlying text.
10. Selected the entire document text using Ctrl + A.
11. Noticed that text underneath one of the black boxes became visible after selection.
12. Identified sensitive information that had not been properly redacted.

<img width="1919" height="1075" alt="Screenshot 2026-02-07 184014" src="https://github.com/user-attachments/assets/cb1c6b2e-eccc-45e8-9941-3addf0cd0a70" />

13. Extracted the visible hidden text, which contained the flag.




