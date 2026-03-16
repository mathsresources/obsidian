Problem:

If we list all the natural numbers below $10$ that are multiples of $3$ or $5$, we get $3, 5, 6$ and $9$. The sum of these multiples is $23$. Find the sum of all the multiples of $3$ or $5$ below $1000$.

Solution:

```
div=[3,5]  
n = 1  
m = 999  
numbers = []  
while(n<=m):  
    if n%div[0]==0 or n%div[1]==0:  
        print(n,'is divisible by at least one of 3 or 5')  
        numbers.append(n)  
    else:  
        print(n,'is not divisible by 3 or 5')  
    n+=1   
print(sum(numbers))
```

Commentary:

I tried to do this without making use of any knowledge of the sums of arithmetic series, or even just natural numbers. Reading further on suggested approaches, in future I will make more use of maths rather than aiming for one based solely on coding a brute force approach.

Date: Sunday 15th March, 2026