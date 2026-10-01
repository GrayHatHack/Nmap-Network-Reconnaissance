# Nmap Network Reconnaissance & Port Scanning

## 📌 Project Overview
This project demonstrates intermediate-level network reconnaissance and security auditing using **Nmap** (Network Mapper). In cybersecurity, reconnaissance is a critical initial phase used by security professionals to discover live hosts, identify open ports, detect running software versions, and perform OS fingerprinting on a target network.

---

## 🛠️ Tools & Technologies Used
* **Operating System:** Kali Linux (VirtualBox)
* **Tool:** Nmap (Network Mapper v7.99)
* **Techniques:** 
  * Host Discovery (`-sn`)
  * SYN Stealth Scanning (`-sS`)
  * Service Version Detection (`-sV`)
  * OS Fingerprinting (`-O`)

---

## 🚀 Step-by-Step Implementation & Execution

### Step 1: Host Discovery & Target Identification
Before performing port scans, a host discovery ping sweep was executed to verify active systems on the network.
* **Command Used:**
  ```bash
  sudo nmap -sn scanme.nmap.org
  ```
### Step 2: Port Scanning & Service Version Detection
To identify active services without triggering heavy alerts, a stealth SYN scan combined with version detection was executed against specific high-priority ports.

* **Command Used:**
  ```bash
  sudo nmap -sS -sV -p 22,80,443 scanme.nmap.org
  ```
* **Key Findings:**

  * Port 22/tcp (Open - OpenSSH 6.6.1p1)

  * Port 80/tcp (Open - Apache httpd 2.4.7)

  * Port 443/tcp (Filtered - HTTPS)    
