# Flag

> **FLAG**

# Prompt

> **What is the sum of the all open ports at padawan.hackingarena.com? This time not only the regular ports has to be considered. E.g. if only tcp22, tcp80 and tcp443 is open then the answer is 545.
> Please check it up to 5000 (to save time), but write the nmap command for all ports in your document.**

# Solution

nmap -sT -p 1-5000 padawan.hackingarena.com 
![[Pasted image 20241009135342.png]]
Summed all ports and got 14,478

# Additional Info

Additional solution / info