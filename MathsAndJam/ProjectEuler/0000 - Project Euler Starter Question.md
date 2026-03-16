Project Euler: [website](https://projecteuler.net)

Problem:

Find the sum of all the squares of odd numbers from 1 to 425000

Solution:

```
n = 1  
m = 425000  
numbers = []  
while (n <= m):  
    numbers.append(pow(n,2))  
    n += 2  
print(sum(numbers))
```

Commentary:

Needed when creating an account. 
Adapted from the solution to [[0001 - Multiples of Three and Five]].
