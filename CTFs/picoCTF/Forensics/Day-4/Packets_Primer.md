# Day 4 – picoCTF Forensics Challenge

## Challenge Name
Packets Primer

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** LT ‘syreal’ Jones  

Download the packet capture file and use packet analysis software to find the flag.

Download Link:
https://artifacts.picoctf.net/c/196/network-dump.flag.pcap

---

## Objective
To analyze a packet capture (PCAP) file using network forensics tools and extract hidden information from captured network traffic.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- Wireshark (Packet Analysis Tool)

---

## Methodology

1. Copied the packet capture download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the packet capture file using:
```bash
wget https://artifacts.picoctf.net/c/196/network-dump.flag.pcap
```
4. Verified the file type to confirm it was a packet capture file:
```bash
file network-dump.flag.pcap
```
5. Confirmed that the file was a PCAP (packet capture) file.
6. Opened the packet capture file using Wireshark:
```bash
wireshark network-dump.flag.pcap
```

<img width="1919" height="1079" alt="Screenshot 2026-02-05 231135" src="https://github.com/user-attachments/assets/1c62d01b-61d2-49eb-80c1-7e3c2358aa23" />

7. Wireshark launched and displayed all captured network packets.
8. Carefully inspected the packets and observed readable ASCII text in the packet details pane alongside the hexadecimal data.

<img width="1919" height="1079" alt="Screenshot 2026-02-05 231205" src="https://github.com/user-attachments/assets/d1ca8ec8-d0e2-4c3b-a417-7e168a5cac69" />

9. Noticed characters resembling: p i c o { ... } indicating the presence of the picoCTF flag spread across packets.
10. Right-clicked on the relevant packet containing readable text.
11. Selected Follow → TCP Stream to reconstruct the full communication stream.

<img width="1919" height="1079" alt="Screenshot 2026-02-05 231457" src="https://github.com/user-attachments/assets/a16e1542-440a-4d99-a99c-bcac4e8964d2" />

12. The reconstructed TCP stream displayed the flag with spaces between each character.
13. Manually removed the spaces to reconstruct the complete flag.

<img width="1919" height="1079" alt="Screenshot 2026-02-05 231408" src="https://github.com/user-attachments/assets/e31bcc7e-d67e-4207-85e9-bb9bf7083e62" />




