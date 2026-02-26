# Day 16 – picoCTF Forensics Challenge

## Challenge Name
What Lies Within

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Julio / Danny  

There's something in the building. Can you retrieve the flag?

Download Link:  
https://challenge-files.picoctf.net/c_fickle_tempest/c0eec6af0f04316e2bdc4a9f095afd0e2d0121f5e543dbc4a65bb0038d72a993/buildings.png

---

## Objective
To analyze a PNG image for hidden steganographic data and recover the concealed flag.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `zsteg`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.

---

3. Downloaded the image file:

```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/c0eec6af0f04316e2bdc4a9f095afd0e2d0121f5e543dbc4a65bb0038d72a993/buildings.png
```
