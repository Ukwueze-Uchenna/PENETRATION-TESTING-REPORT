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
<img src="https://img.shields.io/badge/👨🏽‍💻Pentester: Ukwueze%20Uchenna%20Collins-C00000?style=flat-square" />
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

### 4.2.1. WHOIS
WHOIS was used to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.
> **Command used: ```whois networkwalks.com```**

<img width="1920" height="1080" alt="wk2-pm1-result-whois networkwalks1" src="https://github.com/user-attachments/assets/4f0194fa-0b11-4c36-8367-3422c18d6b92" />

<img width="1920" height="1080" alt="wk2-pm1-result-whois networkwalks2" src="https://github.com/user-attachments/assets/8e63f437-e7f2-42c8-ae97-4df4e4c4c224" />

> ⚠️ **Security relevance: Here the name servers point to HostGator, so an attacker instantly learns the hosting provider. Registration dates, and abuse contacts help with social engineering and planning.**

---

### 4.2.2. Whatweb
WhatWeb was used to identify and fingerprint technologies used by the website.
> **Command used: ```whatweb networkwalks.com```**

<img width="1920" height="1080" alt="wk2-pm1-result-whatweb networkwalks" src="https://github.com/user-attachments/assets/ee685813-98bc-41f5-b138-bfd3c9c43728" />

> ⚠️ **Security relevance: whatweb exposes the exact software and versions (here Wordpress 7.1.4 and WP Download 
Manager 3.3.76). An attacker looks these versions up in vulnerability databases to find known 
exploits. It also leaks the server IP and an email address.**

---

### 4.2.3 Nslookup
Nslookup was used to resolve the targets domain name to its IP address. The provided result identified ```192.232.216.135.```
> **Command used: ```nslookup networkwalks.com; OR, $ nslookup -vc networkwalks.com 8.8.8.8```**```**

<img width="1920" height="1080" alt="wk2-pm1-result-nslookup networkwalks" src="https://github.com/user-attachments/assets/92b4a0c1-7f45-47ed-aeb6-7bb768ace91b" />

> ⚠️ **Security relevance: nslookup turns a domain name into its real IP address (192.232.216.135). Knowing the IP lets an 
attacker scan the server directly, look up other sites on the same IP, and map the target's 
infrastructure.**

---

### 4.2.4 curl
Curl was used with the -I option to inspect the HTTP response headers. This provided additional information about the web application and exposed the WordPress REST API endpoint /wp-json/.
> **Command used: ```curl -I https://networkwalks.com```**

<img width="1920" height="1006" alt="wk2-pm1-result-curl -I networkwalks" src="https://github.com/user-attachments/assets/da4a2f3a-0c1b-4d23-99ec-abd12017a057" />

> ⚠️ **Security relevance: HTTP headers leak the web server, caching stack and hidden endpoints (here the WordPress 
REST API at /wp-json/). Attackers read headers to fingerprint the stack and find entry points 
without even loading the full page.**

---

### 4.2.5 wafw00f 
wafw00f was used to determine whether a Web Application Firewall was protecting the website. The result identified ModSecurity (SpiderLabs) Web Application Firewall.
> **Command used: ```wafw00f networkwalks.com```**

<img width="1920" height="1080" alt="wk2-pm1-results-wafw00f networkwalks" src="https://github.com/user-attachments/assets/f9d2172b-18da-448c-af9a-e968dc21cc44" />

> ⚠️ **Security relevance: wafw00f tells an attacker if a firewall is watching. Here the site sits behind ModSecurity
(SpiderLabs). Knowing a WAF is present shapes the whole attack: naive attempts will be blocked 
or logged, so the attacker must adapt or try to bypass it.**

---

### 4.2.6 dnsrecon 
dnsrecon was used to enumerate DNS records. The results provided information relating to name servers, mail servers, SPF/TXT records, service records and DNS software information.
> **Command used: ```dnsrecon -d networkwalks.com```**

<img width="1920" height="1080" alt="wk2-pm1-result-dnsrecon -d networkwalks" src="https://github.com/user-attachments/assets/63541c8b-9e58-412d-9d78-6a60e5a5966a" />

> ⚠️ **Security relevance: dnsrecon maps the target's entire DNS footprint: mail servers, DNS software version (Bind 
9.16.23), SPF policy and cPanel service records. Each record is a potential foothold and helps an 
attacker understand the email and hosting setup.**

---













