# Flag

> **ProFTPD**

# Prompt

> **What type of service is running on kenobi.hackingarena.com in the port range 4500-5000?**

# Solution

Kali Linux, nmap,
nmap -sV -p 4500-5000 kenobi.hackingarena.com -Pn

PORT     STATE SERVICE VERSION
4746/tcp open  ftp     ProFTPD

# Additional Info

Additional solution / info