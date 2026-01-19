---
tags:
  - Discrete-Math
---


The time required to solve a problem is determined by:

1. Number of operations
2. Size of the input
3. Speed of Hardware/Software

Big-O Notation estimates the growth of functions representing the number of operations only. (Complexity)


***Analyzing Algorithms***

- Depends on the number of iterations of loops
- How much work is done each iteration

```
n^2

for i:= 1 to n do
	for j:=1 to n do
		s[i] := s[i] + s[j]
		
```

We use the tightest bound:

$n^3+ 11n^2 + n^{.25}$  is just O($n^3$)

'At most this much time'

***Big Omega***

This is the lower bound. Note big-O is the upper bound.

For example:

$n^3 + 11n^2 + n^{.25}$

For this big Omega is strictly nothing greater than $O(n^3)$, technically if it was a weak bound you can go faster than $n^3$, but often these are used in their tightest forms.

'At least this much time'


***Big Theta***

This is bigO and bigOmega at the same time.

Check the upper bound (bigO)

Check lower bound (bigOmega)

If both hold, with your selected rate, that is Big Theta.




**this note was imported from my other vault, ideas are not complete :(**


[[Discrete Math]]