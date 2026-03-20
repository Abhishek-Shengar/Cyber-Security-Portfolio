# Day 25 – picoCTF Forensics Challenge

## Challenge Name
Glory of the Garden

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** jedavis / Danny  

This file contains more than it seems.  
Get the flag from garden.jpg.

Download Link: https://challenge-files.picoctf.net/c_fickle_tempest/6013221da747114c37db29c554381dbe4bb4e746cf6bd880f9c3b5d0b495a823/garden.jpg

---

## Objective
To analyze a JPEG file and extract hidden textual data using efficient forensic techniques.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `strings`
- `grep`
- `thunar`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/6013221da747114c37db29c554381dbe4bb4e746cf6bd880f9c3b5d0b495a823/garden.jpg
```
4. Verified the file type:
```bash
file garden.jpg
```

---

## Flag (Masked)
picoCTF{***************}

---
