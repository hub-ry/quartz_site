
_Give a recursive algorithm for finding the maximum of a_

_finite set of integers, making use of the fact that the maximum_

_of n integers is the larger of the last integer in the_

_list and the maximum of the first n − 1 integers in the list._




```

def max(list, n):

	if (n == 1) 
		return list[0]
	
	else
		temp_max = max(list, n-1)
		
		if list[n-1] > temp_max:
			return list[n-1]
		else 
			return temp_max
	```
	
	
The recursive function will itself until n == 1.
Once that happens it return the first element of the list, which is set to temp_max. 

The most recent call before we entered as n=1 was n =2 , so compare list[2-1] with temp_max which will be list[0]. If our element is greater, set temp_max to that elemnet, if its not, compare n = 3 cycle with temp_max, list[0]





```

_Give a recursive algorithm for finding a mode of a list of_

_integers. (A mode is an element in the list that occurs at_

_least as often as every other element.)_

```
def find (list, n):

	
```








**this note was imported from my other vault, ideas are not complete :(**




[[Discrete Math]]