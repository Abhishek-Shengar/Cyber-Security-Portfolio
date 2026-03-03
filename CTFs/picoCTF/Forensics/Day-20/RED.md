# Day 20 – picoCTF Forensics Challenge

## Challenge Name
RED

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Shuailin Pan (LeConjuror)  

RED, RED, RED, RED  

Download Link: https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png

---

## Objective
To analyze a PNG image for hidden steganographic data and recover the concealed flag.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `zsteg`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png
```
4. Verified the file type:
5. Confirmed that the file was a PNG image.
6. Based on the challenge title and category, suspected hidden steganographic data.
7. Used zsteg to analyze the image for hidden content:
8. The tool output revealed an encoded string embedded within one of the color channel bit planes.
9. The extracted string appeared to be Base64-encoded text.


