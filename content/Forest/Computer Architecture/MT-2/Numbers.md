
<span style="color:rgb(146, 208, 80)">2's Complement</span>
- Literally just flip the bits and then + 1, if the binary string gets longer after + 1 then ignore the extended carry bit. 
- If you two's complement the most negative number in a big sequence you will get overflow, for example:

1000 -> 0111 + 1 = 1000


- <span style="color:rgb(146, 208, 80)">Sign extension:</span>
	- extend negative numbers with 1's, positive with 0's

- <span style="color:rgb(146, 208, 80)">Overflow</span>: When you add two numbers of the same sign and it makes a different sign.

```
Examples:


F011 is signed integer. Decimal Value?

1111 0000 0001 0001 ~ a negative number

0000 1111 1110 1111 ~ 0FEF

Decimal: 15 x 16^2 + 14x16 + 15 = 4079

Value = -4079

```