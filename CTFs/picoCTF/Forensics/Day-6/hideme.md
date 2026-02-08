# Day 6 – picoCTF Forensics Challenge

## Challenge Name
hideme

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Geoffrey Njogu  

Every file gets a flag.

The SOC analyst saw one image being sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye here.

Download Link: https://artifacts.picoctf.net/c/261/flag.png

---

## Objective
To analyze an image file and identify hidden embedded data using file carving and extraction techniques.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `binwalk`
- File Manager (Thunar)
- Image Viewer

---

## Methodology

1. Copied the image download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the image file using:
```bash
wget https://artifacts.picoctf.net/c/261/flag.png
```
4. Verified the file type:
```bash
file flag.png
```
5. Confirmed that the file was a PNG image.

<img width="1919" height="1079" alt="Screenshot 2026-02-08 214323" src="https://github.com/user-attachments/assets/25078dea-ebd1-4ce4-bbe8-227b37f2b828" />

6. Suspecting hidden data inside the image, analyzed the file using binwalk:
```bash
binwalk flag.png
```
7. Binwalk output indicated the presence of an embedded ZIP archive within the PNG file.
8. Extracted the embedded contents using binwalk with extraction enabled:
```bash
binwalk --run-as=root -e flag.png
```

<img width="1919" height="1079" alt="Screenshot 2026-02-08 214738" src="https://github.com/user-attachments/assets/eaa989bc-047e-4710-829c-cbe2cdc2e9ea" />

9. After extraction, a new directory named: _flag.png.extracted was created.
10. Listed the contents of the extracted directory: 
```bash
ls _flag.png.extracted
```
11. Navigated into the directory:
```bash
cd _flag.png.extracted
```
12. Observed a subdirectory named: secret
13. Navigated into the secret directory:
```bash
cd secret
```
14. Found another image file named flag.png.
15. Opened the extracted image file using the file manager:
```bash
thunar flag.png
```

<img width="1919" height="1079" alt="Screenshot 2026-02-08 215325" src="https://github.com/user-attachments/assets/cca5530c-a92d-4774-acc3-c133e5191faf" />

16. Double-clicked the image to view it.
17. The image displayed text containing the flag.

<img width="1919" height="1079" alt="Screenshot 2026-02-08 215345" src="https://github.com/user-attachments/assets/c72f70fd-d405-4d9c-87a2-9a395bef81d5" />

