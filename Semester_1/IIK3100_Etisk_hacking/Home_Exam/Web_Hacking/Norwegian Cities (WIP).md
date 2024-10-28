# Flag

> **FLAG**

# Prompt

> **Can you find the flag here: [http://jabba.hackingarena.com:812](http://jabba.hackingarena.com:812/)**

# Solution

Proxy and interupted website to find out that it was possible to bruteforce the cities.

Source code:
```
city=§§
```

Results were three cities with larger size, containing image of the city itself.

* Gjøvik - 378655234
* Trondheim - 275434893
* Oslo - 134357887

Numbers indicating png file name.

Can try to brute force the URL and try multiple file names containing similar numbers. (FFUF is faster here)

http://jabba.hackingarena.com:812/§§.png
# Additional Info

Additional solution / info