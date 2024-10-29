# Flag

> **FLAG**

# Prompt

> **We intercepted a document exchanged between two CIA operators. We noted the IP as 158.39.75.16 and detected some activity on a port somewhere between 4000 and 5000. Can you find the purpose of their mission?![[OperationDancing.jpg]]**

# Solution

Use **nmap** to scan hosts on ip **158.39.75.16** between ports **4000 - 5000**.

```
nmap -sV -p4000-5000 158.39.75.16
```

![[Pasted image 20241029205725.png]]

Attempt to access Samba share by following command:

````
smbclient //<ip>/<share_name>

Ip address: 158.39.75.16
Share_name: Based on the attached picture, ship that sank at given coordinations.
````

SMB client name 

smbclient //<ip>/<share_name> port <4445> -U <username> 
---> password: <jennifer>

Extract all fiiles, open txt and find surname for Mr. P.
Google ship john shipwreck cia. find whole name for mr. P

use last name to find a folder, and file filename doesier.txt

# Additional Info

Additional solution / info