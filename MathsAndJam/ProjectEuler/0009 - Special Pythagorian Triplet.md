---
date: 2026-03-24
tags:
  - projecteuler
  - pythagoras
  - nested_loops
  - bruteforce
  - inelegant
eulertime: 0.057
---

# Problem:

A Pythagorean triplet is a set of three natural numbers, $a \lt b \lt c$, for which,
$$a^2 + b^2 = c^2.$$
For example, $3^2 + 4^2 = 9 + 16 = 25 = 5^2$.
There exists exactly one Pythagorean triplet for which $a + b + c = 1000$.
Find the product $abc$.

# Solution:  31875000

```
import math  
def euler0009():  
    tripletprod = []  
    for c in range(1,500):  
        for b in range(1,500):  
            if math.sqrt(abs(c**2-b**2))%1==0 and c>=b:  
                a = math.sqrt(c**2-b**2)  
                if a+b+c==1000:  
                    trip=(a*b*c)  
                    tripletprod.append(trip)  
    return(tripletprod)  
  
print(euler0009())
```

# Commentary:

This feels deeply inelegant and very brute-force oriented. But it worked, with little tinkering needed to set up the nested loops, which surprised me.

By observing the result, and specifically the triplet ($8,15,17$), it seems plausible now to have arrived at this solution by considering that any triplet which sums to a divisor of $1000$ must lead to the only possible triplet that sums to $1000$, and this could have been worked out by trial and error, as well as an assumption that the solution may be obtained in this way.