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

