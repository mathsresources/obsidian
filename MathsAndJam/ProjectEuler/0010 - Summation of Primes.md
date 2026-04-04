---
date: 2026-03-24
tags:
  - projecteuler
  - prime_numbers
  - sum
eulertime: 1.917
---

# Problem:

The sum of the primes below $10$ is $2 + 3 + 5 + 7 = 17$.
Find the sum of all the primes below two million.

# Solution:  142913828922

```
import math, sympy  
def euler0010(target):  
    primes = []  
    n = 1  
    primesum = 0  
    while n<=target:  
        if sympy.isprime(n)==True:  
            primes.append(n)  
            primesum += n  
        n+=1  
    print(primes)  
    print(primesum)  
euler0010(2000000)
```

# Commentary:

This felt trivially easy compared to the previous problems. A nice encouragement for those working through the problems to complete the first ten?

A fairly slow solution though - inefficient?