<div align="center">

# 🤖 PENETRATION TESTING REPORT

**FOOTPRINTING & NETWORK SCANNING PHASES**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
   <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/windows os-404040?style=flat-square&labelColor=C00000&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />  
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <div align="center">
<img src="https://img.shields.io/badge/Author: Ukwueze%20Uchenna%20Collins-C00000?style=flat-square" />
</p>

---

<div align="center">
W2-PM-FINAL | CYBERSECURITY |  NETWORKWALKS 
</p>
  
</div> 
<p align="left">
🚧 Project Overview 
</p>

</div> 
<p align="left">
  
| **Field** | **Detail** |
|---|---|
| **Pentester** | **Ukwueze Uchenna Collins** |
| **Program/Batch** | Networkwalks-B084 |
| **Date** | 9<sup>th</sup> November, 2026 |
| **Modules completed** | W2-PM1 (Multiple Kali Tools)<br>W2-PM5 (Zenmap Scanning) |
| **Client/Target** | 1. Networkwalks (secured written permission already)<br>2. My own local LAN Network |
| **Permission secured from client?** | Yes |
| **Phases covered** | **Phase 1:** Reconnaissance & Footprinting<br>**Phase 2:** Scanning & Network Discovery<br>|

---

# 🎯 1. Liability Disclaimer

The activities documented in this report were conducted strictly on systems and devices for which prior written authorization was obtained, or on personally owned hardware. The contents of this document are intended strictly for educational and research purposes. The instructor, author, and Networkwalks assume no liability for the misuse or misapplication of this knowledge; all subsequent actions taken by the reader are their sole responsibility. Unauthorized system access constitutes a criminal offense in most jurisdictions, regardless of whether data or systems are damaged, and can result in severe legal penalties, significant fines, career impact (employment termination), and a permanent criminal record. 
> ⚠️ **Note: Authorization must be Secured from Networkwalks before performing reconnaisance & footprinting**

---

# ☄️ 2. Introduction

As part of my Networkwalks internship program (week 2), this report provides a comprehensive analysis of the Footprinting/Reconnaissance phases targeting the networkwalks.com domain and subsequent scanning of the local network utilizing Zenmap. By leveraging a combination of Kali Linux tools and Zenmap, this assessment simulates how a malicious actor actively maps live network hosts. The methodology mirrors an attacker's lifecycle, transitioning from passive data gathering (W2-PM1) to active host discovery (W2-PM5).

### 💡 Footprinting

All footprinting commands were executed within a Kali Linux environment.

### 🔎 Scanning activities 

Were performed via Zenmap on a windows host (pc). 

### 📝 Methodology, analysis framework, and documentation
To ensure reproducibility and rigorous documentation, every technical step outlines the exact commands utilized, corresponding system output, verification screenshots, and a brief analytical note from the attackers point of view regarding the security implications of the exposed data.

---

# ⚒️ 3. Tools Used

Each tool used and its purpose can be found in the table below.

| Tool/commands | Purpose |
|---|---|
| Kali Linux           | Operating system deployed to conduct initial reconnaissance and information gathering.          |
| Windows OS           | Host Operating systems utilized for networking activities including network mapping via Zenmap. |
| WHOIS                | Queries or Finds domain registration details such as registration ownership, critical dates, and authoritative name servers.                                                                                              |
| whatweb              | Identifies and fingerprints web technologies, including servers, CMS - content management system, plugins, and IP.                                                                                                         |
| nslookup             | Performs DNS lookup to resolve target domain names to their respective IP address               |
| curl -I              | Fetches, analyses, and reads the HTTP response headers of the website.                          |
| wafw00f              | Probes the web application to detect the presence and type of Web Application Firewall (WAF) present.                                                                                                                 |
| dnsrecon             | Enumerate or discovers all DNS records (NS, MX, SPF, TXT, SRV).                                 |
| Zenmap (Nmap GUI)    | Scan the local subnet to find live hosts, active IP addresses, and MAC addresses.               |
| Windows CMD          | Local IP and MAC address identification via a command line interface.                           |

---

# 🛡️ 4. Activities Performed
## 4.1. Background
Reconnaissance (also called as footprinting) is the first step in any real attack or security test. Before 
touching a target, an attacker quietly collects as much public information about it as possible. This 
includes who owns the domain, its real IP address, the hosting provider, the web technologies it 
runs, its DNS and mail records, and whether a firewall is protecting it. All of this comes from 
information the target has already made public, so the target never even knows it is being studied. 
This is why recon is powerful and very hard to detect.

> ⚠️ **In this lab, the live website networkwalks.com was footprinted.**

## 💡4.2. Footprinting & Reconnaissance

I performed reconnaissance against the `networkwalks.com` domain using six Kali Linux commands: 

```text
WHOIS
WhatWeb
Nslookup
Curl 
Wafw00f 
DNSRecon
```
> ⚠️ **Note: Each tool was used to collect a different type of information about the target as seen in table 3 above.**

---

### 4.2.1   WHOIS
WHOIS was used to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.

<img width="1920" height="1080" alt="wk2-pm1-result-whois networkwalks2" src="https://github.com/user-attachments/assets/8e63f437-e7f2-42c8-ae97-4df4e4c4c224" />

<img width="1920" height="1080" alt="wk2-pm1-result-whois networkwalks1" src="https://github.com/user-attachments/assets/4f0194fa-0b11-4c36-8367-3422c18d6b92" />

> ⚠️ **Note: Here the name servers point to HostGator, so an attacker instantly learns the hosting provider. Registration dates, and abuse contacts help with social engineering and planning.**

### 4.2.2 




