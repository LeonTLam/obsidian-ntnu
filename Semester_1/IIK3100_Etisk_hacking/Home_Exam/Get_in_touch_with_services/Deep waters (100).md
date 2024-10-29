# Flag

> **Hacking-Arena{r3tri3v3_th3_submar1ne!}**


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
smbclient -p <port> //<ip>/<share_name> -U <username>
then
password for user "joehouston"

Port: 4445
Ip address: 158.39.75.16
Share_name: Based on the attached picture, ship that sank at given coordinations K-129.
Username: joehouston
Password: jennifer
````

When connected to SMB Share, navigate through files and retrieve a file that may lead to flag. In this case, **secretmission.txt** through command:

```
get <file> <save to local dir>
```

![[Pasted image 20241029212717.png]]

Opening the file, we can tell that the information within is trying to lead us to the flag, but we require more information regarding **Mr. P**

The mysterious individual **Mr. P** also known as **John Parangosky** extracted from [wiki/Project_Azorian ](https://en.wikipedia.org/wiki/Project_Azorian)

![[Pasted image 20241029213750.png]]

Extract file based on **secretmission.txt** guidance. 

```
get ".Parangosky/dossier.txt" <local_path>
```

Open dossier.txt and retrieve flag
# Additional Info

Additional solution / info