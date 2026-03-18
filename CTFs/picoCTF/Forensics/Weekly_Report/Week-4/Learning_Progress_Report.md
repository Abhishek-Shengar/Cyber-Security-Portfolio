# Week 04 – Forensics Learning Progress Report  
*picoCTF Forensics Track*

---

## Overview

This report summarizes my **Week 04 progress in Digital Forensics** while solving hands-on challenges on the picoCTF platform.

During this week, I focused on **metadata analysis, steganography extraction, network packet analysis, and multi-layer decoding techniques**. These challenges required combining multiple forensic methods such as Base64 decoding, OCR extraction, steghide usage, and PCAP traffic inspection.

All challenges were solved in a **legal and controlled CTF environment for educational purposes only**.

---

## Challenges Completed (Week 04)

| Day | Challenge Name | Primary Focus Area |
|-----|---------------|-------------------|
| Day 19 | Riddle Registry | PDF Metadata Analysis |
| Day 20 | RED | PNG Steganography (zsteg) |
| Day 21 | Flag in Flame | Multi-layer Encoding (Base64 → Image → OCR → Hex) |
| Day 22 | Ph4nt0m 1ntrud3r | Network Traffic Analysis (PCAP) |
| Day 23 | Hidden in plainsight | Metadata + Steganography (exiftool + steghide) |
| Day 24 | information | Image Metadata Extraction |

---

## Skills & Techniques Learned

### Metadata Forensics
- Extracting metadata using `exiftool`
- Identifying hidden data in fields like **Author, Comment, License**
- Recognizing encoded data stored in metadata

---

### Multi-layer Encoding & Decoding
- Handling multiple layers of encoding:
  - Base64 → Image → OCR → Hex
- Identifying encoding patterns based on structure and character sets
- Using CyberChef and CLI tools for decoding

---

### Image Steganography
- Detecting hidden data in PNG images using `zsteg`
- Extracting embedded content using `steghide`
- Understanding how passphrases are used to protect hidden data

---

### Network Forensics (PCAP Analysis)
- Analyzing packet capture files using Wireshark
- Inspecting TCP payloads for hidden data
- Reconstructing fragmented encoded data across packets

---

### Data Extraction & Reconstruction
- Identifying fragmented or layered data
- Reassembling encoded segments into complete information
- Understanding attacker techniques for hiding data across multiple steps

---

## Tools Used

- **Linux (Kali Linux)**
- `wget`
- `file`
- `exiftool`
- `strings`
- `base64`
- `zsteg`
- `steghide`
- `tesseract`
- `wireshark`
- `nano`
- CyberChef

---

## Key Forensic Concepts Reinforced

- Metadata is a common place to hide sensitive data
- Multiple encoding layers are used to obfuscate information
- Images can contain both visible and hidden (steganographic) data
- Network traffic may carry encoded or fragmented payloads
- Forensic analysis often requires combining multiple techniques
- Proper tool selection is critical for efficient investigation

---

## Professional Development Observations

During Week 04, I improved my ability to:

- Analyze complex, multi-step forensic challenges
- Identify encoding techniques and hidden data patterns
- Combine multiple tools to solve layered problems
- Think like an attacker to understand data hiding techniques

These skills are highly relevant for roles such as:

- **SOC Analyst**
- **Digital Forensic Investigator**
- **Incident Responder**

---

## Learning Outcome (Week 04)

This week enhanced my understanding of **advanced forensic analysis**, especially in areas involving **multi-layer encoding, steganography, and network traffic inspection**. I developed a structured approach to solving complex challenges by breaking them into smaller steps and applying the appropriate tools.

---

## Next Steps (Week 05 Goals)

- Practice advanced disk forensics and memory analysis
- Explore automated forensic tools and scripting
- Improve speed in identifying encoding patterns
- Work on real-world forensic case studies
- Continue building structured and professional documentation

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical forensic challenges conducted in controlled environments.*
