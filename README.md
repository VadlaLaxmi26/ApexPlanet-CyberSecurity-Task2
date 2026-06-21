# ApexPlanet Cybersecurity Internship – Task 2

# Network Security Scanning & Vulnerability Assessment

## 📌 Objective

The objective of this task was to perform network reconnaissance, host discovery, service enumeration, packet analysis, firewall testing, and vulnerability assessment using Kali Linux and Metasploitable2 in a virtual lab environment.

---

# 🛠 Lab Environment

## Attacker Machine

* Kali Linux

## Target Machine

* Metasploitable2

## Virtualization Platform

* Oracle VirtualBox

---

# 🔧 Tools Used

* Nmap
* Wireshark
* Netcat (nc)
* OpenVAS (GVM)
* Metasploitable2
* Kali Linux
* VirtualBox
* Firefox Browser

---

# ⚙️ Network Configuration

Configured a virtual cybersecurity lab using:

### Kali Linux

* Host-Only Adapter
* NAT Adapter

### Metasploitable2

* Host-Only Adapter
* NAT Adapter

Verified connectivity between attacker and target machines using:

```bash
ping 192.168.56.101
```

---

# 🚀 Activities Performed

## 1. Host Discovery

Identified active hosts in the local network.

```bash
nmap -sn 192.168.56.0/24
```

### Outcome

* Detected Kali Linux
* Detected Metasploitable2

---

## 2. Banner Grabbing

Collected service banners from target services.

### FTP Banner

```bash
nc 192.168.56.101 21
```

### HTTP Header Information

```bash
curl -I http://192.168.56.101
```

### Outcome

* Identified FTP service version
* Retrieved HTTP server information

---

## 3. Service Enumeration

Discovered open ports and service versions.

```bash
nmap -sV 192.168.56.101
```

### Services Identified

* FTP
* SSH
* Telnet
* SMTP
* HTTP
* Samba

---

## 4. TCP SYN Scan

Performed stealth TCP scanning.

```bash
sudo nmap -sS 192.168.56.101
```

### Outcome

* Enumerated open TCP ports
* Identified exposed services

---

## 5. Operating System Detection

Identified the target operating system.

```bash
sudo nmap -O 192.168.56.101
```

### Outcome

* Linux-based operating system detected

---

## 6. Aggressive Scan

Performed comprehensive scanning.

```bash
sudo nmap -A 192.168.56.101
```

### Included

* OS Detection
* Service Detection
* NSE Script Scanning
* Traceroute

### Outcome

* Detailed information about services and operating system obtained

---

## 7. Saving Scan Reports

Generated and stored Nmap reports.

```bash
sudo nmap -A 192.168.56.101 -oN nmap-report.txt
```

### Outcome

* Saved detailed scan results for documentation

---

## 8. Packet Analysis Using Wireshark

Captured and analyzed network traffic.

### HTTP Analysis

Accessed:

```text
http://192.168.56.101
```

Captured HTTP packets.

### DNS Analysis

Executed:

```bash
nslookup google.com
```

Captured DNS requests and responses.

### FTP Analysis

Connected using:

```bash
ftp 192.168.56.101
```

Analyzed FTP traffic and authentication packets.

### Outcome

* Observed HTTP communication
* Analyzed DNS resolution process
* Observed FTP authentication traffic

---

## 9. Firewall Configuration and Testing

Viewed existing firewall rules.

```bash
sudo iptables -L
```

Configured firewall rule testing.

### Outcome

* Understood packet filtering concepts
* Analyzed firewall behavior

---

## 10. OpenVAS (GVM) Installation

Installed Greenbone Vulnerability Manager.

```bash
sudo apt update
sudo apt install gvm -y
```

### Setup

```bash
sudo gvm-setup
```

### Verification

```bash
sudo gvm-check-setup
```

### Outcome

* Successfully installed OpenVAS (GVM)
* Verified configuration and services

---

# 📊 Results

Successfully completed:

✅ Virtual Lab Setup

✅ Network Configuration

✅ Host Discovery

✅ Banner Grabbing

✅ Service Enumeration

✅ TCP Port Scanning

✅ Operating System Detection

✅ Aggressive Scanning

✅ Report Generation

✅ Packet Analysis using Wireshark

✅ Firewall Testing

✅ OpenVAS Installation and Verification

---

# 📁 Repository Structure

```text
ApexPlanet-Task2-Network-Security-Scanning
│
├── README.md
├── Screenshots/
│   ├── Network_Setup.png
│   ├── Host_Discovery.png
│   ├── Banner_Grabbing.png
│   ├── Service_Enumeration.png
│   ├── TCP_Scan.png
│   ├── OS_Detection.png
│   ├── Aggressive_Scan.png
│   ├── Wireshark_HTTP.png
│   ├── Wireshark_DNS.png
│   ├── Wireshark_FTP.png
│   ├── Firewall_Testing.png
│   └── GVM_Setup.png
│
└── Reports/
    └── nmap-report.txt
```

---

# 🎯 Learning Outcomes

* Network Reconnaissance
* Host Discovery Techniques
* Service Enumeration
* Operating System Fingerprinting
* Packet Analysis
* Firewall Configuration
* Vulnerability Assessment
* Hands-on Experience with Kali Linux and Metasploitable2

---

# 👩‍💻 Author

Vadla Laxmi

ApexPlanet Cybersecurity Internship
