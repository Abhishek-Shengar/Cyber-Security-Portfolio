# Day 3 – picoCTF Forensics Challenge

## Challenge Name
Lookey here

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones / Mubarak Mikail  

Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.

Download Link: https://artifacts.picoctf.net/c/124/anthem.flag.txt

---

## Objective
To analyze a large text file and locate hidden information using basic forensic string analysis techniques.

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

3. Downloaded the file using:
```bash
wget https://artifacts.picoctf.net/c/124/anthem.flag.txt
```
4. Verified the file type:
```bash
file anthem.flag.txt
```

<img width="1919" height="1078" alt="Screenshot 2026-01-31 141436" src="https://github.com/user-attachments/assets/b3ee0ee9-69a7-4293-8f79-82326cc1c35c" />

5. Extracted all human-readable strings from the file:
```bash
strings anthem.flag.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-01-31 141851" src="https://github.com/user-attachments/assets/23c0a52b-6160-4ea6-812f-d9aaf6eb5d66" />

6. Observed that the output was very large, making manual inspection inefficient.
7. Filtered the extracted strings to search specifically for the picoCTF flag pattern:
```bash
strings anthem.flag.txt | grep pico
```

<img width="1919" height="1079" alt="Screenshot 2026-01-31 141543" src="https://github.com/user-attachments/assets/d5c098dd-2807-4f9b-a466-4b457d461b7b" />

8. The filtered output returned the flag embedded within the large dataset.

---

## Flag
picoCTF{***************}

---

## Summary
This challenge demonstrated how sensitive information can be hidden inside **large volumes of data**.

By using string extraction and targeted pattern searching, I was able to efficiently locate the embedded flag without manually reviewing the entire file. This challenge highlighted the importance of automation and filtering techniques in digital forensics when dealing with large datasets.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
