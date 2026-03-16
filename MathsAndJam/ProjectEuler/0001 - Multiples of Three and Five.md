---
date: 2026-03-15
tags:
  - projecteuler
  - divisibility
  - while_loop
  - multiples
  - sequences
  - nocode
eulertime: 0.002
---
# Problem:

If we list all the natural numbers below $10$ that are multiples of $3$ or $5$, we get $3, 5, 6$ and $9$. The sum of these multiples is $23$. Find the sum of all the multiples of $3$ or $5$ below $1000$.

# Solution: 233168

```
def euler0001(n=1,m=999):  
    div=[3,5]  
    numbers = []  
    while(n<=m):  
        if n%div[0]==0 or n%div[1]==0:  
            print(n,'is divisible by at least one of 3 or 5')  
            numbers.append(n)  
        else:  
            print(n,'is not divisible by 3 or 5')  
        n+=1  
    print(numbers)  
    print(sum(numbers))  
euler0001()
```

# Commentary:

I first tried to do this without making use of any knowledge of the sums of arithmetic series, or even just natural numbers. Reading further on suggested approaches, in future I will make more use of maths in my solutions rather than aiming for one based solely on coding a brute force approach. Below is a more maths-based method:

The sum of the multiples of 3 and 5 under 1000 can be calculated as:

$$
\text{sum of the multiples of 3 }+\text{ sum of the multiples of 5 }-\text{ sum of the multiples of 15}
$$

The sum of the natural numbers less than 1000 is given by:

$$
\sum^{N}_{n=1} n=\frac{1}{2}N(N+1)
$$

The multiples of 3 below 999 extend to 999, and their sum is:

$$
3\times \sum^{333}_{n=1} n = 3\times \frac{1}{2}\times 333 \times 334 = 166833 
$$

The multiples of 5 below 999 extend to 995, and their sum is:

$$
5\times \sum^{199}_{n=1} n = 5\times \frac{1}{2}\times 199 \times 200 = 99500
$$

The multiples of 15 below 999 extend to 990, and their sum is:

$$
15\times \sum^{990}_{n=1} n = 15\times \frac{1}{2}\times 66 \times 67 = 33165 
$$

Giving a result, without any coding, of:

$$
166833+99500-33165=233168
$$