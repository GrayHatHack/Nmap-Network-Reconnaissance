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
### Step 3: Operating System (OS) Fingerprinting
To gather intelligence on the underlying target system architecture and TCP/IP stack behavior.

* **Command Used:**
  ```bash
  sudo nmap -O -T4 scanme.nmap.org
  ```

### 📸 Screenshots & Visual Proof

### Port & Service Version Detection Output
  ![Port Scan Output](Screenshot%202026-10-01%20174556.png)

### OS Fingerprinting & Stack Analysis Output
![OS Detection Output](Screenshot%202026-10-01%20175700.png)

---

## 📈 Key Learnings & Takeaways
1. **Stealth Auditing:** Learned how SYN scans (`-sS`) optimize footprint reduction during network evaluations.
2. **Service Mapping:** Gained hands-on experience in detecting service signatures and potential version vulnerabilities.
3. **OS Intelligence:** Understood how remote network stack fingerprinting works during security assessments.
  
