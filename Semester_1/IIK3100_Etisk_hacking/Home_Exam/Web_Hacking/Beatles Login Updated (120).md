# Flag

> **FLAG**

# Prompt

> **Find the user: [http://vader.hackingarena.com:825](http://vader.hackingarena.com:825/)**

# Solution

Since we are working on multiple user-logins and already have access to 3 of them. I decided to use burp and collect the 3 different cookie id's.

* John: beatlesid=11161
* Paul: beatlesid=15803
* George: beatlesid=10303

Immediately we can tell that the id's are prime numbers, which led me to brute force the cookie id's with all prime numbers between 11161 and 15803 using **fuff**


# Additional Info

Additional solution / info