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


# Additional Info

Additional solution / info