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

Download Link:  
https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png

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

---

3. Downloaded the image file:

```bash
wget https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png
```



