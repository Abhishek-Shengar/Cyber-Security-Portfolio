# Day 12 – picoCTF Forensics Challenge

## Challenge Name
m00nwalk

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** Joon  

Decode this message from the moon.

File: message.wav  

Download Link:  
https://challenge-files.picoctf.net/c_fickle_tempest/67884a117da864fd93ca3cfc5d8b4d1aae71c84d7f3d2a89c1b5d0b3a19e0a71/message.wav

---

## Objective
To analyze an audio file and decode hidden image data transmitted using SSTV (Slow Scan Television) encoding.

---

## Tools / Commands Used
- Linux Terminal
- `file`
- `sstv`
- File Manager (Thunar)

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the audio file:
```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/67884a117da864fd93ca3cfc5d8b4d1aae71c84d7f3d2a89c1b5d0b3a19e0a71/message.wav
```
4. Verified the file type:
```bash
file message.wav
```

<img width="1919" height="1079" alt="Screenshot 2026-02-18 205020" src="https://github.com/user-attachments/assets/b878660c-57a0-4232-a4f2-c0b28fad0a0d" />

5. Confirmed that the file was a WAV audio file.
6. Based on the challenge description and observing the signal characteristics, identified that the audio contained an SSTV (Slow Scan Television) broadcast signal.
7. Used the SSTV decoding tool to extract the transmitted image:
```bash
sstv -d message.wav -o flag.png
```
- `-d` specifies the input audio file.
- `-o` specifies the output image file.
8. The decoding process generated a new file:
```bash
flag.png
```
9. Opened the image file:
```bash
thunar flag.png
```

<img width="1919" height="1077" alt="Screenshot 2026-02-18 210706" src="https://github.com/user-attachments/assets/019bb2e2-639d-43de-b0a3-0d0f541577cd" />

10. Viewed the image and identified the flag displayed within it.

<img width="1919" height="1076" alt="Screenshot 2026-02-18 211013" src="https://github.com/user-attachments/assets/25171831-36ab-48af-89b2-110fc7d6320c" />

---

## Flag
picoCTF{***************}

---

## Summary

This challenge demonstrated **audio forensics and SSTV signal decoding**.

The WAV file contained an SSTV-encoded image transmitted as an audio signal. By decoding the signal using an SSTV tool, I was able to reconstruct the hidden image and recover the flag. This challenge highlights how non-textual data, such as images, can be transmitted and concealed within audio signals.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
