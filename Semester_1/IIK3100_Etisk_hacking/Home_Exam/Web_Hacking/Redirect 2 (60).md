# Flag

> **Hacking-Arena{XSSSSSSSSSSSSS_ssst!}**

# Prompt

> **Can you redirect [http://3cpo.hackingarena.com:821](http://3cpo.hackingarena.com:821/) to [http://3cpo.hackingarena.com:822](http://3cpo.hackingarena.com:822/) ?**

# Solution

Attempting a simple **href** attribute with the whole URL provides us with information regarding input filtering where "hacking" is filtered out to prevent exploitation. 

By reading and researching documentation regarding XSS filtering on [cheatsheetseries.owasp.org](https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html) we can attempt a workaround by encoding the whole URL so that the website does not recognize "hacking" anymore.

On any website or tool, for example [hashemian.com](https://www.hashemian.com/tools/html-url-encode-decode.php) I simply used "Decimal Encode" on the entire URL and inputted a simple href-attribute with a decimal decoded URL to http://3cpo.hackingarena.com:822

# Additional Info

Additional solution / info