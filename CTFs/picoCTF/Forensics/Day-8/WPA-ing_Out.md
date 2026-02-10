# Day 8 – picoCTF Forensics Challenge

## Challenge Name
WPA-ing Out

## Category
Forensics

## Difficulty
Medium

## Description / Problem Statement
**Author:** MistressVampy  

I thought that my password was super-secret, but it turns out that passwords passed over the AIR can be CRACKED, especially if I used the same wireless network password as one in the rockyou.txt credential dump.

Use this PCAP file and the rockyou wordlist.  
The flag should be entered in the `picoCTF{XXXXXX}` format.

Download Link:  
https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap

---

## Objective
To analyze a wireless packet capture file and recover the WPA/WPA2 network password using a wordlist-based attack.

---

## Tools / Commands Used
- Linux Terminal (Kali Linux)
- `wget`
- `file`
- `aircrack-ng`
- `rockyou.txt` wordlist

---

## Methodology

1. Copied the PCAP download link from the challenge page.
2. Opened a terminal in **Kali Linux**.

---

3. Downloaded the packet capture file using:
```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```

```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```

```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```

```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```

```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```

```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```
