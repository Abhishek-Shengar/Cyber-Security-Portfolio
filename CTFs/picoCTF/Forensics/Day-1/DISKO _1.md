# Day 27 – picoCTF Forensics Challenge

## Challenge Name
DISKO 1

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Darkraicg492  

Can you find the flag in this disk image?

Download Link: https://artifacts.picoctf.net/c/538/disko-1.dd.gz

---

## Objective
To analyze a disk image file and locate hidden information using basic digital forensics techniques.

---

## Tools / Commands Used
- Kali Linux
- `wget`
- `gunzip`
- `file`
- `strings`
- `grep`

---

## Methodology

1. Copied the disk image download link from the challenge page.
2. Opened a terminal in **Kali Linux**.

---

3. Downloaded the compressed disk image using `wget`:
```bash
wget https://artifacts.picoctf.net/c/538/disko-1.dd.gz
```
4. After downloading, verified the file type:
```bash
file disko-1.dd.gz
```
5. Decompressed the disk image using gunzip:
```bash
gunzip disko-1.dd.gz
```
6. This produced the raw disk image file:
```bash
disko-1.dd
```
7. Checked the file type of the disk image:
```bash
file disko-1.dd
```
8. Since the challenge was introductory, began analysis by searching for readable strings within the disk image.
9. Extracted human-readable strings from the disk image:
```bash
strings disko-1.dd
```
10. Extracted human-readable strings from the disk image:
```bash
strings disko-1.dd | grep picoCTF
```
11. The command returned a matching string containing the flag.


