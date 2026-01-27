# Scanning Networks
*CEH – Ethical Hacking Notes*

---

## Introduction

Network scanning is the process of **examining a target network** to identify:
- Live hosts
- Open ports
- Running services
- Operating systems
- Security controls such as firewalls and IDS/IPS

Scanning bridges the gap between **reconnaissance** and **exploitation** and plays a critical role in vulnerability assessment.

---

## Objectives of Network Scanning

During network scanning, the attacker or security professional aims to:

- Perform host discovery  
- Perform port and service discovery  
- Perform operating system discovery  
- Scan networks while attempting to bypass IDS and firewalls  

---

## What is Network Scanning?

Network scanning is the process of examining the **network infrastructure** to identify:
- Active devices (hosts)
- Open ports
- Services running on those ports
- Potential entry points for attacks

Scanning provides a **technical view of the attack surface** and helps determine the next steps in security testing.

---

## Host Discovery

Host discovery is used to identify **which systems are alive** on a network.

Common techniques include:
- ICMP echo requests (ping)
- ARP requests (local networks)
- TCP/UDP-based probing

### Example (Nmap Host Discovery)
```bash
nmap -sS 192.168.1.0/24
```
---

## Port & Service Discovery

Port scanning is the process of identifying open ports on a target system and determining which services are running on those ports.

This helps in understanding:
- Exposed services
- Possible vulnerabilities
- Misconfigurations in network services

```bash
nmap -sV <target-ip>
```

---

## Operating System Discovery

Operating System (OS) discovery, also known as OS fingerprinting, is used to determine the operating system running on a target machine.

This information is useful because:
- Vulnerabilities are often OS-specific
- Exploits depend on OS behavior

```bash
nmap -O <target-ip>
```
---

## Scanning Beyond IDS and Firewalls

Firewalls and IDS/IPS systems monitor and block suspicious network traffic.  
During security testing, scanning techniques may be used to reduce detection and understand network behavior under restrictions.

Common techniques include:
- Fragmented packets
- Decoy scanning
- Timing-based scans
- Source port manipulation

These techniques help analyze how well security controls respond to scanning activity.

---

## OSI Model (Networking Basics)

Understanding the OSI model is essential for network scanning and attack analysis, as it explains how data flows through a network.

### OSI Layers Explained

- **Application Layer**  
  Protocols such as FTP, SSH, Telnet, SMTP, DNS, and HTTP

- **Presentation Layer**  
  Responsible for encryption (SSL/TLS) and data compression

- **Session Layer**  
  Establishes, manages, and terminates communication sessions

- **Transport Layer**  
  Handles end-to-end communication using TCP and UDP

- **Network Layer**  
  Responsible for IP addressing, ICMP, ARP, and packet routing

- **Data Link Layer**  
  Works with MAC addresses and frames  
  (MAC address is embedded in the Network Interface Card – NIC)

- **Physical Layer**  
  Transmits data in the form of bits (e.g., 01010101)

---

# Enumeration

## Enumeration Overview

Enumeration is the process of **actively extracting detailed information** about a target system after network scanning has identified live hosts and open ports.

Unlike scanning, enumeration involves **direct interaction** with the target to obtain sensitive details such as users, services, shares, and configurations.

**Objective:** Identify precise attack vectors for later phases like exploitation and privilege escalation.

---

## Information Gathered During Enumeration

- Usernames and groups  
- Hostnames and domain details  
- Network shares and permissions  
- Running services and versions  
- Operating system details  
- Password and account policies  
- SNMP data from network devices  
- Email IDs and contact information  

---

## Scanning vs Enumeration

| Scanning | Enumeration |
|--------|-------------|
| Identifies live hosts and open ports | Extracts detailed system data |
| Less intrusive | More intrusive |
| No authentication | May involve authentication |
| Broad-level discovery | Deep, system-specific discovery |

---

## Types of Enumeration

### 1. NetBIOS Enumeration

Used to gather information from **Windows-based systems** using NetBIOS and SMB services.

**Information Obtained:**
- Computer name  
- Domain/workgroup name  
- Logged-in users  
- Shared resources  

**Common Ports:**
- TCP/UDP 137, 138, 139  
- TCP 445  

---

### 2. SNMP Enumeration

Uses **Simple Network Management Protocol (SNMP)** to extract data from network devices such as routers, switches, and servers.

**Information Obtained:**
- Network devices  
- Routing tables  
- Interface details  
- System uptime  
- Installed software  

**Common Port:**
- UDP 161  

**Risk:** Weak or default community strings like `public` and `private`.

---

### 3. LDAP Enumeration

Used in **Active Directory environments** to gather directory-related information.

**Information Obtained:**
- Users and groups  
- Organizational Units (OUs)  
- Domain structure  
- Password policies  

**Common Ports:**
- TCP/UDP 389 (LDAP)  
- TCP 636 (LDAPS)  

---

### 4. SMB Enumeration

Targets **Server Message Block (SMB)** services for file and printer sharing.

**Information Obtained:**
- Shared folders  
- Access permissions  
- User access levels  

**Common Port:**
- TCP 445  

---

### 5. DNS Enumeration

Used to identify **DNS records and subdomains** related to the target organization.

**Information Obtained:**
- Hostnames  
- Subdomains  
- Mail servers (MX records)  
- Zone transfer data  

**Common Port:**
- TCP/UDP 53  

---

### 6. SMTP Enumeration

Used to verify **valid email users** on mail servers.

**Information Obtained:**
- Valid usernames  
- Email addresses  

**Common Port:**
- TCP 25  

---

### 7. RPC Enumeration

Used to extract information from **Remote Procedure Call (RPC)** services.

**Information Obtained:**
- Network services  
- User and group information  

**Common Ports:**
- TCP 135  
- Dynamic RPC ports  

---

## Enumeration Techniques

- Banner grabbing  
- Null session enumeration  
- Brute-force enumeration  
- Service-specific queries  
- Anonymous login testing  

---

## Tools Used for Enumeration

### Common Enumeration Tools

- Nmap (NSE scripts)  
- enum4linux  
- SNMPwalk  
- rpcclient  
- Netcat  
- Metasploit auxiliary modules  

---

## Enumeration in Metasploit

Metasploit provides **auxiliary modules** for enumeration purposes.

**Key Points:**
- Used for scanning and information gathering  
- No payload is used  
- Supports SMB, SNMP, FTP, DNS, and more  

---

## Risks Identified During Enumeration

- Weak or default credentials  
- Misconfigured services  
- Excessive permissions  
- Anonymous access enabled  
- Legacy and insecure protocols  

---

## Usage of Enumeration Results

Information obtained during enumeration is used to:
- Perform password attacks  
- Identify vulnerabilities  
- Plan exploitation strategies  
- Escalate privileges  

---

## Conclusion

Network scanning and system hacking concepts form the foundation of vulnerability assessment and penetration testing.  
Understanding scanning techniques, OSI layers, and exploitation components helps security professionals identify risks before attackers can exploit them.
