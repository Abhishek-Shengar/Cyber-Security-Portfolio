# Day 9 – picoCTF Forensics Challenge

## Challenge Name
Matryoshka doll

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Susie / Pandu  

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?

Image: dolls.jpg  

Download Link: https://challenge-files.picoctf.net/c_wily_courier/feaddb84eaaa2f8d6b83bda9e7a9c46a86474361e095fea9ee3840873f3506b4/dolls.jpg

---

## Objective
To identify and extract recursively nested files hidden within an image file until the final embedded content is revealed.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `unzip`
- `ls`
- `cd`
- `cat`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file using:
```bash
wget https://challenge-files.picoctf.net/c_wily_courier/feaddb84eaaa2f8d6b83bda9e7a9c46a86474361e095fea9ee3840873f3506b4/dolls.jpg
```
4. Checked the file type:
```bash
file dolls.jpg
```
5. Although the file had a .jpg extension, the file command revealed that it was actually a ZIP archive.
6. Checked the file type:
```bash
unzip dolls.jpg
```
7. Listed the contents:
```bash
ls
```
8. Listed the contents:
```bash
base_images
```
9. Observed a directory named:
```bash
cd base_images
```
10. Found another file named 2_c.jpg, which again appeared to be a JPG file.
11. Verified and extracted it:
```bash
unzip 2_c.jpg
```
12. This revealed another nested base_images directory.
13. Repeated the same steps recursively:
```bash
cd base_images
unzip 3_c.jpg
cd base_images
unzip 4_c.jpg
```
14. Repeated the same steps recursively:
```bash
flag.txt
```
15. Viewed the contents of the file:
```bash
cat flag.txt
```
16. Viewed the contents of the file:






