# Flag

> **Hacking-Arena{H4rd d4y5 0verfl0w}**

# Prompt

> **PROMPT**

# Solution

When logging in as user=anonymous, we can tell that the unusual text-form that appears can be tested for vulnerability. Since this text-form is a unique case for user=anonymous, we need to get the cookie for this scenario.

Retrieving the cookie can be done by using **burpSuite** and intercepting the web server when logging in as anonymous. We are then left with the cookie:

```
Cookie: PHPSESSID=4h84k6rantkj5olieg85ui31q5
```

This cookie can be used with **SQLMap** to test vulnerability of specific forms, which hopefully will prompt us the tables of the web server.

````
sqlmap -u "http://r2d2.hackingarena.com:1819/index.php" --cookie="PHPSESSID=4h84k6rantkj5olieg85ui31q5" --forms --dbs

Additional information
````

