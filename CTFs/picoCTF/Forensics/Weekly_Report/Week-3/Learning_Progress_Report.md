# Week 03 – Forensics Learning Progress Report  
*picoCTF Forensics Track*

---

## Overview

This report summarizes my **Week 03 progress in Digital Forensics** while solving hands-on challenges on the picoCTF platform.

During this week, I worked on challenges involving **file signature verification, recursive archive extraction, image metadata inspection, steganography detection, and polyglot file analysis**. These tasks helped me better understand how attackers can hide data inside files and how forensic techniques can be used to uncover hidden artifacts.

All challenges were solved in a **legal and controlled CTF environment for educational purposes only**.

---

## Challenges Completed (Week 03)

| Day | Challenge Name | Primary Focus Area |
|-----|---------------|-------------------|
| Day 13 | extensions | File Signature vs File Extension |
| Day 14 | like1000 | Recursive Archive Extraction |
| Day 15 | So Meta | Embedded Strings in Image Files |
| Day 16 | What Lies Within | PNG Steganography (Bit-Plane Analysis) |
| Day 17 | CanYouSee | Image Metadata Analysis |
| Day 18 | Secret of the Polyglot | Polyglot File Analysis |

---

## Skills & Techniques Learned

### File Signature & Extension Analysis
- Verifying actual file type using `file`
- Detecting mismatches between file extensions and true file signatures
- Understanding how attackers disguise files by manipulating extensions

---

### Recursive Archive Analysis
- Identifying nested archive structures
- Extracting multi-layer compressed files
- Recognizing patterns in recursive archive challenges
- Using automation and alternative forensic approaches to extract data

---

### Image Forensics
- Extracting readable data from image binaries using `strings`
- Identifying hidden textual artifacts within image files
- Detecting embedded information without complex steganography

---

### Steganography Detection
- Analyzing PNG images for hidden bit-plane data
- Using tools like `zsteg` to detect concealed information
- Understanding how image color channels can store hidden messages

---

### Metadata Forensics
- Extracting metadata from images using `exiftool`
- Identifying encoded information hidden within metadata fields
- Decoding Base64-encoded data to recover hidden content

---

### Polyglot File Analysis
- Understanding polyglot files that function as multiple file types
- Opening the same file in different formats to reveal hidden data
- Recognizing how attackers can combine file formats to hide information

---

## Tools Used

- **Linux (Kali Linux)**
- `wget`
- `file`
- `strings`
- `grep`
- `tar`
- `unzip`
- `zsteg`
- `exiftool`
- `eog`
- CyberChef
- Linux command-line utilities

---

## Key Forensic Concepts Reinforced

- File extensions cannot always be trusted
- Metadata often contains hidden information
- Images can hide both textual and binary data
- Nested archives are commonly used for obfuscation
- Polyglot files can behave as multiple file formats
- Proper forensic analysis requires examining files from multiple perspectives

---

## Professional Development Observations

During Week 03, I strengthened my ability to:

- Investigate suspicious files systematically
- Choose appropriate forensic tools based on file type
- Analyze both visible data and hidden artifacts
- Think critically about how attackers conceal information

These skills closely align with responsibilities of **SOC analysts, incident responders, and digital forensic investigators**.

---

## Learning Outcome (Week 03)

This week expanded my forensic analysis capabilities by focusing on **file structure investigation, steganography detection, metadata extraction, and multi-format file interpretation**. The challenges reinforced the importance of examining digital evidence beyond its surface appearance.

---

## Next Steps (Week 04 Goals)

- Explore deeper disk image analysis
- Practice advanced steganography detection
- Analyze complex file formats and embedded data
- Continue building structured forensic documentation
- Expand knowledge of forensic investigation tools

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical forensic challenges conducted in controlled environments.*
