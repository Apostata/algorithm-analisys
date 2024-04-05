# Ordenated Linear Search

**Entry**: $\langle A, n, k \rangle$, where $A\left[1..n\right]$ is an array(vector) of $n$ elements that the value is in ascending order and $k$ is the element to be searched. $A\left[i\right] < A[i + 1]$. For every $1 \leq i \leq n$ $k$ is a number.\
\
**Output**: The index of the element $A$ that the key is equal to $k$ or -1 if the element is not in the array.

$A\left[1..9\right]$ =
 | key   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
 | ----- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | value | -6  | -1  | 3   | 7   | 10  | 27  | 35  | 37  | 52  |

for $k = 27$ the output is 27.\
for $k = 2$ the output is 6.

## Pseudocode

```pseudocode
OrdenatedSearch(A, n, k)
	
	i = 1
	while i <= n and A[i] < k
		i = i + 1
		if i <= n and A[i] == k
			return i
		else
			return -1
```	

## Idea

The algorithm goes through the array $A$ from the first element to an element that is greater than the key $k$, because it is ordenated in crescent order comparing each element with the key $k$. If the element is equal to the key, the algorithm returns the index of the element, but if the element is greater than the key, the algorithm returns -1, just like if the element is not in the array.