# Flag

> **Hacking_Arena{M1schief_M4naged}**

# Prompt

> **Do you know all the spells?

[http://3cpo.hackingarena.com:802](http://3cpo.hackingarena.com:802/)**

# Solution

Attack by requesting multiple urls from /Mysterious_Note

![[Pasted image 20241022125927.png]]

The variables to test in this case, is a list of spells in one word. Performed by doing a **Simple List** and copy pasting a list of single-worded spells (Harry Potter) from a github repository.

![[Pasted image 20241022130321.png]]

The results are sorted from largest to smallest and by checking the largest length response, we get redirected to a page with a flag.

![[Pasted image 20241022130546.png]]

![[Pasted image 20241022130603.png]]
# Additional Info

Additional solution / info