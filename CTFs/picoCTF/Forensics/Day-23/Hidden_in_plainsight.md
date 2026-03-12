# Day 23 – picoCTF Forensics Challenge

## Challenge Name
Hidden in plainsight

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Yahaya Meddy  

You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag.

Download Link: https://challenge-files.picoctf.net/c_amiable_citadel/0e679342e0fe04fa2efa860dda0923cba52108031ac4e1ab519df850c2764b5c/img.jpg

---

## Objective
To analyze a JPEG image and investigate hidden data embedded within the file.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file:
```bash
wget https://challenge-files.picoctf.net/c_amiable_citadel/0e679342e0fe04fa2efa860dda0923cba52108031ac4e1ab519df850c2764b5c/img.jpg
```
4. Checked the file type using the file command:
```bash
file img.jpg
```
5. Confirmed that the file was a JPEG image file.

<img width="1919" height="1079" alt="Screenshot 2026-03-10 225932" src="https://github.com/user-attachments/assets/b0159ead-0068-4d20-a647-294d601d254a" />

6. Used exiftool to analyze the file.
7. Found base64 encrypted data.
8. With the nano command stored in flagclue.txt file.

<img width="1919" height="1079" alt="Screenshot 2026-03-10 231311" src="https://github.com/user-attachments/assets/78d46527-4871-463b-a564-ad411dae4bba" />

<img width="1919" height="1079" alt="Screenshot 2026-03-10 233716" src="https://github.com/user-attachments/assets/945511f5-0826-43a0-87af-489013dd344a" />

<img width="1919" height="1077" alt="Screenshot 2026-03-10 235540" src="https://github.com/user-attachments/assets/aa0b2a4e-8bd9-47ee-900f-ee09b15d9c36" />

<img width="1919" height="1079" alt="Screenshot 2026-03-10 231530" src="https://github.com/user-attachments/assets/443756e5-e077-4273-ba86-9fb4d9614542" />

<img width="1919" height="1079" alt="Screenshot 2026-03-10 234245" src="https://github.com/user-attachments/assets/1ea7dcff-5554-42b8-be34-873048e475dc" />

