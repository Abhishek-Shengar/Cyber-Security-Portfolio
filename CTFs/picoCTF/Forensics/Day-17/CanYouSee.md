# Day 17 – picoCTF Forensics Challenge

## Challenge Name
CanYouSee

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Mubarak Mikail  

How about some hide and seek?

Download Link: https://artifacts.picoctf.net/c_titan/130/unknown.zip

---

## Objective
To analyze a compressed file and recover hidden information from image metadata.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `unzip`
- `exiftool`
- CyberChef (Base64 decoding)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the compressed file:
```bash
wget https://artifacts.picoctf.net/c_titan/130/unknown.zip
```
