---
date: 2026-03-19
tags:
  - projecteuler
  - multiples
  - divisibility
  - prime_factors
  - nocode
  - nocodesolutionyet
eulertime: NA
---

# Problem:

$2520$ is the smallest number that can be divided by each of the numbers from $1$ to $10$ without any remainder.

What is the smallest positive number that is **evenly divisible** (divisible with no remainder) by all of the numbers from $1$ to $20$?

# Solution:  232792560

```
No Python solution yet.
```

# Commentary:

This is the same as asking for the lowest common multiple of the natural numbers from 1 to 20.

Prime factorisations of the (non-prime) natural numbers greater than 1:

$$
\begin{align}
4 &= 2^2\\
6 &= 2 \times 3\\
8 &=2^3\\
10 &= 2 \times 5\\
12 &= 2^2\times 3\\
14 &= 2\times 7\\
15 &=3 \times 5\\
16 &= 2^4\\
18 &= 2\times 3^2\\
20 &= 2^2 \times 5\\
\end{align}
$$

The lowest common multiple of the natural numbers from 1 to 20 is:

$$
2^4 \times 3^3 \times 5 \times 7 \times 11\times 13 \times 17 \times 19 = 232792560
$$

Hence no coding is needed. However, I would like to try creating some Python code for this as an exercise.