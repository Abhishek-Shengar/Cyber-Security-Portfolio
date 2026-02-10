# Day 7 – picoCTF Forensics Challenge

## Challenge Name
MSB

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

This image passes LSB statistical analysis, but we can't help but think there must be something to the visual artifacts present in this image.

Download Link: https://artifacts.picoctf.net/c/307/Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisada.flag.png

---

## Objective
To analyze an image for hidden data using **Most Significant Bit (MSB) steganography techniques** and extract concealed information.

---

## Tools / Techniques Used
- Image Viewer
- Online Steganography Analysis Tool (StegOnline)
- Bit-plane analysis
- Text searching within extracted data

---

## Methodology

1. Downloaded the PNG image file from the provided link.
2. Opened the image using an image viewer and observed that it appeared visually normal at first glance.

<img width="1919" height="1018" alt="Screenshot 2026-02-09 231931" src="https://github.com/user-attachments/assets/367f0582-786b-44a0-8ade-cc539de3f50d" />

3. Based on the challenge description, noted that:
   - The image passed **LSB (Least Significant Bit)** analysis.
   - Visual artifacts suggested data might be hidden using **MSB (Most Significant Bit)** manipulation.
4. Used an online steganography analysis tool (StegOnline) to further inspect the image.

<img width="1919" height="966" alt="Screenshot 2026-02-09 233635" src="https://github.com/user-attachments/assets/8d4e801c-d407-449e-b2ba-9fec8649bdda" />

5. Uploaded the PNG file to the tool.

<img width="1919" height="966" alt="Screenshot 2026-02-09 233701" src="https://github.com/user-attachments/assets/d3851b0f-ef18-4a0f-9e6b-fecb5a10e234" />

6. Selected the **Extract Files/Data** option to analyze embedded data.

<img width="1919" height="970" alt="Screenshot 2026-02-09 231738" src="https://github.com/user-attachments/assets/1314975f-0b78-4161-b515-8e18a92f98a9" />

7. In the bit-plane selection section, focused on the **7th bit plane** (Most Significant Bit).

<img width="1919" height="970" alt="Screenshot 2026-02-09 231815" src="https://github.com/user-attachments/assets/0c098805-4d87-4b5d-a9cb-4ee1ffd96761" />

8. Enabled extraction for all color channels:
   - Red (R)
   - Green (G)
   - Blue (B)

<img width="1919" height="963" alt="Screenshot 2026-02-09 231835" src="https://github.com/user-attachments/assets/0d5d0698-14f6-46be-9078-2a5bf808f680" />

9. Executed the extraction process.
10. The tool produced extracted data from the image.

<img width="1919" height="967" alt="Screenshot 2026-02-09 231906" src="https://github.com/user-attachments/assets/9cc6379c-84ac-4ac9-8755-cca6cd95ed01" />

11. Downloaded the extracted data and opened it using a text editor.

<img width="1919" height="974" alt="Screenshot 2026-02-09 232051" src="https://github.com/user-attachments/assets/0d45a1d6-938d-43e1-a57e-7c62a7d0ff32" />

12. Searched within the extracted content for the picoCTF flag pattern.
13. Identified the flag within the extracted data.

<img width="1919" height="974" alt="Screenshot 2026-02-09 232249" src="https://github.com/user-attachments/assets/d11ca578-1aa1-4653-8338-f5f504439eac" />

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated **image steganography using Most Significant Bit (MSB) manipulation**.

Although the image did not reveal hidden data through traditional LSB analysis, examining the MSB bit planes exposed concealed information. By extracting and analyzing the MSB data across all color channels, I was able to recover the hidden flag. This challenge highlighted that steganographic data can be hidden in less common bit planes and requires deeper analysis beyond standard techniques.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
