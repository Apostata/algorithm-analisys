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
   
1. There is a element in the array $A$ that is has the key $k$, then and only then, the algorithm returns the index of the element. So if the algorithm finds the key(condition C), then it returns an array index(condition D) and it will only return an array index(condition D) if the key is in the array(condition C).\
$C \longleftrightarrow D$
   
2. So if the algorithm goes through all the elements and does not find the key, then its not return an array index.\
$\not C \longleftrightarrow \not D$

3. Also to prove that the algorithm is correct, we must prove that the loop invariant(s) are true.

To prove the result, lets supose that we have the following invariant:\
\
$P(t)$ = "Before the $i$-th$ iteration, begins, $i = t$ and the array $A[1..,i-1]$ does not have the key $k$".

What we must prove?\
\
$\alpha$ = "If there isn't an element with $k$ key, then the algorithm returns a non valid index".

$\beta$ = "If there is an element with $k$ key, then the algorithm returns the index of the element".

So let's prove the $\alpha$.
- The loop can terminate when $i\ge n$. In this case, the loop executed $n$ times and $P(n+1)$ tells us that the array $A[1..n]$ (the full array) does not have the key $k$.
according to $\alpha$, the algorithm returns -1, that is a non valid index, so $\alpha$ is true.


then let's prove the $\beta$.
- The loop can terminate when $i\le n$ and $A[i] = k$, and then returns $i$. According to $\beta$, the algorithm returns the index of the element that has the key $k$, so $\beta$ is true. 

So we proved that the possible **results** of the algorithm are correct. now we must prove that the loop invariant(s) are true.

### Proof of invariant(s)
so here is our invariant(s):\
\
$P(t)$ = "Before the $i$-th$ iteration, begins, $i = t$ and the array $A[1..,i-1]$ does not have the key $k$".

Lets prove this invariant(s) by **induction**.

1. **Initialization**:
   The loop invariant is true before the first iteration - $P(1)$. Before the first iteration, $i = 1$ and the array $A[1..,i-1]$ is empty, so the array $A[1..,i-1]$ does not have the key $k$. So $P(1)$ is true.

2. **Maintenance**:
   The loop invariant is true before an iteration - $P(t)$. Suppose that the loop invariant is true before the $i$-th iteration, $P(t)$ is true. So the array $A[1..,t-1]$ does not have the key $k$. If the array $A[1..,t]$ does not have the key $k$, then the loop invariant is true.

3. **Termination**:
   The loop invariant is true after the last iteraction, at the end of the loop - $P(t+1)$. The loop can terminate when $i\ge n$. In this case, the loop executed $n$ times and $P(n+1)$ tells us that the array $A[1..n]$ (the full array) does not have the key $k$. So the loop invariant is true after the last iteration.
