$a_n = n^2$
$a_0 = 0$
$a_1 = 1$
$a_2 = 4$
$\text{base case : } a_0 = 0$
$a_n = a_{n-1} + (2n -1)$


**Fibonacci Proof (Strong Induction)**


Prove $f_1^2 + f_2^2 + ... + f_n^2 = f_nf_{n+1}$     

base case: n = 1
Fibonacci numbers: 0 1 1 2 3 5 etc

$0^2 + 1^2 = 1 * 1$ ~ the base case holds true

Induction Step:

$f_1^2 + f_2^2 + ... + f_n^2 + f_{n+1}^2 = f_n f_{n+1}+f_{n+1}^2$

factor out $f_{n+1}$ on right side:

$f_{n+1} (f_n + f_{n+1})$ 

Notice the expression in the parenthesis:

$f_{n+1}f_{n+2}$

The proof is complete






**this note was imported from my other vault, ideas are not complete :(**




[[Discrete Math]]