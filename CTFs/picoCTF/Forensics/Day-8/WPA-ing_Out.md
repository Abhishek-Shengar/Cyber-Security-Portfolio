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

Download Link: https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap

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
3. Downloaded the packet capture file using:
```bash
wget https://artifacts.picoctf.net/c/41/wpa-ing_out.pcap
```
4. Verified the file type:
```bash
file wpa-ing_out.pcap
```

<img width="1919" height="1079" alt="Screenshot 2026-02-10 172247" src="https://github.com/user-attachments/assets/9e433cab-6afb-40b7-95e0-6c7a8b2281c6" />

5. Confirmed that the file was a PCAP (wireless packet capture) file.
6. Based on the provided hint, identified that aircrack-ng could be used to crack WPA/WPA2 passwords from captured handshakes.
7. Located the rockyou.txt wordlist in the directory:
```bash
cd /usr/share/wordlists/
```
8. Used aircrack-ng with the wordlist to attempt cracking the wireless password:
```bash
aircrack-ng wpa-ing_out.pcap -w /usr/share/wordlists/rockyou.txt
```

<img width="1919" height="1076" alt="Screenshot 2026-02-10 175228" src="https://github.com/user-attachments/assets/b2e5bfda-b103-43ef-aa88-360272efeea7" />

9. Aircrack-ng analyzed the capture file, detected a valid WPA handshake, and began testing passwords from the wordlist.
10. After processing, aircrack-ng displayed:
```bash
KEY FOUND! [ <Password> ]
```

<img width="1919" height="1077" alt="Screenshot 2026-02-10 172937" src="https://github.com/user-attachments/assets/ade0ae92-3211-4355-a89a-4cc162e656cf" />

11. Extracted the discovered password.
12. Formatted the password according to the challenge requirement:
```bash
picoCTF{<Password>}
```
13. Submitted the formatted value as the flag.

---

## Flag (Masked)
picoCTF{***************}

---

## Summary
This challenge demonstrated **wireless forensics and WPA/WPA2 password cracking**.

By analyzing a wireless packet capture containing a valid handshake and using a common password wordlist, I was able to recover the network key. This challenge highlighted how weak or reused passwords can compromise wireless network security and emphasized the importance of strong, unique credentials.

---

📌 *All activities were performed in a legal and controlled CTF environment for educational purposes only.*
