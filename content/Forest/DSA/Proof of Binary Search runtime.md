How do we prove the respective runtime for this?


1. Induction (mentioned in discrete math)
	1. Start with an informed guess.
	  $T_{ss}(n) = C_{rs}log_2(n) + C_{ss}$
	2. Basis
	  $C_{rs} log_2(1) + C_{ss} = C_{ss}$
	  0 + $C_{ss} = C_{ss}$
	3. Induction (n > 1): Assume the statement is true for $n' < n$ (Inductive Hypothesis)

	  $T_{ss}(n) = C_{rs} + T_{ss}(\frac{n}{2})$
	  $=$ $C_{rs} + C_{rs}log_2(\frac{n}{2}) + C_{ss}$
	  $= C_{rs} + C_{rs}(log_2(n) - log_2(2)) + C_{ss}$
	   $=C_{rs}log_2(n) + C_{ss}$ 
	   




