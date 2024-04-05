# Algorithm Analysis Course

## Introduction
What is an algorithm?
They are sequences of steps described in an unambiguous way that correctly solve a problem.

- What is algorithm analysis?
It is the science that studies the efficiency of algorithms, allowing us to predict behavior and performance without the need to implement it on a specific device.

## Iteractive Algorithms
What is an iterative algorithm?
- It is an algorithm that uses loops to repeat a block of code until a certain condition is met.

## Loop Invariant (P)

What is a loop invariant?
- It is a property that is true before each iteration of a loop. In other words is a property that is coserved by the loop, or that is a constant in each iteration of the loop. In other words, the loop invariant is a property that grants that the loop will end.\
So what?
- It is used to prove the correctness of an algorithm.\
How?
- We must prove that the loop invariant is true before the first iteration, that if it is true before an iteration.

### Notation
- $P$: Loop invariant.
- $T$: Number of times that the loop will be executed.
- $t$: Number of iterations of the loop.
- $i$: Generic number of iterations.
- $n$: Number of elements in the array.
- $A$: Array of elements.
- $k$: Key to be searched.

- $P(1)$: Loop invariant - Property that is true before the first iteration, or before the loop starts..
- $P(t)$: Loop invariant - Property that is true before the $t$-th iteration.
- $P(t+1)$: Loop invariant - Property that is true after the $t$-th iteration, or after the loop ends.

## How to prove the correctness of an iterative algorithm?

- What is the loop invariant(s) of the algorithm?
- How can we prove that is a valid invariant?
- We must prove that is correct for all possible inputs (induction).
- We must prove that is valid for any $n$ (number of elements in the array)
  
### Proof of the loop invariant(s)
For the loop invariant(s) proof, we must prove that the loop invariant(s) are true before the first iteration, that if the loop invariant(s) are true before an iteration, they are true after the iteration, and that if the loop invariant(s) are true when the loop ends, the algorithm is correct.

**induction**: It is a way to prove that a property is true for all natural numbers. It is divided into three steps:

1. **Initialization**: Prove that the loop invariant is true before the first iteration - $P(1)$.
2. **Maintenance**: Prove that if the loop invariant is true before an iteration - $P(i)$.
3. **Termination**: Prove that if the loop invariant is true after the last iteraction, at the end of the loop - $P(t+1)$.

Obviviouly, as we do not know the number of iterations that the loop will perform, we should prove that **Initialization** is true, **Maintenance** is true, before any number of iterations between $1$ and $i$ and **Termination** is true.

### Correctness
The loop invariant is a property that remains true before and after each iteration of a loop in an algorithm. It is used to help prove the correctness of an algorithm, but it is not sufficient on its own to prove total correctness.

Proving the loop invariant involves showing that:

The invariant is true before the first iteration of the loop (initialization).
If the invariant is true before an iteration of the loop, it remains true for the next iteration (maintenance).
Proving the correctness of an algorithm as a whole involves more than just proving the loop invariant. In addition to proving the loop invariant, you also need to show that:

The algorithm terminates (termination). For loops, this usually involves showing that there is a variable that is approaching a limit with each iteration.
When the algorithm terminates, the result is correct (finalization). This usually involves showing that the loop invariant, along with the loop exit condition, implies the desired post-condition of the algorithm.
Therefore, the loop invariant is a tool used in proving the correctness of an algorithm, but proving the loop invariant alone is not sufficient to prove the total correctness of an algorithm.

## Pseudocode
- It is a way to describe an algorithm in a way that is independent of any programming language.

## Content
- [Linear Search](linear_search.md)
- [Ordenated Linear Search](ordenated_linear_search.md)
- [Better Ordenated Linear Search](better_ordenated_linear_search.md)
- [Binary Search](binary_search.md)

### Reference and Credits

-[Introdução à análise de algoritmos](https://www.youtube.com/watch?v=_HBTCUNPxOg&list=PLncEdvQ20-mgGanwuFczm-4IwIdIcIiha&index=1) by  [Carla Negri Lintzmayer](http://professor.ufabc.edu.br/~carla.negri/) 

Thanks [Carla Negri Lintzmayer](http://professor.ufabc.edu.br/~carla.negri/) to share your knowledge.


