# Binary Search

**Entry**: $\langle A, n, k \rangle$, where $A\left[1..n\right]$ is an array(vector) of $n$ elements that the value is in ascending order and $k$ is the element to be searched. $A\left[i\right] < A[i + 1]$. For every $1 \leq i \leq n$ $k$ is a number.\\

**Output**: The index of the element $A$ that the key is equal to $k$ or -1 if the element is not in the array.

$A\left[1..9\right]$ =
 | key   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
 | ----- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | value | -6  | -1  | 3   | 7   | 10  | 27  | 35  | 37  | 52  |

for $k = 27$ the output is 6.\
for $k = 2$ the output is -1.

## Pseudocode

```pseudocode
BinarySearch(A, n, k)
	
	int left = 1;
	int right = n;
	while (left <= rigth) {
		int middle = (left + right) / 2;
		if (k > A[middle]) {
			left = middle + 1;
		} else {
			right = middle;
		}
		
		if (k == A[left]) {
			return left;
		}
	}
	return -1;
```	

## Idea

The algorithm goes through the array $A$ dividing the array in half, comparing the middle element with the key $k$. If the element is equal to the key, the algorithm returns the index of the element. If the key is lesser than the middle element, the algorithm goes to the left half of the array, if the key is greater than the middle element, the algorithm goes to the right half of the array. If the algorithm goes through all the elements and does not find the key, it returns -1.

