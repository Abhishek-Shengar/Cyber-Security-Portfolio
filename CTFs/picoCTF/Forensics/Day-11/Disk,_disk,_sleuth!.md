# Day 11 – picoCTF Forensics Challenge

## Challenge Name
Disk, disk, sleuth!

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** syreal  

Use `srch_strings` from The Sleuth Kit and some terminal-fu to find a flag in this disk image.

File: dds1-alpine.flag.img.gz  

Download Link: https://challenge-files.picoctf.net/c_wily_courier/8643b47c3c19e52e891a4684258e1d1cbb65094afa9cf81317b563004a739653/dds1-alpine.flag.img.gz

---

## Objective
To analyze a compressed disk image file and locate hidden data using string extraction techniques.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `gzip`
- `strings`
- `grep`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the compressed disk image:
```bash
wget https://challenge-files.picoctf.net/c_wily_courier/8643b47c3c19e52e891a4684258e1d1cbb65094afa9cf81317b563004a739653/dds1-alpine.flag.img.gz
```
4. Verified the file type:
```bash
file dds1-alpine.flag.img.gz
```
5. Confirmed that the file was a gzip-compressed disk image (not a ZIP file).
6. Decompressed the image file:
```bash
gzip -d dds1-alpine.flag.img.gz
```
7. This produced the raw disk image file:
```bash
dds1-alpine.flag.img
```
8. Based on the challenge hint referencing srch_strings (from The Sleuth Kit), used string extraction techniques to search for readable data within the disk image.
9. Extracted and filtered readable strings to search specifically for the picoCTF flag pattern:
```bash
strings dds1-alpine.flag.img | grep picoCTF
```


