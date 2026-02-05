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

Download Link: https://artifacts.picoctf.net/c/196/network-dump.flag.pcap

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



