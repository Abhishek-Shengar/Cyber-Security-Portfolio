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
