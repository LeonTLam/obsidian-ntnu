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

The EIP tells us that the padding ended before EQoC from the random string. Count the number of letters before EQoC, which is 156.

Next step is to use pwndbg to find 'jmp esp'. This is done by running template.py with padding equal 156 and GDB as a debugger to the PID template.py is running on. 

![[Pasted image 20241115175121.png]]

Now back to template.py, add 'jmp esp' as a payload and add the payload from the previous CTF "Strawberry Exploit".

Lastly, run template.py at koala2.hackingarena.no at port 805 using command:
python3 template.py koala2.hackingarena.no 805

We should now have access to the web server and can run 'ls' and 'cat' to output the flag.

![[Pasted image 20241115175352.png]]