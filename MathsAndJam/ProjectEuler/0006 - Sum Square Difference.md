---
date: 2026-03-19
tags:
  - square_numbers
eulertime: 0.000
---

# Problem:

The sum of the squares of the first ten natural numbers is,
$$1^2 + 2^2 + ... + 10^2 = 385.$$
The square of the sum of the first ten natural numbers is,
$$(1 + 2 + ... + 10)^2 = 55^2 = 3025.$$
Hence the difference between the sum of the squares of the first ten natural numbers and the square of the sum is $3025 - 385 = 2640$.

Find the difference between the sum of the squares of the first one hundred natural numbers and the square of the sum.

# Solution:  25164150 

```
def square_sums(n):  
    squares = []  
    for x in range(1,n+1):  
        squares.append(x**2)  
    sumsquares = sum(squares)  
    sumsq = sum(list(range(1,n+1)))  
    squaresums = sumsq**2  
    print(squaresums-sumsquares)  
square_sums(100)
```

# Commentary:

This was very trivial to complete using Python. I haven't explored any algebraic properties of this problem yet.