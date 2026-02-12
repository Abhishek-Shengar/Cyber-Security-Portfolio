# Day 10 – picoCTF Forensics Challenge

## Challenge Name
MacroHard WeakEdge

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** madStacks  

I've hidden a flag in this file. Can you find it?

File: Forensics_is_fun.pptm  

Download Link:  
https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm

---

## Objective
To analyze a macro-enabled PowerPoint file and locate hidden data within its internal file structure.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `unzip`
- `cd`
- `ls`
- `cat`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.

---

3. Downloaded the file using:
```bash
wget https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm

