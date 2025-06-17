# Red Team Home Lab – Beginner-Friendly Cybersecurity Lab

This project is a 5-day practical red team home lab using VirtualBox with Kali Linux (attacker) and Metasploitable 2 (vulnerable target). It simulates real-world offensive security workflows including reconnaissance, scanning, exploitation, and post-exploitation.

---

## Lab Setup

- Kali Linux (2023.x)
- Metasploitable 2
- VirtualBox Host-Only Networking

---

## Tools Used

- `nmap` – Network scanning
- `netdiscover` – Live host discovery
- `ftp` – Manual FTP enumeration
- `smbclient`, `enum4linux` – SMB enumeration
- `msfconsole` – Exploitation via Metasploit
- `whoami`, `id`, `netstat`, etc. – Post-exploitation

---

## Daily Breakdown

### Day 1 – Setup
- Installed and configured VMs
- Verified networking (host-only)
- Took IP screenshots

### Day 2 – Recon + Scanning
- Ran `nmap -sV` and other commands
- Identified open ports, vulnerable services

### Day 3 – Enumeration
- Enumerated FTP and SMB services
- Found valid usernames, anonymous access

### Day 4 – Exploitation
- Used Metasploit to exploit `vsftpd 2.3.4` backdoor
- Demonstrated shell access

### Day 5 – Post-Exploitation
- Ran enumeration commands on target
- Simulated persistence techniques
- Documented findings

---

## Screenshots

Every day includes screenshots showing:
- Commands used
- Tool outputs
- Shell access proof
- Enumeration results

---

## What I Learned

- How red teamers think: from discovery to full compromise
- Practical use of popular offensive tools
- Linux fundamentals & working in CLI-only environments
- How to document attacks like a real penetration tester

