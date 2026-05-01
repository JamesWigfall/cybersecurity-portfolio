# Network Analysis and Security Assessment

**Prepared by:** James Wigfall  

---

## Overview

This project demonstrates the use of network analysis and security tools to identify open ports, analyze protocols, and assess potential vulnerabilities in a target environment. The assessment includes reconnaissance, scanning, protocol analysis, and ethical considerations for cybersecurity operations.

---

## Common Ports and Network Security Controls

### Common TCP/UDP Ports

| Protocol | Port |
|----------|------|
| HTTP | 80 |
| HTTPS | 443 |
| FTP | 20/21 |
| SSH | 22 |
| SMTP | 25 |
| RDP | 3389 |

---

### Network Security Controls

Security devices play a critical role in managing traffic and protecting network infrastructure:

- **Firewalls** enforce access control by filtering traffic based on IP, ports, and protocols  
- **Routers** manage traffic between networks and subnets  
- **Intrusion Prevention Systems (IPS)** detect and block malicious activity  
- **VLANs** segment networks to isolate users and reduce attack spread  
- **Layer 3 Switches** control communication between subnets using ACLs  

These controls support **network segmentation** and the principle of **least privilege**, reducing overall risk.

---

## Network Diagnostic Tools

### Tools Used

- **Ping / Traceroute** – Verify connectivity and trace network paths  
- **NSLookup / Dig** – Resolve domain names and identify DNS records  
- **Netstat** – Identify active ports and services  
- **DNSDumpster** – OSINT tool for domain reconnaissance  
- **Nmap / Zenmap** – Port scanning, OS detection, and vulnerability discovery  
- **Wireshark** – Packet capture and deep protocol analysis  

---

### Key Insights

- Nmap revealed open ports and exposed services  
- Wireshark provided visibility into TCP, UDP, HTTP, TLS, and ARP traffic  
- DNS tools helped identify infrastructure and domain relationships  

👉 Nmap and Wireshark were the most valuable tools due to their depth in **discovery and analysis**

---

## Ethical Considerations

The use of network tools must follow strict ethical and legal guidelines:

- Always obtain **explicit authorization** before scanning systems  
- Follow **Rules of Engagement (ROE)**  
- Use **coordinated vulnerability disclosure** when reporting findings  

Unauthorized scanning may violate laws such as the **Computer Fraud and Abuse Act (CFAA)**.

---

## Network Discovery Results

### Key Findings

- Target system IP: 10.13.246.13  
- 1000 ports scanned per host  
- Open ports identified included:
  - Web services (80, 443)  
  - Remote access (22, 3389)  
  - File sharing and system services  

---

### Security Observations

- Systems with multiple open ports increase attack surface  
- Misconfigured services can expose sensitive access points  
- Proper firewall rules and segmentation are critical  

---

## Nmap Scanning

### Commands Used

```bash
sudo nmap -sS -p- -T4 -oN nmap_TCPSYN.txt target
sudo nmap -sS -p- -T3 -oN nmap_UDP.txt target
sudo nmap -Pn -sS -sV -O --osscan-guess target
