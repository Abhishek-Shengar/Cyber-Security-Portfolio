# Week 01 – Forensics Learning Progress Report  
*picoCTF Forensics Track*

---

## Overview
This report summarizes my **Week 01 progress in Digital Forensics** while solving hands-on challenges on the picoCTF platform.

During this week, I focused on understanding **how digital evidence can hide within files, images, documents, and network traffic**. The challenges introduced core forensic concepts such as **disk image analysis, file carving, metadata inspection, packet capture analysis, and document redaction flaws**.

All challenges were solved in **legal, controlled environments** for educational purposes only.

---

## Challenges Completed (Week 01)

| Day | Challenge Name | Primary Focus Area |
|----|---------------|-------------------|
| Day 1 | DISKO 1 | Disk Image Analysis |
| Day 2 | Enhance! | SVG File & String Analysis |
| Day 3 | Lookey here | Large Dataset Inspection |
| Day 4 | Packets Primer | Network Traffic (PCAP) Analysis |
| Day 5 | Redaction gone wrong | PDF Document Forensics |
| Day 6 | hideme | Embedded File Extraction |

---

## Skills & Techniques Learned

###  Disk & File Analysis
- Working with raw disk image files
- Extracting readable data from binary files
- Understanding how data persists on storage media
- Recognizing common file formats and signatures

---

###  Image & Media Forensics
- Analyzing SVG files for hidden text elements
- Understanding how vector graphics store textual data
- Identifying embedded files inside image formats
- Extracting hidden content using file carving techniques

---

###  Document Forensics
- Analyzing PDF files for improperly redacted content
- Understanding the difference between visual redaction and secure redaction
- Recovering hidden text from document layers
- Recognizing common document handling mistakes

---

###  Network Forensics
- Analyzing PCAP files using packet analysis tools
- Identifying readable data within packet payloads
- Reconstructing communication using TCP stream analysis
- Understanding how sensitive data can leak through network traffic

---

###  Data Extraction & Filtering
- Using string extraction to analyze large datasets
- Applying pattern-based searching to reduce noise
- Efficiently locating hidden information in large files
- Manual reconstruction of fragmented data

---

## Tools Used

- **Linux (Kali / Ubuntu)**
- **Command-Line Utilities**
  - `wget`
  - `file`
  - `strings`
  - `grep`
- **Wireshark**
- **Binwalk**
- **File Manager (Thunar)**
- **PDF Viewer**
- **Image Viewer**
- **Git & GitHub**
- **Markdown (`.md`) for documentation**

---

## Key Forensics Concepts Reinforced

- Hidden data can exist beyond what is visually visible
- File formats often contain layered or embedded information
- Network traffic can expose sensitive information
- Improper redaction does not equal data removal
- Automated tools must be combined with manual analysis
- Digital artifacts often persist unless securely removed

---

## OWASP & Security Relevance

Although these challenges focus on forensics, they reinforce real-world security issues such as:
- Information Disclosure
- Improper Data Handling
- Security Misconfiguration
- Insecure Data Storage
- Incident Response & Evidence Analysis

---

## Documentation & Professional Practices

- Maintained **daily Markdown writeups** for each challenge
- Followed a **consistent documentation structure**
- Clearly explained analysis steps and reasoning
- Used **ethical flag masking**
- Practiced writing like a **junior SOC analyst / forensic investigator**

---

## Learning Outcome (Week 01)

This week provided a strong foundation in **digital forensics fundamentals**.  
I learned how attackers may hide data and how investigators can systematically recover it using both automated tools and manual analysis techniques. These skills are essential for **incident response, SOC operations, and forensic investigations**.

---

## Next Steps (Week 02 Goals)

- Explore advanced image and memory forensics
- Practice deeper PCAP traffic analysis
- Learn metadata and filesystem structures
- Begin correlating forensic findings with attack scenarios
- Continue building a professional forensics portfolio

---

📌 *This progress report reflects hands-on cybersecurity learning through ethical forensic challenges conducted in controlled environments.*
