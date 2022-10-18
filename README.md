# OSCP
Offensive Security Certified Professional is an ethical hacking certification offered by Offensive Security that teaches penetration testing methodologies and the use of the tools included with the Kali Linux distribution.
# Enumeration
## NMAP
nmap -sV -sS 127.0.0.1 (all ports)
## SMB
## Gobuster
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
# Shell Upgrade
## Python
python -c 'import pty; pty.spawn("/bin/bash")'
# Tool Transfer
## Python
python3 -m http.server 8080

