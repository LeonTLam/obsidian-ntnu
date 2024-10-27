# Flag

> **FLAG**

# Prompt

> **Ladies and Gentlemen,
> This is challenge no.5.
> A little bit of everything...
> Ask 3CPO (3cpo.hackingarena.com) on port range 21000-22000

# Solution

Run **nmap** and port scan from 21000 to 22000. 

![[Pasted image 20241027023524.png]]

Run **ncat** to connect to remote server and open the TCP connection to specified port.

![[Pasted image 20241027023601.png]]

Find the server on port 21214 is running on FTP, and proceed by connecting to the FTP server anonymously with FileZilla.

![[Pasted image 20241027023818.png]]
# Additional Info

Additional solution / info