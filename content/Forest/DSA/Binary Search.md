---
tags:
  - DSA
---


- Assumes that the data is sorted


Steps
1. Find median index = $\lfloor \frac{l + r}{2}\rfloor$
2. Then check does (search num) = median num?
3. If no, check if (search num) is greater than or less than median num
4. Then repeat between l + r


***PieceWise Description:***

```
BinarySearch(A,x,l,r) 

n, r < l
m, A[m] = x
BS(A,x,l, m-1), A[m] > x
BS(A,x,m+1, r), A[m] < x

note: n = null,not in array, m = (current) median

```




Pseudocode:
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