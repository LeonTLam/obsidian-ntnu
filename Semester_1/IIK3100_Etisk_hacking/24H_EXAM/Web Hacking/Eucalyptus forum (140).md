# Flag

> Hacking-Arena{In the jungle, the mighty jungle}

# Prompt

> My koala hacker team already tried this challenge. Just ask Bamboo, his password is Eucalyptus (reverse).

>[http://koala.hackingarena.no:803](http://koala.hackingarena.no:803/) [http://koala.hackingarena.com:803](http://koala.hackingarena.com:803/) (same site)

>I'd rather work with them than with some boring Pandas :D

# Solution

Based on the prompt, log into the website with username and password:

Bamboo
sutpylacuE

![[Pasted image 20241115205845.png]]

Read through the chat logs and try to log in as Marlow without a password. Realize you cannot change userId either. BurpSuite and proxy the website and find the cookieId:

![[Pasted image 20241115210004.png]]

Split the CalypId in two parts, the first one being:

QmFtYm9v - Base64
1731702874 - UNIX Timestamp


# Additional Info

Additional solution / info