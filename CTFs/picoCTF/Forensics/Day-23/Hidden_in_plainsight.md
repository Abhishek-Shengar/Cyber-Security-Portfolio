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

6. Since the challenge suggested hidden data inside the image, examined the image metadata using `exiftool`:
```bash
exiftool img.jpg
```
7. Observed a Base64 encoded string in the Comment metadata field.
8. Copied the encoded data and saved it into a text file:
```bash
nano flagclue.txt
```

<img width="1919" height="1079" alt="Screenshot 2026-03-10 231311" src="https://github.com/user-attachments/assets/78d46527-4871-463b-a564-ad411dae4bba" />

9. Pasted the copied encoded data into the file and saved it (Ctrl + O, press Enter) and exited the editor (Ctrl + X).

<img width="1919" height="1079" alt="Screenshot 2026-03-10 233716" src="https://github.com/user-attachments/assets/945511f5-0826-43a0-87af-489013dd344a" />

10. Decoded the encrypted message with command:
```bash
base64 -d flgclue.txt
```
11. The decoded output revealed another encoded string associated with steghide decoded text.
12. Copied this newly revealed encoded string and saved it into another file:
```bash
nano flagclue2.txt
```

<img width="1919" height="1076" alt="Screenshot 2026-03-14 230241" src="https://github.com/user-attachments/assets/c83fff71-fddb-47d7-b063-8118ad4c2239" />

13. Pasted the encoded data, saved the file (Ctrl + O, Enter) and exited (Ctrl + X).

<img width="1919" height="1079" alt="Screenshot 2026-03-10 231530" src="https://github.com/user-attachments/assets/443756e5-e077-4273-ba86-9fb4d9614542" />

14. Decoded the second encoded string:
```bash
base64 -d flagclue2.txt
```
15. The decoded output revealed a **passphrase** for extracting hidden data embedded inside the image.

<img width="1919" height="1078" alt="Screenshot 2026-03-14 230323" src="https://github.com/user-attachments/assets/c867a2c1-b627-4d4b-9f44-61c4b54c8c8f" />

16. Suspected that the image might contain steganographically hidden data.
17. Used the `steghide` tool to extract the hidden content from the image:
```bash
steghide extract -sf img.jpg
```
18. When prompted, entered the previously decoded passphrase.

<img width="1919" height="1079" alt="Screenshot 2026-03-10 234245" src="https://github.com/user-attachments/assets/1ea7dcff-5554-42b8-be34-873048e475dc" />

19. The extraction process revealed a hidden file containing the flag.

---

## Flag (Masked)
picoCTF{***************}

---

---

## Summary

This challenge demonstrated **image metadata analysis, layered Base64 decoding, and steganography extraction**.

Although the image initially appeared ordinary, hidden information was stored within its metadata. By analyzing the metadata with `exiftool`, I discovered Base64 encoded strings that required multiple decoding steps. The decoded output revealed a passphrase, which was then used with `steghide` to extract hidden data embedded inside the image. This challenge highlights how attackers may combine metadata concealment and steganography to hide sensitive information.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*






