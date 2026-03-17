---
date: 2026-03-17
tags:
  - projecteuler
  - prime_numbers
  - divisibility
  - factors
eulertime: 0.018
---

# Problem:

The prime factors of $13195$ are $5, 7, 13$ and $29$.
What is the largest prime factor of the number $600851475143$?

# Solution: 6857

```
import math, sympy  
def euler0003(target):  
    prime_factors = []  
    primes = 2  
    root = math.floor(math.sqrt(target))  
    while primes<=root:  
        if target%primes==0 and sympy.isprime(primes)==True:  
            prime_factors.append(primes)  
            if sympy.isprime(target // primes):  
                prime_factors.append(target // primes)  
        primes+=1  
    print(prime_factors)  
euler0003(600851475143)
```

# Commentary:

This took a surprising number of attempts to get right. It ended up feeling more complete and checkable by instead creating a function to list all prime factors of the target number.