# OSCP
Offensive Security Certified Professional is an ethical hacking certification offered by Offensive Security that teaches penetration testing methodologies and the use of the tools included with the Kali Linux distribution.
# Enumeration
## NMAP
nmap -sV -sS 127.0.0.1 (all ports)
## Nikto
nikto -h 127.0.0.1
## SMB
## Gobuster
gobuster dir -u 127.0.0.1 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt 
## Linpeas
## Winpeas
# Payloads
## msfvenom
# Brute Force
# Exploits
## Apache Apisix 2.8
(CVE-2022-24112)  
{"error_msg":"404 Route Not Found"}  
https://github.com/twseptian/cve-2022-24112
## Ladon Framework
(NO CVE)  
WSGIServer 0.1 (Python 2.7.16)  
https://www.exploit-db.com/exploits/43113  
# Shell Upgrade
## Python
python -c 'import pty; pty.spawn("/bin/bash")'
# Tool Transfer
## Python
python3 -m http.server 8080
# Privilege Escalation
## Crontab
cat /etc/crontab

