---
date: 2026-03-20
tags:
  - projecteuler
  - prime_numbers
  - ordinal
eulertime: 0.068
---

# Problem:

By listing the first six prime numbers: $2, 3, 5, 7, 11$, and $13$, we can see that the $6$th prime is $13$.

What is the $10\,001$st prime number?

# Solution:  104743

```
import math, sympy  
def ordinal_prime(n):  
    ord = 0  
    m = 1  
    while ord<n:  
        m +=1  
        if sympy.isprime(m):  
            ord += 1  
    print(m)  
ordinal_prime(10001)
```

# Commentary:

A nice, easy challenge once the timing of when to tick forward the ordinal count and the number count was figured out correctly.

It took 14.836 seconds to find the millionth prime, which is 15485863.

For context, Euler found a 10 digit prime number ($M_{31}$) in 1772.