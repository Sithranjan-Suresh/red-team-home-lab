# Day 3 – Scanning & Enumeration

## Tools Used
- ftp
- telnet
- enum4linux
- nikto
- whatweb
- nmap (with -sC -sV)

## Findings

### FTP (Port 21)
- Anonymous login: Allowed
- Attempted `ls`: No files or directories visible
- Attempted `cd` into `/pub`, `/var`, `/etc`: Access denied
- Likely a secure configuration, or limited view for anonymous user
- Lesson: Just because you get in doesn’t mean you can see everything

### Telnet (Port 23)
- Login success using `msfadmin:msfadmin`

### SMB (139/445)
- Accounts found:
  - administrator
  - guest
  - krbtgt
  - domain admins
  - root
  - bin
  - none
- These usernames may help with password spraying or brute force in exploitation phase
- Vulnerability: Anonymous login allows account enumeration — a misconfiguration in SMB

### HTTP (Port 80)
- Found pages: `/mutillidae/`, `/phpinfo.php`, etc
- Nikto reports:
  - Directory listing enabled
  - Outdated Apache version
  - PHP info disclosure

### Nmap Scripts
- Shows service banners and OS guess

## Lessons Learned
- Anonymous FTP access is a huge risk
- Default creds still active on Telnet
- SMB leaks user data
- Web app has multiple exposed paths

