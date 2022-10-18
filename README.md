# OSCP
Offensive Security Certified Professional is an ethical hacking certification offered by Offensive Security that teaches penetration testing methodologies and the use of the tools included with the Kali Linux distribution.
# Enumeration
## NMAP
nmap -sV -sS 127.0.0.1 (all ports)
## Nikto
nikto -h 127.0.0.1
## SMB
## Gobuster
gobuster dir -e -w /usr/share/wordlists/dirb/common.txt -t 5 -u http://127.0.0.1 -q
## Linpeas
## Winpeas
# Payloads
## msfvenom
# Brute Force
# Cracking
## Hashcat (https://hashcat.net/wiki/doku.php?id=example_hashes)
hashcat -a 0 -m 1600 -w 2 --show hash.txt /usr/share/wordlists/rockyou.txt  
# Exploits
## Apache Apisix 2.8
(CVE-2022-24112)  
{"error_msg":"404 Route Not Found"}  
https://github.com/twseptian/cve-2022-24112
## Ladon Framework
(NO CVE)  
WSGIServer 0.1 (Python 2.7.16)  
https://www.exploit-db.com/exploits/43113  
https://www.youtube.com/watch?v=3XgGjEG0lLw  
# Shell Upgrade
## Python
python -c 'import pty; pty.spawn("/bin/bash")'
# Tool Transfer
## Python
python3 -m http.server 8080
# Privilege Escalation
## Crontab
cat /etc/crontab

