# Flag

> skarddalseggi

# Prompt

> Our tartget has a quite strong password, his MD5 hash is 53ba4c338b0578878240cff683fa9a1d

>Well, we are also smart, so we placed a thin layer of hardly visible dust on every key on his keyboard :D We checked it after login and he used the following keys: a d e g i k l r s

>He didn't touch the Shift or AltGr, no capital letter, no number, no special character. Can you crack his password?

>Non flag format

# Solution

Utilize hash-identifier to discover the hash-type to be likely MD5.

![[Pasted image 20241115133719.png]]

Utilize hash-cat to crack the STRONG password (like from length 8 upwards)

hashcat -m 0 -a 3 "53ba4c338b0578878240cff683fa9a1d" -1 adegiklrs ?1?1?1?1?1?1?1?1?1?1?1?1?1?1?1 -increment

![[Pasted image 20241115225411.png]]

This will attempt cracking the hash with combinations from 1 letter upwards, where it ended on a string-value at length 13.
# Additional Info

Additional solution / info