# Day 2 – Reconnaissance

## Objective
Identify open ports, running services, and possible vulnerabilities on Metasploitable 2.

## Target IP
192.168.56.102

## Nmap Findings
- Open Ports:
  - 21 (FTP)
  - 22 (SSH)
  - 23 (Telnet)
  - 80 (HTTP)
  - 3306 (MySQL)
  - 5432 (PostgreSQL)
  - ...etc

- Detected Services:
  - FTP: vsftpd 2.3.4
  - Telnet: Linux telnetd
  - HTTP: Apache 2.2.8
  - SSH: OpenSSH 4.7p1
  - MySQL: 5.0.51a

## Analysis
- vsftpd 2.3.4 is known vulnerable (backdoor)
- Telnet is open – may allow weak/no password
- Apache version is outdated → possible remote exploits
- No firewall detected
- SSH version is old but may require creds

## Tools Used
- nmap (`-sV`, `-A`, `-O`)
- netcat


## Lessons Learned
- Discovered multiple vulnerable services without logging in
- Practiced using Nmap flags to extract service versions
- Learned importance of version detection for exploitation
