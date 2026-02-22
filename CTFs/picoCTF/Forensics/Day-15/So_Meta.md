# Day 15 – picoCTF Forensics Challenge

## Challenge Name
So Meta

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Kevin Cooper / Danny  

Find the flag in this picture.

Download Link:  
https://challenge-files.picoctf.net/c_fickle_tempest/010f805d3d59e58913240f26904349f886a0ee71c205d46185ada895377818af/pico_img.png

---

## Objective
To analyze an image file for hidden metadata or embedded readable content and recover the flag.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `strings`
- `grep`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.

---

3. Downloaded the image file:

```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/010f805d3d59e58913240f26904349f886a0ee71c205d46185ada895377818af/pico_img.png
```



