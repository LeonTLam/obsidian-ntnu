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

I downloaded all of the shadow files which revealed hashed login credentials which I used **[dcode](https://www.dcode.fr/md5-hash)** to decode.

```
shadow.old
lou:$1$e39e74fb4e80ba656f773669ed50315a:18777:0:99999:7:::

shadow.old.1
lou:$1$d41219060e0c16c228ed4682cade6379:18777:0:99999:7:::

shadow.old.2
lou:$1$28d34f2e053dee2c0e9399a7924cd978:18777:0:99999:7:::

shadow.old.3
lou:$1$be1ae2eeeca8fb8302aed56fb0a6019d:18777:0:99999:7:::

shadow.old.4
lou:$1$5501462a4c13dd55a6b236ef4550e3e4:18777:0:99999:7:::

shadow.old.5
lou:$1$09084cc0cda34fd80bfa3cc0ae8fe3dc:18777:0:99999:7:::
```

Login credentials:

```
shadow.old
lou:Mary

shadow.old.1
lou:Sandra

shadow.old.2
lou:Tina

shadow.old.3
lou:Rita

shadow.old.4
lou:Erica

shadow.old.5
lou:Monica
```
# Additional Info

Additional solution / info