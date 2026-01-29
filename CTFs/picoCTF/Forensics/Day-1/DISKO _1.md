# Day 1 – picoCTF Forensics Challenge

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
3. Downloaded the compressed disk image using `wget`:
```bash
wget https://artifacts.picoctf.net/c/538/disko-1.dd.gz
```

<img width="1919" height="1079" alt="Screenshot 2026-01-29 222535" src="https://github.com/user-attachments/assets/28517a0b-a090-4522-8dbd-33b42d3abdef" />

4. After downloading, verified the file type:
```bash
file disko-1.dd.gz
```
5. Decompressed the disk image using gunzip:
```bash
gunzip disko-1.dd.gz
```
6. This produced the raw disk image file:
```bash
disko-1.dd
```
7. Checked the file type of the disk image:
```bash
file disko-1.dd
```

<img width="1919" height="1079" alt="Screenshot 2026-01-29 223058" src="https://github.com/user-attachments/assets/c5c23180-06e7-4910-9fa4-4e958ae8862e" />

8. Since the challenge was introductory, began analysis by searching for readable strings within the disk image.
9. Extracted human-readable strings from the disk image:
```bash
strings disko-1.dd
```
10. Filtered the output to search specifically for the picoCTF flag format:
```bash
strings disko-1.dd | grep picoCTF
```
11. The command returned a matching string containing the flag.

<img width="1919" height="1079" alt="Screenshot 2026-01-29 223408" src="https://github.com/user-attachments/assets/b5628339-689c-4e07-966f-c46d68ce77fc" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge introduced **basic disk image forensics**.

By downloading and decompressing the disk image, I analyzed its contents using simple string extraction techniques. Searching for human-readable data revealed the embedded flag. This challenge demonstrated how sensitive information can remain recoverable from disk images even without the use of advanced forensic tools.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*

