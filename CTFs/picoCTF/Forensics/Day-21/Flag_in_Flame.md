# Day 21 – picoCTF Forensics Challenge

## Challenge Name
Flag in Flame

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Prince Niyonshuti N.

The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within?

Download Link: https://challenge-files.picoctf.net/c_amiable_citadel/ade5acd5e8e7082fc52cbbb6b297da484b0656fa4ce51b3b923c9d2c0f4a93f7/logs.txt

---

## Objective
To analyze encoded log data and extract hidden information through multiple decoding and forensic analysis steps.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `strings`
- `base64`
- `tesseract`
- `cat`
- CyberChef

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the log file:
```bash
wget https://challenge-files.picoctf.net/c_amiable_citadel/ade5acd5e8e7082fc52cbbb6b297da484b0656fa4ce51b3b923c9d2c0f4a93f7/logs.txt
```
4. Verified the file type:
```bash
file logs.txt
```
5. Confirmed that the file contained large encoded text data.
6. Inspected the content and identified that the data appeared to be Base64 encoded.
7. Decoded the Base64 data and redirected the output into an image file:
```bash
strings logs.txt | base64 -d > flag.jpg
```
8. The decoded output generated an image file named flag.jpg.
9. Opened the image and observed encoded text embedded inside the image.
10. Used OCR to extract the text from the image:
