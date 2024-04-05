# Better Ordenated Linear Search

**Entry**: $\langle A, n, k \rangle$, where $A\left[1..n\right]$ is an array(vector) of $n$ elements that the value is in ascending order and $k$ is the element to be searched. $A\left[i\right] < A[i + 1]$. for every $1 \leq i \leq n$ $k$ is a number.\
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
BetterOrdenatedSearch(A, n, k)
	
	i = A[n/2]
	while i <= n and i >= 1 and A[i] != k
	if A[i] == k
		return i
	else if k > A[i]
		i = i + 1
	else
		i = i - 1

```	

## Idea

As the algoritm is ordenated you can compare the $k$ with $A\frac{\left[i\right]}{2}$, then if $k$ is greater than $A\frac{\left[i\right]}{2}$ you can go to the next element $A\frac{\left[i + 1\right]}{2}$, but if $k$ is lesser to $A\frac{\left[i\right]}{2}$ you can go back to the previous element $A\frac{\left[i - 1\right]}{2}$ . If you find the element that is equal to $k$ you can return the index of the element, but if you go through all the the halfs of the array and does not find the key, it returns -1.