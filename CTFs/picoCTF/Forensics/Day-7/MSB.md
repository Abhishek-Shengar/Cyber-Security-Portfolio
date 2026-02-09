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

Download Link:  
https://artifacts.picoctf.net/c/307/Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisada.flag.png

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

---

3. Based on the challenge description, noted that:
   - The image passed **LSB (Least Significant Bit)** analysis
   - Visual artifacts suggested data might be hidden using **MSB (Most Significant Bit)** manipulation

---

4. Used an online steganography analysis tool (StegOnline) to further inspect the image.
5. Uploaded the PNG file to the tool.

---

6. Selected the **Extract Files/Data** option to analyze embedded data.
7. In the bit-plane selection section, focused on the **7th bit plane** (Most Significant Bit).
8. Enabled extraction for all color channels:
   - Red (R)
   - Green (G)
   - Blue (B)

---

9. Executed the extraction process.
10. The tool produced extracted data from the image.

---

11. Downloaded the extracted data and opened it using a text editor.
12. Searched within the extracted content for the picoCTF flag pattern.
13. Identified the flag within the extracted data.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated **image steganography using Most Significant Bit (MSB) manipulation**.

Although the image did not reveal hidden data through traditional LSB analysis, examining the MSB bit planes exposed concealed information. By extracting and analyzing the MSB data across all color channels, I was able to recover the hidden flag. This challenge highlighted that steganographic data can be hidden in less common bit planes and requires deeper analysis beyond standard techniques.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*

