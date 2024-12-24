# Flag

> **UiO-Hacking-Arena{Lucy 1n the Sky w1th Flags}**

# Prompt

> **There must be something hidden here: [http://r2d2.hackingarena.com:1811](http://r2d2.hackingarena.com:1811/)**

# Solution

Inspect website and recognize song.php and parameter songid that is an integer.

Utilize Burp to intrude and interfere with responses to check multiple songid's.

Instead of bruteforcing and checking thousands of songid's, recognize a pattern where all albums end with 53. 

Edit payload and attack all songid's with a suffix of 53. Sort all attacks by largest to lowest content length. Scroll through the responses until finding a html file with appropriate flag.

# Additional Info

Additional solution / info