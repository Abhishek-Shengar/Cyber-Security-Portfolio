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
