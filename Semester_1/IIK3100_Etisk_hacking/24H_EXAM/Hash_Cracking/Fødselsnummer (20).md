# Flag

> 06026263422

# Prompt

> His password is his fødselsnummer. That's what we know: 06cd97558029ae3a9e1f7fcdcd74771d

>Non flag format

# Solution

Utilize hash-identifier to discover the hash type to be MD5

![[Pasted image 20241115133420.png]]

Utilize hash-cat to crack the hash-code with pattern of 11 digits. Additionally, make hash-cat increment starting with fewer digits and gradually increase with command (?d for digits):

hashcat -m 0 -a 3 --increment "/home/kali/Desktop/hash.txt" ?d?d?d?d?d?d?d?d?d?d?d

![[Pasted image 20241115133346.png]]
# Additional Info

Additional solution / info