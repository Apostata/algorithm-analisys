# Linear Search

**Entry**: $\langle A, n, k \rangle$, where $A\left[1..n\right]$ is an array(vector) of $n$ elements and $k$ is the element to be searched.\
\
**Output**: The key of the element $A$ that the key is equal to $k$ or -1 if the element is not in the array.

$A\left[1..9\right]$ =
 | key   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
 | ----- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | value | 16  | 9   | -3  | 5   | 4   | 27  | 46  | 11  | -5  |
  
\
for $k = 27$ the output is 6.\
for $k = 2$ the output is -1.

## Pseudocode

```pseudocode
SimpleSearch(A, n, k)
	
	i = 1
	while i <= n and A[i] != k
		i = i + 1
		if i <= n and A[i] == k
			return i
		else
			return -1
```

## Idea

The algorithm goes through the array $A$ from the first element to the last element, comparing each element with the key $k$. If the element is equal to the key, the algorithm returns the index of the element. If the algorithm goes through all the elements and does not find the key, it returns -1.

## Correctness
   
1. There is a element in the array $A$ that is has the key $k$, then and only then, the algorithm returns the index of the element. So if the algorithm finds the key(condition C), then it returns an array index(condition D) and it will only return an array index(condition D) if the key is in the array(condition C). $C \longleftrightarrow D$
   
2. So if the algorithm goes through all the elements and does not find the key, then its not return an array index.
3. $\not C \longleftrightarrow \not D$

4. Also to prove that the algorithm is correct, we must prove that the loop invariant(s) are true.
   
### Proof of invariant(s)

