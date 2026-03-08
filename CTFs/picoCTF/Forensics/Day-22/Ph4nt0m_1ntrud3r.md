# Day 22 – picoCTF Forensics Challenge

## Challenge Name
Ph4nt0m 1ntrud3r

## Category
Forensics

## Difficulty
Easy

## Description / Problem Statement
**Author:** Prince Niyonshuti N.

A digital ghost has breached my defenses, and my sensitive data has been stolen! Your mission is to uncover how this phantom intruder infiltrated the system and retrieve the hidden flag.

To solve this challenge, analyze the provided PCAP file and track down the attack method by examining the network traffic.

Download Link: https://challenge-files.picoctf.net/c_verbal_sleep/a16868557f2510da0f9614e00e69950868489749884fd7db5a3247937eabe7bc/myNetworkTraffic.pcap

---

## Objective
To analyze network traffic in a PCAP file and reconstruct encoded data transmitted by an attacker.

---

## Tools / Commands Used
- Linux Terminal
- `wget`
- `file`
- `wireshark`
- CyberChef

---

## Methodology

1. Copied the download link from the challenge page.
2. Opened a terminal in **Linux**.
3. Downloaded the PCAP file:
```bash
wget https://challenge-files.picoctf.net/c_verbal_sleep/a16868557f2510da0f9614e00e69950868489749884fd7db5a3247937eabe7bc/myNetworkTraffic.pcap
```

<img width="1919" height="1079" alt="Screenshot 2026-03-07 093731" src="https://github.com/user-attachments/assets/16b7162f-c6bd-489b-a631-af4548081ce5" />

<img width="1919" height="1079" alt="Screenshot 2026-03-07 093817" src="https://github.com/user-attachments/assets/7496ea53-55dd-49fe-90d0-ed67e7f52cbe" />

<img width="1919" height="1079" alt="Screenshot 2026-03-07 095516" src="https://github.com/user-attachments/assets/b61aae11-2d83-4066-a588-d2f5f0d856a9" />

<img width="1910" height="872" alt="Screenshot 2026-03-08 233615" src="https://github.com/user-attachments/assets/e57450ce-098f-4045-8507-0f945f4e4be8" />

<img width="1919" height="1079" alt="Screenshot 2026-03-07 100850" src="https://github.com/user-attachments/assets/1cba37be-a100-472d-b645-e697d2b40a18" />

<img width="1919" height="966" alt="Screenshot 2026-03-07 100551" src="https://github.com/user-attachments/assets/0ab37644-a6c7-4795-a4a2-2d8209f50587" />

