--10/9/2023--
#### Subtraction
A+B is A+B+0
A-B is A+(!B+1)

XOR causes a bit to be opposite of de other

To subtract, we
	1. throw an xor on the second input carry with the carry in input that as the subtract bit (holy cow)
	2. if the carry in is one, now it both inverts the second values, and 