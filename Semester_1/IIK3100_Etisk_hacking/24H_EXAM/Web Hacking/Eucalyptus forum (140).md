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

QmFtYm9v - Base64 - Bamboo
1731702874 - UNIX Timestamp - Fri 15 November 2024 20:34:34 UTC

Use CyberChef and encode the username Marlov and timestamp to where we think he logged in

Marlow - Base64 - TWFybG93
14 November 2024 11:53:00 UTC - UNIX Timestamp - 1731585180

And since we expect that Marlow logged in a bit earlier than writing his message, we will use the last four digits of the UNIX Timestamp for brute forcing his total CookieId using ffuf and a number list with leading zeroes from 0000-9999 (9999 seconds equaling 2.7 hours).

ffuf -u http://koala.hackingarena.no:803/messages.php -H "Cookie: CalypId=TWFybG93173158FUZZ" -w /home/kali/Desktop/leading_zeroes.txt -fs 2253

![[Pasted image 20241115223648.png]]

Lastly, curl the website with Marlow's activ
# Additional Info

Additional solution / info