# Day 13 – picoCTF Forensics Challenge

## Challenge Name
extensions

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Sanjay C / Danny  

This is a really weird text file. Can you find the flag?  
Get the flag from TXT.

Download Link:  
https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt

---

## Objective
To identify mismatched file extensions and recover hidden data by analyzing the true file type.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `eog` (Eye of GNOME Image Viewer)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt
```
4. Verified the file type:
