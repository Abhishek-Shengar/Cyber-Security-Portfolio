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
```
4. Verified the file type:
```bash
file Forensics_is_fun.pptm
```
5. Confirmed that the .pptm file is a Microsoft PowerPoint macro-enabled document, which internally uses a ZIP-based structure (Office Open XML format).
6. Extracted the file contents using:
```bash
unzip Forensics_is_fun.pptm
```
7. Listed the extracted directories and files:
```bash
ls
```
8. Observed multiple folders including:
```bash
ppt/
```
9. Navigated into the PowerPoint internal directory structure:
```bash
cd ppt/slideMasters/
```
10. Identified a suspicious file named:
```bash
hidden
```
11. Read the contents of the hidden file:
```bash
cat hidden
```
12. The file contained encoded text.
13. Based on the structure and character set, recognized the data as Base64-encoded.
14. Copied the encoded string and opened CyberChef.
15. Applied the From Base64 decoding operation.

