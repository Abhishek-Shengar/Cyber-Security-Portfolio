# Footprinting & Reconnaissance
*CEH Master – Ethical Hacking Notes*

---

## Introduction

Footprinting and reconnaissance are the **initial and most critical phases** of ethical hacking.  
The objective of this phase is to **collect maximum information about a target** before performing any active testing or exploitation.

Effective reconnaissance helps in:
- Understanding the target’s attack surface
- Identifying exposed assets and technologies
- Planning further security assessment steps

---

## Types of Footprinting

### 1. Active Footprinting

Active footprinting involves **direct interaction with the target system**.  
This method may alert the target and is generally performed after passive techniques.

**Examples:**
- Direct scanning
- Interacting with target services
- Sending packets to gather information

---

### 2. Passive Footprinting

Passive footprinting involves **gathering information without directly interacting with the target**.  
It is stealthy and does not generate logs on the target side.

**Examples:**
- Search engines
- Public databases
- OSINT tools
- Social networking platforms

---

## Footprinting Using Search Engines

Search engines are widely used for passive reconnaissance and OSINT-based information gathering.

**Common Search Engines:**
- Google
- Bing
- DuckDuckGo
- Yahoo

---

## Google Advanced Search Operators (Google Dorking)

Google Dorking is the use of **advanced search operators** to locate sensitive or exposed information indexed by search engines.

**Common Operators:**
- `filetype:` – Search for specific file types (PDF, DOC, XLS, etc.)
- `site:` – Restrict results to a specific domain
- `intitle:` – Search for keywords in the page title
- `inurl:` – Search for keywords in the URL

These operators can help identify:
- Exposed documents
- Login portals
- Configuration files
- Development or test environments

---

## Domain & Infrastructure Information Gathering

### Netcraft Domain Search

Netcraft is used to:
- Identify company domains and subdomains
- Gather hosting and infrastructure details
- Understand technology exposure

It helps in building a **target infrastructure overview**.

---

### Shodan

Shodan is a search engine used to discover **internet-connected devices**.

It is commonly used for:
- IoT device discovery
- Open ports and exposed services
- Banner and service information gathering

Shodan is especially useful for identifying **misconfigured or publicly exposed systems**.

---

### Censys

Censys is used for:
- Internet-wide scanning
- Certificate and service discovery
- Cloud and IoT asset analysis

It is often used alongside Shodan to **validate and correlate findings**.

---

## Subdomain Enumeration

### Finding Subdomains Using Sublist3r

Subdomain enumeration helps in expanding the attack surface by identifying **additional or hidden subdomains**.

**Installation:**
```bash
apt install sublist3r
```
Usage:
```bash
sublist3r -d <domain-name>
```
Example:
```bash
sublist3r -d eccouncil.org
```
This technique can reveal:
- Admin panels
- Development environments
- Legacy or forgotten services

## Passive Operating System Fingerprinting

The target operating system can often be identified **without active scanning** using:

- Netcraft  
- Shodan  
- Censys  

Passive OS fingerprinting helps in understanding:
- Possible vulnerabilities  
- System architecture  
- Attack feasibility  

---

## Social Media & Username Enumeration

### Gathering Personal Information Using Sherlock

Sherlock is used to check **username availability across multiple social networking platforms**.

**Installation:**
```bash
apt install sherlock
```
Usage:
```bash
sherlock <username>
```
Example:
```bash
sherlock ElonMusk
```
This technique is useful for:
- OSINT investigations  
- Social engineering assessments  
- Understanding digital footprint exposure  


---

## Conclusion

Footprinting and reconnaissance form the **foundation of ethical hacking**.  
Accurate and stealthy information gathering enables better planning, safer testing, and more effective security assessments.
