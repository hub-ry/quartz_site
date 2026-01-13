introduction introduction

$$T_{SS}(n) \leq T_{US}(n)$$


T : Input -> $R^+$ : Runtime Expressions, Close Forms, "Cost"



Cost of unsuccessful = Cost (declaration) + Cost (assignments)


#### Figuring Cost of Linear Search


```
Algorithm Linear Search(A:array, x:item):
	let n be the size of A
	i <- 0
	
	while (i < n) and A[i] != x do:
		i <- i+1
	end while
	
	if i = n     // unsuccessful search
	
	if i < n     // successful search case
	
	
```


Cost of unsuccessful = Cost (declaration) + Cost (assignments)
					+Cdd + Casg (equals 0 line)
					+Ccmp + (Caa)^n + Ccmp + Cand (while loop condition)n
					+(Cadd + Casg)n
					+ Cret





Tus(n) for assigns. is $\Theta$ (n)

more on bigTheta later [[Algorithms and Big-O]] from discrete math for reference

