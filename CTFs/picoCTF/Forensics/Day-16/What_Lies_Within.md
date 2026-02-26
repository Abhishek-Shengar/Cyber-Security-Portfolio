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

Download Link: https://challenge-files.picoctf.net/c_fickle_tempest/c0eec6af0f04316e2bdc4a9f095afd0e2d0121f5e543dbc4a65bb0038d72a993/buildings.png

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
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/c0eec6af0f04316e2bdc4a9f095afd0e2d0121f5e543dbc4a65bb0038d72a993/buildings.png
```
4. Verified the file type:
```bash
file buildings.png
```
5. Confirmed that the file was a PNG image (8-bit/color RGBA).
6. Based on the challenge name and category, suspected steganographic data hidden within the image.
7. Used zsteg, a tool designed to detect and extract hidden data from PNG images:
```bash
zsteg buildings.pn
```
8. The tool analyzed various bit planes and color channels.
9. Identified readable hidden data in one of the extracted outputs.
10. Extracted the flag from the revealed hidden text.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary

This challenge demonstrated **PNG steganography detection using bit-plane analysis**.

Although the image appeared normal visually, hidden data was embedded within its color channel bit planes. Using the `zsteg` tool, I was able to analyze the image structure and extract the concealed flag. This challenge highlights the importance of specialized steganography tools when investigating image-based data concealment.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
