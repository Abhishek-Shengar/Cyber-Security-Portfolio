<img width="1919" height="1079" alt="Screenshot 2026-01-30 184315" src="https://github.com/user-attachments/assets/0c390f21-5246-4ebd-8d29-99c41439222e" /># Day 2 – picoCTF Forensics Challenge

## Challenge Name
Enhance!

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

Download this image file and find the flag.

Download Link: https://artifacts.picoctf.net/c/100/drawing.flag.svg

---

## Objective
To analyze an SVG image file and locate hidden information using basic forensic inspection and string analysis techniques.

---

## Tools / Techniques Used
- Linux Terminal
- File type analysis
- String extraction
- Pattern searching within files

---

## Methodology

1. Copied the image file download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the SVG image file using a command-line download utility.
```bash
wget https://artifacts.picoctf.net/c/100/drawing.flag.svg
```
4. Verified the file type to confirm that it was an SVG (Scalable Vector Graphics) file.
```bash
file drawing.flag.svg
```

<img width="1919" height="1079" alt="Screenshot 2026-01-30 183737" src="https://github.com/user-attachments/assets/84f5d3b8-e4c7-4f1d-9497-07d1da7ed469" />

5. Attempted an initial search for the picoCTF flag pattern within the file using string filtering techniques.
6. The search returned no direct matches, indicating the flag was not stored as a single continuous string.
```bash
strings drawing.flag.svg | grep pico
```
7. Extracted all human-readable strings from the SVG file.
8. Observed that the output contained a large amount of SVG and XML markup.
```bash
strings drawing.flag.svg
```

<img width="1919" height="1079" alt="Screenshot 2026-01-30 183916" src="https://github.com/user-attachments/assets/b382e5d8-9ddd-4167-9113-d34eea37e894" />

9. Noticed repeated use of `<tspan>` elements, which are used in SVG files to store individual characters or text segments.
10. Filtered the extracted strings to focus specifically on these `<tspan>` elements.
```bash
strings drawing.flag.svg | grep tspan
```
11. Carefully analyzed the output and identified individual characters stored between SVG tags.
12. Manually reconstructed the flag by combining these characters in the correct sequence.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge focused on **forensic analysis of an SVG image file**.

By extracting and analyzing human-readable strings from the SVG file, I identified that the flag was distributed across multiple text elements. Carefully reviewing and reconstructing these characters allowed me to recover the full flag. This challenge demonstrated how image files—especially vector graphics—can conceal sensitive information within their underlying structure.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
