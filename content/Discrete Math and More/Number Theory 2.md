---
tags:
  - Discrete-Math
---


Number Theory 1 is the introduction: modulo.

Modulo can be used for cryptography and just making your computer not crash in a lot of ways. Its used in a lot more than odd/even number flags :)


***Prime***

Int only divisible by 1 or itself.
Number not prime is composite.

Primes less than 20 

{2,3,5,7,11,13,17,19}



***Finding Primes - Trial Division***

If n is a composite integer, then n a prime divisor less than or equal to $\sqrt{n}$

***Sieve of Eratosthenes***

Used to find all primes not exceeding a specified postive integer.

Find all primes less than 50. 

```
class Solution(object): 

def countPrimes(self, n): 
	if n < 2: 
		return 0 
		
	sieve = [True] * n 
	sieve[0] = sieve[1] = False 
	
	i = 2 
	
	while i * i < n: 
		if sieve[i]: 
			for j in range(i * i, n, i): 
			sieve[j] = False 
		i += 1 
		
	return sum(sieve)
```


***Computing Bézout coefficients***

i wrote it down srr its not going here.










**this note was imported from my other vault, ideas are not complete :(**




[[Discrete Math]]