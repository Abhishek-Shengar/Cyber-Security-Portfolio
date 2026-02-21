# Week 02 – Forensics Learning Progress Report  
*picoCTF Forensics Track*

---

## Overview

This report summarizes my **Week 02 progress in Digital Forensics** through hands-on picoCTF challenges.

During this week, I explored more advanced forensic techniques including:

- Image steganography (MSB analysis)
- Wireless packet cracking (WPA handshake)
- Recursive archive extraction
- Office document internal structure analysis
- Disk image investigation using string analysis
- Audio signal decoding (SSTV)

These challenges strengthened my ability to analyze different file formats, decode hidden data, and apply multiple forensic approaches depending on the scenario.

All challenges were solved in a **legal, controlled CTF environment for educational purposes only**.

---

## Challenges Completed (Week 02)

| Day | Challenge Name | Primary Focus Area |
|-----|---------------|-------------------|
| Day 7 | MSB | Image Steganography (Bit-Plane Analysis) |
| Day 8 | WPA-ing Out | Wireless Forensics (WPA Handshake Cracking) |
| Day 9 | Matryoshka doll | Recursive Archive Extraction |
| Day 10 | MacroHard WeakEdge | Office File Structure & Base64 Decoding |
| Day 11 | Disk, disk, sleuth! | Disk Image String Analysis |
| Day 12 | m00nwalk | Audio Forensics (SSTV Decoding) |

---

## Skills & Techniques Learned

### Image Steganography & Bit-Level Analysis
- Understanding Most Significant Bit (MSB) manipulation
- Extracting hidden data from image bit planes
- Identifying visual artifacts as steganographic indicators
- Analyzing hidden data across RGB channels

---

### Wireless Forensics
- Understanding WPA/WPA2 handshake captures
- Performing offline dictionary attacks using wordlists
- Cracking weak wireless passwords
- Recognizing risks of reused credentials

---

### Recursive Archive Analysis
- Identifying nested archive structures
- Extracting layered compressed files
- Recognizing archive recursion patterns
- Using automation to reduce repetitive extraction tasks

---

### Office Document Forensics
- Understanding that `.pptm` files are ZIP-based (Office Open XML)
- Inspecting internal directory structures
- Locating hidden embedded files
- Decoding Base64-encoded content

---

### Disk Image Investigation
- Decompressing disk images
- Extracting readable strings from raw images
- Using pattern-based filtering to locate flags
- Understanding filesystem artifact persistence

---

### Audio & Signal Forensics
- Identifying SSTV (Slow Scan Television) encoded audio
- Converting audio signals into images
- Understanding how non-textual data can be transmitted via sound
- Reconstructing hidden content from waveform data

---

## Tools Used

- **Linux (Kali Linux)**
- `strings`
- `grep`
- `gzip`
- `unzip`
- `tar`
- `aircrack-ng`
- `foremost`
- `sstv`
- `eog`
- CyberChef
- StegOnline
- Wireshark (previous week reference)

---

## Key Forensic Concepts Reinforced

- File extensions cannot be trusted — verify file signatures
- Hidden data may exist in non-obvious bit planes
- Audio files can carry encoded visual information
- Weak passwords remain a major real-world vulnerability
- Archive recursion is a common CTF obfuscation technique
- Disk images can contain recoverable readable artifacts
- Multiple forensic approaches may solve the same problem

---

## Professional Development Observations

During Week 02, I began thinking more like a:

- SOC Analyst
- Digital Forensic Investigator
- Incident Responder

Instead of relying on a single tool, I evaluated:
- File structure
- Encoding patterns
- Network artifacts
- Embedded content
- Signal characteristics

This improved my analytical thinking and tool-selection strategy.

---

## Learning Outcome (Week 02)

This week significantly expanded my forensic exposure across:

- Image analysis
- Wireless security
- Audio decoding
- Disk artifact extraction
- Office document inspection

I developed stronger confidence in identifying hidden data across different digital mediums and applying the correct forensic technique for each scenario.

---

## Next Steps (Week 03 Goals)

- Explore advanced disk forensics (The Sleuth Kit tools)
- Practice deeper network traffic analysis
- Learn memory forensics basics
- Study steganography detection methods
- Continue structured forensic documentation

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical forensic challenges conducted in controlled environments.*
