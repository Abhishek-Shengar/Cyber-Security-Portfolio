# Day 27 – picoCTF Forensics Challenge

## Challenge Name
WhitePages

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** John Hammond  

I stopped using YellowPages and moved onto WhitePages... but the page they gave me is all blank!

Download Link: https://challenge-files.picoctf.net/c_fickle_tempest/ab5453de03105a8aab9c68b0b46e66a4fe0a781c3915ab519f7fab31b3ce6894/whitepages.txt

---

## Objective
To analyze a seemingly empty text file and recover hidden information encoded using whitespace characters.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- Text Editor
- CyberChef

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/ab5453de03105a8aab9c68b0b46e66a4fe0a781c3915ab519f7fab31b3ce6894/whitepages.txt
```
