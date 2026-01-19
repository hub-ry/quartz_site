---
tags:
  - DSA
---


##### Binary Search [[Binary Search]]

- Assumes that the data is sorted
Steps
1. Find median index = $\lfloor \frac{l + r}{2}\rfloor$
2. Then check does (search num) = median num?
3. If no, check if (search num) is greater than or less than median num
4. Then repeat between l + r


Pseudo Pseudo Logic (PieceWise Description):

```
BinarySearch(A,x,l,r) 

n, r < l
m, A[m] = x
BS(A,x,l, m-1), A[m] > x
BS(A,x,m+1, r), A[m] < x

note: n = null,not in array, m = (current) median

```


```
Algorithm Binary Search(A:array, x:item, l:Z, R:Z)

# unsuccessful search
if r < l then:
	return n 
end if


m <- median formula

# successful search 
if A[m] = x then
	return m
end if

# split the 'deck'
if A[m] > x then 
	return BS(A, x, l, m-1);
end if

A[m] < x then
	return BS(A, x, m+1, r)
end algorithm


```



let $C_{us}$ be the cost of the operations run during the US case

let $C_{ss}$ be the cost of running the successful search case.



**We can claim that the cost of going left or right recurse is the same.**


Next Step: Runtime
[[Runtime Operations]]


Runtime for Binary:

$$T_{ss}(n) = $$

$C_{ss}, n = 1$
$C_{rs} + T_{ss}(\frac{n}{2}), otherwise$




we started with n, then $\frac{n}{2}$, then $\frac{n}{4}$, then $\frac{n}{8}$
this is $log_2(n)$


#### Proof of Binary Search Runtime [[Proof of Binary Search runtime]]
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
	   



***Another Method: Substitutions***

Iterate until you can determine the form.


$$T_{ss}(1) = C_{ss}$$
$$T_{ss}(1) = C_{rs} + T_{ss}(\frac{n}{2})$$
$T_{ss}(n) = C_{rs} + T_{ss}(\frac{n}{2})$
= 2Crs + Tss(n/4)
= 3Crs +Tss(n/8)
= 4Crs + Tss(n/16)
...
=...

we stop when $\frac{n}{2^k}$ = 1 -> k = $log_2(n)$

= Crs $log_2(n) + T_ss(\frac{n}{2log_2(n)})$

Tss(n) = Crs $log_2(n) + Css$



Therefore we can say that is O($log_2(n)$)

$o \leq C_{rs}log_2(n) + C_{ss} \leq C \cdot log_2(n)$ : c?



c > 0 